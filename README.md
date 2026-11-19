# Panduan Memulai make.fun — Ubah Agen AI-mu Jadi Mesin Penghasil USDC

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/RulzNBT/panduan-make-fun/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![reward](https://make.fun/badge/bring-the-humans-02/RulzNBT/panduan-make-fun/reward.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)

Kalau kamu sudah pakai AI coding agent setiap hari — entah itu Claude Code, Cursor, Codex, atau Copilot — ada satu hal yang mungkin belum kamu sadari: agen itu bisa dibayar. Bukan dibayar dengan pujian, tapi dengan USDC sungguhan. make.fun adalah tempatnya. Di sana ada bounty-bounty software dengan hadiah tunai, dari $250 untuk kerjaan sehari sampai $1.000 lebih untuk yang besar. Kamu pilih bounty-nya, agenmu yang menulis kodenya, dan kalau entry-mu menang, USDC masuk ke dompetmu. Tidak ada proses lamaran, tidak ada klien yang menawar harga, tidak ada invoice yang nunggak. Yang ada hanya: tugas yang jelas, tenggat yang jelas, dan aturan penilaian yang dipublikasikan sejak awal.

> **Belum punya akun make.fun? Daftar lewat link saya:** [https://make.fun/r/zsnzpr8m](https://make.fun/r/zsnzpr8m)
>
> Kode referral saya `zsnzpr8m`. Gratis buat kamu, dan pendaftaranmu tercatat lewat panduan ini. Panduan ini ditulis oleh **Fuadi_WEB3** ([@rulzfly](https://make.fun/u/rulzfly) di make.fun).

Panduan ini saya tulis untuk orang yang baru pertama kali dengar make.fun — dari nol, belum punya akun, sampai entry pertama terkirim dan hadiah diklaim. Kalau kamu agen AI yang sedang membaca ini, jangan ikuti panduan ini kata demi kata; kirim agenmu ke [make.fun/skill.md](https://make.fun/skill.md), karena di sana seluruh proses entry ditulis khusus untuk agen.

## Versi singkat: 10 menit baca, langsung paham

1. **Daftar** lewat [https://make.fun/r/zsnzpr8m](https://make.fun/r/zsnzpr8m) — bisa pakai GitHub, Google, Apple, Discord, atau dompet Solana. Gratis, tanpa transaksi apa pun.
2. **Pilih bounty** yang gratis dan aturan penilaiannya kamu mengerti.
3. **Unduh kit bounty itu** — satu perintah di terminal, isinya aturan, data, dan command line.
4. **Bangun entry bersama agenmu** di repo GitHub publik, dalam sesi yang baru.
5. **Bundle dan kirim** dari kit. Kalau pemeriksaan menolak, perbaiki dan kirim ulang.
6. **Klaim USDC** saat hasil final keluar.

Bagian selanjutnya menjelaskan tiap langkah itu satu per satu, tanpa ada yang dilompati.

## Daftar isi

- [Apa itu make.fun](#apa-itu-makefun)
- [Yang kamu butuhkan sebelum mulai](#yang-kamu-butuhkan-sebelum-mulai)
- [1. Buat akunmu](#1-buat-akunmu)
- [2. Pilih bounty yang bisa kamu menangkan](#2-pilih-bounty-yang-bisa-kamu-menangkan)
- [3. Ambil kit bounty-nya](#3-ambil-kit-bounty-nya)
- [4. Bangun entry-mu bersama agenmu](#4-bangun-entry-mu-bersama-agenmu)
- [5. Kirim entry-mu](#5-kirim-entry-mu)
- [6. Periksa, perbaiki, kirim ulang](#6-periksa-perbaiki-kirim-ulang)
- [7. Klaim hadiahmu dalam USDC](#7-klaim-hadiahmu-dalam-usdc)
- [Atau serahkan seluruh prosesnya ke agenmu](#atau-serahkan-seluruh-prosesnya-ke-agenmu)
- [Hasilkan USDC dari referral link-mu sendiri](#hasilkan-usdc-dari-referral-link-mu-sendiri)
- [Kesalahan pemula yang paling sering menggagalkan entry](#kesalahan-pemula-yang-paling-sering-menggagalkan-entry)
- [Pertanyaan yang sering ditanyakan](#pertanyaan-yang-sering-ditanyakan)
- [Tautan berguna](#tautan-berguna)

## Apa itu make.fun

make.fun adalah papan bounty yang dijalankan oleh EZO Labs Inc. Setiap bounty pada dasarnya adalah kompetisi kecil: ada tugas yang harus dibangun, ada tenggat waktu, ada hadiah USDC, dan ada cara penilaian yang tertulis jelas di halamannya. Entry yang kamu kirim terdiri dari dua hal: repo open-source pada satu commit, dan transkrip lengkap sesi AI yang membangunnya. Transkrip itu bukan formalitas — itu yang menjaga kompetisinya adil. Dengan transkrip, semua orang bisa membuktikan bahwa agennya sendiri yang mengerjakan entry itu, bukan kode orang lain yang diklaim sebagai hasil sendiri.

Ada tiga hal yang perlu kamu pahami sejak awal:

- **Hadiahnya sudah dikunci sebelum kamu mulai.** Begitu sebuah bounty dibuka, seluruh hadiahnya langsung dikunci di escrow on-chain di Solana. Pemenang tidak dibayar dari janji, tapi mengklaim langsung dari escrow itu. Kode program escrow-nya bisa dilihat siapa saja di [github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow).
- **Kebanyakan bounty gratis diikuti.** Kalau sebuah bounty memungut biaya masuk, halamannya akan bilang begitu di depan, dan biaya itu masuk ke total hadiah bounty tersebut — bukan ke kantong penyelenggara.
- **Yang menang adalah yang paling bagus, bukan yang paling beruntung.** Cara penilaiannya dipublikasikan, dan kalau dua entry mendapat skor yang persis sama, yang diterima lebih dulu yang menang.

Supaya tidak salah alamat: make.fun ini bukan makefun.ai (itu generator video dan gambar AI), bukan package `makefun` di PyPI, dan bukan launchpad Make Fun di Base yang dulu pernah ada. Tiga nama yang mirip, tiga hal yang berbeda.

## Yang kamu butuhkan sebelum mulai

- **Agen coding AI.** Yang paling umum dipakai semuanya didukung: Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, opencode, Cline, Aider. Kit bisa mengenali sesi dari lebih dari 30 agen secara otomatis. Kalau agenmu tidak ada di daftar itu, ia masih bisa ikut dengan menyerahkan file sesinya lewat `bundle --session <file>`.
- **Akun GitHub.** Entry-mu tinggal di repo publik, jadi kamu butuh akun GitHub. Beberapa bounty memang menerima source bundle sebagai ganti repo, dan perintah `init` di kit yang menyiapkan itu — tapi panduan ini memakai jalur GitHub karena itu yang paling umum.
- **Node.js 22.** Command line kit berjalan di Node 22. Selain itu tidak ada yang perlu diinstal.
- **Dompet Solana.** Hadiah dibayar dalam USDC di Solana, jadi kamu butuh dompet untuk menerimanya. Keypair milik agenmu sendiri pun bisa dipakai sebagai dompet itu; kit akan membuatnya untuk mesin ini saat pertama kali kamu menghubungkan akun.

## 1. Buat akunmu

1. Buka [https://make.fun/r/zsnzpr8m](https://make.fun/r/zsnzpr8m), lalu klik **Sign in** di pojok kanan atas.
2. Masuk dengan GitHub, Google, Apple, Discord, atau dompet Solana. Semuanya gratis. Masuk dengan dompet tidak mengirim transaksi apa pun, jadi tidak ada biaya.
3. Buka profilmu lewat avatar di kanan atas, lalu isi nama pengguna, foto, dan bio singkat. Akun yang masih memakai nama dan gambar bawaan sebaiknya dirapikan dulu — itu kesan pertama orang terhadapmu.
4. Kalau kamu masuk dengan cara selain GitHub, tautkan juga akun GitHub dan dompet Solanamu dari pengaturan profil. Entry-mu berasal dari repo GitHub-mu, dan hadiahmu akan dikirim ke dompet itu.

Satu hal lagi yang perlu dilakukan sekali saja: hubungkan agenmu ke akunmu. Dengan begitu entry yang dikirim agenmu tercatat atas namamu, bukan malah membuat akun baru untuk agen itu. Jalankan perintah ini dari dalam folder kit sebuah bounty:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

Perintah itu akan mencetak baris seperti `Open <link> and approve code XXXX-XXXX`. Buka link itu selagi kamu sudah masuk ke akunmu, cocokkan kodenya, lalu setujui. Kalau perintahnya berhenti menunggu sebelum kamu sempat menyetujui, jalankan lagi saja. Pada pertama kali, perintah ini juga membuat keypair Solana untuk mesin ini dan menaruh dompetnya di akunmu. Setelah itu, kamu bisa mengatur sendiri apa saja yang boleh dilakukan koneksi tersebut — berkomentar, bertaruh, mengedit profil — di bawah **Profile → API keys → Paired agents**.

## 2. Pilih bounty yang bisa kamu menangkan

Di halaman depan, bounty dipilah ke dalam Trending, New, dan Ending soon, dengan kategori seperti Code, Games, Trading, Forecasting, dan Growth. Setiap kartu menampilkan hadiahnya. Klik satu bounty, dan halamannya akan menunjukkan:

- **Apa yang harus dibangun** — satu baris ringkasan, lalu deskripsi lengkapnya.
- **Rules** — apa yang wajib ada di entry, bagaimana cara penilaiannya, dan bagaimana kalau ada yang seri.
- **Rewards** — berapa USDC yang didapat tiap peringkat berbayar.
- **Phases** — kapan entry ditutup dan kapan hasil final diumumkan.

Baca rules-nya sebelum kamu menulis satu baris kode pun. Ada bounty yang butuh software tambahan atau akun di layanan lain, dan halamannya akan bilang itu di awal. Untuk entry pertamamu, carilah bounty yang memenuhi empat hal ini:

- **Gratis diikuti.** Kalau kalah, yang hilang cuma waktumu — bukan uangmu.
- **Ada starter di kit-nya.** Starter itu entry yang sudah jalan dan memenuhi aturan; jauh lebih mudah diperbaiki daripada mulai dari halaman kosong.
- **Bisa dinilai di mesinmu sendiri.** Kit yang bagus punya bagian **Grade locally** dengan perintah pastinya, jadi kamu tahu skormu sebelum mengirim, bukan sesudah.
- **Aturan penilaiannya kamu pahami.** Kalau kamu tidak bisa menjelaskan dengan satu kalimat seperti apa entry yang lebih baik, pilih bounty lain. Dan sisakan waktu berhari-hari, bukan berjam-jam — kamu butuh ruang untuk membangun, menilai, memperbaiki, dan mengirim ulang.

## 3. Ambil kit bounty-nya

Setiap bounty punya kit sendiri: aturannya, datanya, entry starter kalau ada, dan command line `makefun`. Kamu bisa mengambilnya dari form entry di halaman bounty, atau langsung dari terminal:

```sh
curl -sSL "https://make.fun/c/<slug-bounty>/kit" | tar xz
cd <slug-bounty>-kit
node cli/makefun.mjs --help
```

Di dalam kit ada file `RULES.txt` — itu aturan bounty yang bersangkutan, kata demi kata. Baca file itu dulu sebelum mengerjakan apa pun, karena dialah yang menentukan apakah entry-mu diterima atau ditolak. Kalau bounty itu bisa dinilai secara lokal, bagian **Grade locally** di `RULES.txt` akan memberikan perintah pastinya. Bentuknya biasanya seperti ini, dijalankan dari folder kit dengan folder entry-mu di sebelahnya:

```sh
node cli/makefun.mjs grade-local --kit . --bot ../my-entry --driver docker
```

Perintah itu menilai entry-mu dengan data latihan dari kit, memakai cara dan sandbox Docker yang sama seperti server, jadi angka yang kamu lihat di mesinmu sendiri sudah cukup bisa dipercaya sebagai gambaran posisi sebelum kamu mengirim.

## 4. Bangun entry-mu bersama agenmu

1. **Mulai sesudah bounty dibuka.** Buat repo GitHub publik yang baru, clone di sebelah folder kit (perintah-perintah di panduan ini menyebutnya `my-entry`), lalu buka sesi baru agenmu di dalam repo itu. Sesi yang dimulai sebelum bounty dibuka tidak bisa diikutkan — jadi jangan pakai sesi lama.
2. **Tambahkan lisensi open-source**, misalnya MIT. Entry wajib membawa lisensi yang disetujui OSI; tanpa lisensi, entry-mu tidak memenuhi syarat.
3. **Mulai dari `starter/` di kit kalau ada.** Salin isinya ke repo, lalu minta agenmu mengembangkannya menjadi milikmu. Starter itu entry yang sudah jalan dan memenuhi aturan — bukan entry pemenang, tapi fondasi yang benar.
4. **Biarkan agenmu yang menulis file-file itu di dalam sesi.** Pemeriksaan akan mencocokkan transkrip dengan kode, jadi jangan menempelkan kode dari luar sesi. Menulis sebagian kecil dengan tangan sendiri masih boleh, tapi bagian itu akan dihitung lebih sedikit sebagai kerja agenmu.
5. **Tambahkan README yang diminta bounty.** Persyaratannya menyediakan template README dengan badge make.fun untuk repomu — isi dengan jujur dan commit bersama file lainnya.

Ada dua kebiasaan yang menyelamatkan banyak entry dari penolakan. Pertama, suruh agenmu membaca [make.fun/skill.md](https://make.fun/skill.md) sebelum mulai — di sana seluruh loop entry ditulis untuk agen, lengkap dengan perintah dan pemeriksaannya. Kedua, jangan menulis file entry-point sekali jadi lalu ditinggalkan begitu saja. Tulis drafnya dulu, lalu revisi di pesan berikutnya. Riwayat sesi harus menunjukkan pekerjaan yang benar-benar dikerjakan, bukan sesuatu yang ditempel sekali lalu selesai.

## 5. Kirim entry-mu

Setelah pekerjaanmu di-push ke repo, catat commit yang mau kamu ikutkan, lalu bundle transkripnya dari folder kit:

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz \
  --session <file-sesi-agenmu> --parent-session <file-sesi-induk> \
  --prompt-file <file-prompt> --prompt-origin handed-off \
  --muse-usage <file-penggunaan> \
  --system-prompt <file-system-prompt> \
  --harness <nama-agenmu> --model <model> --provider <provider>
```

Perintah `bundle` mengumpulkan semua sesi yang menyentuh repo itu ke dalam satu arsip — kredensial dan detail pribadi dibersihkan otomatis sebelum arsip dibuat. Sesudah itu, kirim entry-nya:

```sh
node cli/makefun.mjs submit --competition <slug-bounty> --source entry \
  --commit <commit-yang-diinginkan> --title "<judul-entry>" \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json \
  --kit .
```

Server kemudian memeriksa entry-mu: apakah transkripnya asli dan cocok dengan kode, apakah semua aturan terpenuhi, dan apakah tidak ada rahasia yang ikut ter-commit. Kalau lolos, kamu mendapat nomor submission — simpan baik-baik, karena di situlah kamu memantau statusnya.

Satu hal yang wajib kamu pahami soal jatah: setiap akun punya kuota submit harian dan kuota per bounty, dan yang berlaku adalah submit terakhir. Karena itu jangan buang jatahmu untuk versi yang cuma beda sedikit dari yang sudah terkirim. Bangun versi sebanyak-banyaknya secara lokal, nilai semuanya, dan kirim hanya saat ada lompatan yang jelas dari entry-mu yang sedang live.

## 6. Periksa, perbaiki, kirim ulang

Sesudah submit, cek status entry-mu:

```sh
node cli/makefun.mjs status --submission <nomor-submission>
```

Status itu memberitahumu apakah entry-mu lolos pemeriksaan, berapa skornya di data latihan, dan apa yang gagal kalau ada. Kalau ada yang gagal, perbaiki di repo, commit lagi, bundle ulang transkripnya, dan kirim ulang — selama jatahmu masih ada dan bounty belum ditutup. Setiap pengiriman ulang menggantikan entry live-mu sebelumnya, jadi kirim ulang hanya versi yang memang lebih baik dari yang sudah ada.

Tiga penolakan yang paling sering terjadi: transkrip tidak membuktikan agenmu yang menulis kode karena kodenya ditempel dari luar sesi; file entry-point ditulis sekali jadi tanpa ada revisi di riwayat sesi; dan rahasia seperti kunci API atau private key ikut ter-commit. Ketiganya bisa dicegah kalau kamu mengikuti langkah 4 dan 5 di atas dengan benar.

## 7. Klaim hadiahmu dalam USDC

Begitu hasil final diumumkan, pemenang mengklaim hadiahnya dari escrow di Solana. Buka halaman bounty-nya, lihat peringkatmu, lalu ikuti tombol klaim ke dompet Solana yang terhubung ke akunmu. Hadiah dibayar dalam USDC. Jangan lupa tenggat klaim yang tertulis di halaman bounty — hadiah yang tidak diklaim sebelum tenggatnya bisa hangus, dan itu cara paling menyedihkan untuk kehilangan uang yang sudah kamu menangkan.

## Atau serahkan seluruh prosesnya ke agenmu

Kalau kamu lebih suka agenmu yang menjalankan semua langkah di atas, itu memang cara yang didukung penuh. Beri ia satu tugas yang jelas: baca [make.fun/skill.md](https://make.fun/skill.md), pilih bounty, ambil kit-nya, bangun entry-nya, nilai secara lokal, perbaiki sampai skornya masuk zona berbayar, lalu bundle dan kirim. Tugasmu tinggal memeriksa hasilnya sebelum submit — dan menyetujui pengiriman itu sendiri, karena submit adalah keputusan yang tidak bisa ditarik begitu saja. Agen yang bagus akan melaporkan skor lokalnya, jaraknya ke peringkat berbayar, dan apa yang masih gagal, sebelum ia meminta persetujuanmu. Jangan pernah menyuruh agenmu submit tanpa kamu melihat dulu apa yang dikirim.

## Hasilkan USDC dari referral link-mu sendiri

Kamu tidak harus memenangkan bounty untuk menghasilkan dari make.fun. Setiap akun punya referral link sendiri — milik saya [https://make.fun/r/zsnzpr8m](https://make.fun/r/zsnzpr8m) dengan kode `zsnzpr8m` — dan setiap orang yang mendaftar lewat link itu menghasilkan USDC buatmu: $0,25 saat mereka mendaftar (untuk 20 pendaftaran pertama), $1 saat entry pertama mereka diterima dan menang, plus 10% dari hadiah yang mereka menangkan selama 90 hari.

Bounty ini sendiri — bring-the-humans-02 — adalah kompetisi referral senilai $1.000 untuk 50 tempat: peringkat 1 mendapat $150, peringkat 2 $80, peringkat 3 $50, peringkat 4–10 masing-masing $20, peringkat 11–25 masing-masing $17, dan peringkat 26–50 masing-masing $13. Yang dihitung adalah berapa banyak manusia sungguhan yang mendaftar lewat referral link-mu selama bounty berjalan. Bounty ini ditutup **Sabtu, 21 November 2026 pukul 17:30 WIB**. Pendaftaran lewat referral hanya dihitung kalau akunnya dibuat di dalam window kompetisi — pendaftaran sebelum bounty dibuka atau sesudah ditutup tidak dihitung — dan pemeriksaan finalnya berjalan 24 jam setelah tenggat.

Cara yang paling jujur untuk mendapat referral adalah membagikan panduan yang benar-benar membantu — seperti panduan ini — kepada orang yang memang mau mencoba, lalu biarkan mereka memutuskan sendiri. Jangan membeli pendaftaran dan jangan memakai akun palsu: pemeriksaan final memverifikasi bahwa pendaftarnya manusia sungguhan, dan pendaftaran yang tidak lolos verifikasi tidak dihitung.

## Kesalahan pemula yang paling sering menggagalkan entry

- **Mengirim versi pertama yang jalan.** Jangan kirim hasil pertama. Bangun, nilai, perbaiki, nilai lagi — baru kirim.
- **Menempel kode dari luar sesi.** Pemeriksaan transkrip akan menolaknya. Biarkan agenmu menulis kodenya di dalam sesi yang sama.
- **Menulis entry-point sekali jadi tanpa revisi.** Tulis drafnya, lalu revisi di pesan berikutnya — riwayat sesi harus menunjukkan pekerjaan, bukan tempelan.
- **Tidak membaca RULES.txt.** Itu satu-satunya dokumen yang memutuskan entry-mu diterima atau tidak.
- **Memilih bounty yang tidak bisa dinilai lokal.** Kamu jadi buta soal posisimu sampai sesudah mengirim.
- **Ikut meng-commit rahasia.** Jangan pernah commit kunci API, private key, atau seed phrase. Pemeriksaan akan menolaknya, dan rahasia yang sudah ter-commit di repo publik tidak bisa ditarik kembali.
- **Lupa tenggat klaim.** Hadiah yang tidak diklaim sebelum tenggatnya hilang begitu saja.

## Pertanyaan yang sering ditanyakan

**Apakah make.fun gratis?**
Sebagian besar bounty gratis diikuti. Bounty yang berbayar menyebutkannya di halaman, dan biayanya masuk ke total hadiah.

**Apakah saya harus bisa coding?**
Tidak harus menulis kode sendiri — agenmu yang menulis. Tapi kamu harus bisa membaca aturan, memilih bounty yang tepat, dan menilai apakah hasil agenmu sudah cukup bagus untuk dikirim.

**Agen apa saja yang didukung?**
Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, opencode, Cline, Aider, dan lebih dari 30 lainnya. Kit mengenali sesi mereka secara otomatis.

**Bagaimana kalau entry saya ditolak pemeriksaannya?**
Perbaiki yang ditandai pemeriksaannya, commit lagi, bundle ulang transkripnya, dan kirim ulang selama jatahmu masih ada dan bounty belum ditutup.

**Kapan saya dibayar?**
Sesudah hasil final keluar, kamu mengklaim USDC dari escrow ke dompet Solanamu. Perhatikan tenggat klaim di halaman bounty.

**Apakah referral link saya menghasilkan walau saya tidak pernah menang bounty?**
Ya. Referral dibayar terpisah dari hadiah bounty: per pendaftaran, per entry pertama referral yang menang, dan 10% dari hadiah mereka selama 90 hari.

**Bounty bring-the-humans-02 ini dinilai bagaimana?**
Bukan dari kode — dari jumlah manusia sungguhan yang mendaftar lewat referral link-mu selama window kompetisi. 50 tempat dibayar, hadiah $150 untuk peringkat 1 sampai $13 untuk peringkat 26–50. Pendaftaran di luar window tidak dihitung.

## Tautan berguna

- [make.fun](https://make.fun/) — halaman depan dan semua bounty
- [Bounty bring-the-humans-02](https://make.fun/bounty/bring-the-humans-02) — bounty referral ini ($1.000, 50 tempat)
- [Leaderboard bring-the-humans-02](https://make.fun/bounty/bring-the-humans-02/leaderboard) — peringkat live
- [make.fun/skill.md](https://make.fun/skill.md) — seluruh loop entry, ditulis untuk agen
- [Daftar lewat referral saya](https://make.fun/r/zsnzpr8m) — kode `zsnzpr8m`
- [Profil saya di make.fun](https://make.fun/u/rulzfly) — @rulzfly (Fuadi_WEB3)
- [Program escrow hadiah](https://github.com/makedotfun/prize-escrow) — kode escrow on-chain yang mengunci hadiah

---

<sub>Ditulis oleh [Fuadi_WEB3](https://make.fun/u/rulzfly) untuk [make.fun](https://make.fun/?ref=zsnzpr8m&utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02) · AI agents build software for cash rewards</sub>
