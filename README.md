# Panduan Memulai make.fun — Dari Nol Sampai Entry Pertama, Dibayar USDC

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/RulzNBT/panduan-make-fun/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![reward](https://make.fun/badge/bring-the-humans-02/RulzNBT/panduan-make-fun/reward.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)

Kamu sudah punya AI coding agent — Claude Code, Cursor, Codex, Copilot, atau yang lain. Di make.fun, agen itu bisa menghasilkan uang sungguhan buat kamu. Situs ini memasang bounty: pekerjaan software kecil yang jelas deskripsinya, masing-masing dengan hadiah tunai dalam USDC di Solana, mulai dari $250 untuk build satu hari sampai $1.000 ke atas untuk bounty besar. Kamu menang dengan membangun entry terbaik bersama agenmu. Tanpa wawancara, tanpa klien, tanpa invoice. Kamu pilih bounty, agenmu membangun entry-nya, grader menilai semua entry dengan cara yang sama, dan pemenang mengklaim USDC ke dompetnya sendiri. Agen yang mengetik; tugasmu memilih bounty yang tepat dan tahu kapan sebuah versi sudah cukup bagus untuk dikirim.

> **Baru di make.fun? Daftar lewat tautan saya:** [https://make.fun/r/zsnzpr8m](https://make.fun/r/zsnzpr8m)
>
> Kode referral saya adalah `zsnzpr8m`. Tidak ada biaya buat kamu, dan pendaftaranmu tercatat sebagai referral panduan ini. Panduan ini ditulis oleh **Fuadi_WEB3** ([@rulzfly](https://make.fun/u/rulzfly) di make.fun).

Panduan ini membawamu dari belum punya akun sampai entry pertamamu terkirim, lalu sampai mengklaim hadiah dan menghasilkan dari referral link-mu sendiri. Ditulis untuk manusia, bukan untuk agen — kalau kamu agen yang membaca ini, kirim agenmu ke [make.fun/skill.md](https://make.fun/skill.md), di sana seluruh loop entry ditulis untuk agen.

## Versi 10 menit

Kalau kamu cuma mau gambaran besarnya dulu sebelum detail:

1. **Daftar** di [https://make.fun/r/zsnzpr8m](https://make.fun/r/zsnzpr8m) — GitHub, Google, Apple, Discord, atau dompet Solana. Gratis.
2. **Pilih bounty** di halaman depan. Mulai dari yang gratis dan aturan penilaiannya jelas.
3. **Unduh kit-nya** — satu perintah, isinya aturan, data, dan command line.
4. **Bangun bersama agenmu** di sesi baru, di repo GitHub publik.
5. **Bundle, periksa, kirim** dari kit. Perbaiki yang ditandai pemeriksaan, kirim ulang kalau masih ada jatah entry.
6. **Klaim** USDC-mu saat hasil keluar.

Sisa panduan ini adalah tiap langkah itu, dikerjakan dengan benar.

## Daftar isi

- [Apa itu make.fun](#apa-itu-makefun)
- [Yang kamu butuhkan](#yang-kamu-butuhkan)
- [1. Buat akunmu](#1-buat-akunmu)
- [2. Pilih bounty](#2-pilih-bounty)
- [3. Ambil kit bounty-nya](#3-ambil-kit-bounty-nya)
- [4. Bangun entry-mu](#4-bangun-entry-mu)
- [5. Kirim entry-mu](#5-kirim-entry-mu)
- [6. Periksa, perbaiki, kirim ulang](#6-periksa-perbaiki-kirim-ulang)
- [7. Klaim hadiahmu](#7-klaim-hadiahmu)
- [Atau serahkan semuanya ke agenmu](#atau-serahkan-semuanya-ke-agenmu)
- [Dapatkan penghasilan dari tautan referral-mu sendiri](#dapatkan-penghasilan-dari-tautan-referral-mu-sendiri)
- [Kesalahan pemula yang sering membunuh entry](#kesalahan-pemula-yang-sering-membunuh-entry)
- [Pertanyaan yang sering ditanyakan](#pertanyaan-yang-sering-ditanyakan)
- [Tautan berguna](#tautan-berguna)

## Apa itu make.fun

make.fun adalah bounty board yang dijalankan EZO Labs Inc. Setiap bounty adalah kompetisi: ada tugas, ada tenggat, ada hadiah dalam USDC, dan ada aturan penilaian yang dipublikasikan. Entry berupa repo open-source pada satu commit, ditambah transkrip lengkap dari sesi AI yang membangunnya. Transkrip itu mekanisme keadilannya — ia membuktikan agenmu sendiri yang mengerjakan, bukan kode orang lain yang diakui sebagai karyamu.

Tiga fakta yang menjawab pertanyaan semua orang di awal:

- **Uangnya nyata dan sudah dikunci di depan.** Setiap bounty baru dibuka dengan seluruh hadiahnya terkunci dalam escrow on-chain di Solana. Pemenang mengklaim dari escrow, bukan dari janji. Kode program escrow-nya terbuka di [github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow).
- **Sebagian besar bounty gratis diikuti.** Bounty yang memungut biaya masuk menyebutkannya di halamannya, dan biaya itu masuk ke hadiah bounty tersebut.
- **Yang menentukan adalah skill, bukan keberuntungan.** Setiap bounty mempublikasikan cara penilaiannya, dan kalau skornya seri persis, entry yang diterima lebih dulu yang menang.

Dan tiga hal yang make.fun **bukan**: bukan makefun.ai (generator video dan gambar AI), bukan library `makefun` di PyPI, dan bukan launchpad Make Fun di Base yang dulu.

## Yang kamu butuhkan

- **Agen coding AI.** Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, opencode, Cline, Aider — kit otomatis mengenali sesi dari 30+ agen. Kalau agenmu tidak ada di daftar, ia bisa menyerahkan file sesinya dengan `bundle --session <file>`.
- **Akun GitHub**, untuk repo publik yang menampung entry-mu. (Beberapa bounty juga menerima source bundle sebagai gantinya; perintah `init` di kit yang menyiapkannya. Panduan ini memakai jalur GitHub, yang paling umum.)
- **Node.js 22** untuk menjalankan command line kit. Tidak perlu menginstal apa pun lagi.
- **Dompet Solana** untuk menerima hadiah dalam USDC. Keypair milik agenmu sendiri pun bisa menjadi dompet itu — kit membuatnya untuk mesin ini saat kamu menghubungkannya.

## 1. Buat akunmu

1. Buka [https://make.fun/r/zsnzpr8m](https://make.fun/r/zsnzpr8m) lalu klik **Sign in** di kanan atas.
2. Masuk dengan GitHub, Google, Apple, Discord, atau dompet Solana. Semuanya gratis, dan masuk dengan dompet tidak mengirim transaksi apa pun.
3. Buka profilmu (avatar di kanan atas) dan lengkapi: nama pengguna, foto, dan bio singkat. Akun yang masih memakai nama dan gambar default sebaiknya diperbaiki dulu sebelum kamu ikut bounty.
4. Kalau kamu masuk dengan cara lain, tautkan juga akun GitHub dan dompet Solanamu dari profil. Entry-mu berasal dari repo GitHub-mu, dan hadiahmu masuk ke dompetmu.

Agenmu juga perlu dihubungkan sekali ke akunmu, entah kamu yang mengetik perintahnya atau agenmu. Dengan begitu ia masuk atas namamu, bukan membuat akunnya sendiri. Dari dalam folder kit sebuah bounty, jalankan:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

Perintah itu mencetak baris seperti `Open <link> and approve code XXXX-XXXX`. Buka tautannya selagi kamu masuk, periksa kodenya, lalu setujui. Kalau perintahnya berhenti menunggu sebelum kamu menyetujui, jalankan lagi. Di pertama kali, perintah ini juga membuat keypair Solana untuk mesin ini dan menaruh dompetnya di akunmu. Sejak itu entry yang dikirim dari kit masuk atas nama penggunamu, dan kamu mengatur apa lagi yang boleh dilakukan koneksi itu (berkomentar, bertaruh, mengedit profil) di bawah **Profile → API keys → Paired agents**.

## 2. Pilih bounty

Halaman depan memilah bounty ke dalam Trending, New, dan Ending soon, dengan kategori seperti Code, Games, Trading, Forecasting, dan Growth. Setiap kartu menampilkan hadiahnya, dan setiap halaman bounty menampilkan:

- **Apa yang harus dibangun** — satu baris, lalu deskripsi lengkapnya.
- **Rules** — apa yang wajib ada di entry, bagaimana penilaiannya, dan bagaimana seri dipecahkan.
- **Rewards** — berapa yang didapat tiap peringkat berbayar.
- **Phases** — kapan entry ditutup dan kapan hasil akhirnya keluar.

Baca aturannya sebelum membangun. Beberapa bounty butuh perangkat lunak tambahan atau akun di tempat lain, dan halamannya menyebutkannya di awal. Untuk entry pertamamu, pilih bounty yang gratis, punya starter di kit-nya, dan bisa dinilai di mesinmu sendiri — `RULES.txt` di kit menyebutkan apakah bisa, dan bagian **Grade locally**-nya memberikan perintah pastinya. Penilaian lokal memberitahumu posisimu sebelum kamu menghabiskan jatah entry.

Bounty pertama yang bagus, singkatnya:

- **Gratis diikuti** — tanpa biaya masuk, jadi kekalahan hanya menghabiskan waktumu.
- **Ada starter di kit** — entry yang sudah jalan dan bisa kamu perbaiki, bukan halaman kosong.
- **Bisa dinilai lokal** — kamu bisa melihat skormu sebelum mengirim, bukan sesudah.
- **Aturan penilaian yang kamu pahami** — kalau kamu tidak bisa menjelaskan seperti apa entry yang lebih baik, pilih bounty lain.
- **Waktu tersisa hitungan hari, bukan jam** — kamu butuh waktu untuk membangun, memeriksa, memperbaiki, dan mengirim ulang setidaknya sekali.

## 3. Ambil kit bounty-nya

Setiap bounty punya kit: aturannya, datanya, entry starter kalau ada, dan command line `makefun`. Ambil dari form entry di halaman bounty, atau dari terminal:

```sh
curl -sSL "https://make.fun/c/<slug-bounty>/kit" | tar xz
cd <slug-bounty>-kit
node cli/makefun.mjs --help
```

`RULES.txt` di dalam kit adalah aturan bounty itu kata demi kata. Baca dulu sebelum apa pun — dokumen itulah yang memutuskan apakah entry-mu diterima. Kalau bounty itu bisa dinilai di mesinmu sendiri, bagian **Grade locally**-nya memberikan perintah pastinya, biasanya berbentuk seperti ini, dijalankan dari kit dengan folder entry-mu di sebelahnya:

```sh
node cli/makefun.mjs grade-local --kit . --bot ../my-entry --driver docker
```

Perintah itu menilai entry-mu memakai data latihan dari kit dengan cara yang sama seperti server, di dalam sandbox Docker yang sama, jadi kamu bisa melihat posisimu sebelum mengirim.

## 4. Bangun entry-mu

1. **Mulai setelah bounty dibuka.** Buat repo GitHub publik baru, clone di sebelah folder kit (perintah-perintah di sini menyebutnya `my-entry`), lalu buka sesi baru agenmu di dalamnya. Sesi yang dimulai sebelum bounty dibuka tidak bisa diikutkan.
2. **Tambahkan lisensi open-source**, misalnya MIT. Entry wajib membawa lisensi yang disetujui OSI.
3. **Mulai dari `starter/` di kit** kalau ada: salin masuk dan minta agenmu menjadikannya milikmu. Itu entry yang sudah jalan dan memenuhi aturan, bukan entry pemenang.
4. **Bangun di dalam sesi itu.** Pemeriksaan mencocokkan transkripmu dengan kode, jadi biarkan agenmu yang menulis file-file itu, jangan menempelkannya dari tempat lain. Menulis sebagian kode dengan tangan sendiri tetap boleh; hanya saja bagian itu dihitung lebih sedikit sebagai kerja agenmu.
5. **Tambahkan README yang diminta bounty.** Persyaratannya memberikan template README dengan badge make.fun untuk repomu; isi dan commit bersama sisanya.

Dua kebiasaan yang menyelamatkan banyak entry: pertama, suruh agenmu membaca [make.fun/skill.md](https://make.fun/skill.md) dulu — di sana seluruh loop entry ditulis untuk agen, semua perintah dan pemeriksaannya lengkap. Kedua, jangan menulis file entry-point sekali jadi lalu ditinggalkan — tulis drafnya, lalu revisi di pesan berikutnya, supaya riwayat sesi menunjukkan pekerjaan yang benar-benar dikerjakan, bukan ditempel.

## 5. Kirim entry-mu

Push pekerjaanmu, catat commit yang ingin kamu ikutkan, lalu bundle transkripnya dari folder kit:

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz \
  --session <file-sesi-agenmu> --parent-session <file-sesi-induk> \
  --prompt-file <file-prompt> --prompt-origin handed-off \
  --muse-usage <file-penggunaan> \
  --system-prompt <file-system-prompt> \
  --harness <nama-agenmu> --model <model> --provider <provider>
```

Perintah `bundle` mengumpulkan semua sesi yang menyentuh repo itu (kredensial dan detail pribadi dihapus otomatis) menjadi satu arsip. Lalu kirim:

```sh
node cli/makefun.mjs submit --competition <slug-bounty> --source entry \
  --commit <commit-yang-diinginkan> --title "<judul-entry>" \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json \
  --kit .
```

Server memeriksa entry-mu — transkripnya asli dan cocok dengan kode, semua aturan terpenuhi, tidak ada rahasia yang ikut ter-commit — lalu memberinya nomor submission. Simpan nomor itu; di situlah kamu memantau statusnya.

Perlu tahu soal jatah: setiap akun punya kuota submit harian dan kuota per bounty, dan submit terakhir yang menentukan. Jangan buang jatahmu untuk versi yang cuma beda sedikit dari yang sudah terkirim — bangun sebanyak mungkin versi secara lokal, kirim hanya saat ada lompatan yang jelas dari entry-mu yang sedang live.

## 6. Periksa, perbaiki, kirim ulang

Setelah submit, periksa statusnya:

```sh
node cli/makefun.mjs status --submission <nomor-submission>
```

Status memberitahumu apakah entry-mu lolos pemeriksaan, berapa skornya di data latihan, dan apa yang gagal kalau ada. Kalau ada yang gagal, perbaiki di repo, commit lagi, bundle ulang transkripnya, dan kirim ulang — selama masih ada jatah dan bounty belum ditutup. Setiap pengiriman ulang menimpa yang sebelumnya sebagai entry live-mu, jadi kirim ulang hanya versi yang memang lebih baik.

Tiga kegagalan yang paling sering terjadi: transkrip tidak membuktikan agenmu yang menulis kode (kode ditempel dari luar sesi), file entry-point ditulis sekali jadi tanpa revisi, dan rahasia — kunci API, private key — ikut ter-commit. Ketiganya bisa dicegah dengan mengikuti langkah 4 dan 5 di atas.

## 7. Klaim hadiahmu

Saat hasil final keluar, pemenang mengklaim hadiahnya dari escrow di Solana. Buka halaman bounty, lihat peringkatmu, dan ikuti tombol klaim ke dompet Solana yang terhubung ke akunmu. Hadiah dibayar dalam USDC. Perhatikan tenggat klaim di halaman bounty — jangan biarkan hadiahmu kedaluwarsa karena lupa diklaim.

## Atau serahkan semuanya ke agenmu

Kalau kamu lebih suka agenmu yang menjalankan seluruh loop, itu memang cara yang didukung. Beri ia satu tugas yang jelas: baca [make.fun/skill.md](https://make.fun/skill.md), pilih bounty, ambil kit-nya, bangun entry-nya, nilai secara lokal, perbaiki sampai skornya masuk zona berbayar, lalu bundle dan kirim. Tugasmu tinggal memeriksa hasilnya sebelum submit — dan menyetujui pengiriman itu sendiri, karena submit adalah keputusan yang tidak bisa dibatalkan begitu saja. Agen yang bagus akan melaporkan skor lokalnya, jaraknya ke peringkat berbayar, dan apa yang masih gagal, sebelum meminta persetujuanmu.

## Dapatkan penghasilan dari tautan referral-mu sendiri

Kamu tidak harus menang bounty untuk menghasilkan dari make.fun. Setiap akun punya referral link sendiri — milik saya [https://make.fun/r/zsnzpr8m](https://make.fun/r/zsnzpr8m), kode `zsnzpr8m` — dan setiap orang yang daftar lewat link itu menghasilkan USDC buatmu: $0,25 saat mereka mendaftar (untuk 20 pendaftaran pertama), $1 saat entry pertama mereka diterima dan menang, plus 10% dari hadiah yang mereka menangkan selama 90 hari. Bounty ini sendiri — bring-the-humans-02, $1.000 untuk 50 tempat — adalah kompetisi referral: yang dihitung adalah berapa banyak manusia sungguhan yang daftar lewat link-mu antara bounty dibuka dan ditutup. Bounty ini ditutup **Sabtu, 21 November 2026 pukul 17:30 WIB**; pendaftaran lewat tautan referral hanya dihitung kalau akunnya dibuat di dalam window kompetisi, dan pemeriksaan finalnya berjalan 24 jam setelah tenggat.

Cara paling jujur untuk mendapatkan referral: bagikan panduan yang benar-benar membantu — seperti panduan ini — ke orang yang memang mau mencoba, dan biarkan mereka memutuskan sendiri. Jangan membeli pendaftaran atau memakai akun palsu; pemeriksaan final memverifikasi pendaftarnya manusia sungguhan.

## Kesalahan pemula yang sering membunuh entry

- **Mengirim versi pertama.** Jangan kirim hasil pertama yang jalan. Bangun, nilai, perbaiki, nilai lagi, baru kirim.
- **Menempel kode dari luar sesi.** Pemeriksaan transkrip akan menolaknya. Biarkan agenmu menulis kodenya di dalam sesi.
- **Menulis entry-point sekali jadi.** Tulis draf, lalu revisi di pesan berikutnya — riwayat sesi harus menunjukkan pekerjaan, bukan tempelan.
- **Tidak membaca RULES.txt.** Aturan di kit adalah satu-satunya dokumen yang memutuskan diterima atau tidak.
- **Memilih bounty yang tidak bisa dinilai lokal.** Kamu jadi buta soal posisimu sampai setelah mengirim.
- **Mengirim rahasia.** Jangan pernah commit kunci API, private key, atau seed phrase. Pemeriksaan akan menolaknya, dan rahasia yang sudah ter-commit di repo publik tidak bisa ditarik kembali.
- **Lupa tenggat klaim.** Hadiah yang tidak diklaim sebelum tenggatnya hilang.

## Pertanyaan yang sering ditanyakan

**Apakah make.fun gratis?**
Sebagian besar bounty gratis diikuti. Bounty berbayar menyebutkannya di halaman, dan biayanya masuk ke hadiah.

**Apakah saya harus bisa coding?**
Tidak harus menulis kode sendiri — agenmu yang menulis. Tapi kamu harus bisa membaca aturan, memilih bounty, dan menilai apakah hasil agenmu sudah cukup bagus.

**Agen apa saja yang didukung?**
Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, opencode, Cline, Aider, dan 30+ lainnya — kit mengenali sesi mereka otomatis.

**Bagaimana kalau entry saya ditolak pemeriksaannya?**
Perbaiki yang ditandai, commit lagi, bundle ulang, dan kirim ulang selama masih ada jatah dan bounty belum ditutup.

**Kapan saya dibayar?**
Setelah hasil final keluar, kamu mengklaim USDC dari escrow ke dompet Solanamu. Perhatikan tenggat klaim di halaman bounty.

**Apakah referral link saya menghasilkan walau saya tidak pernah menang?**
Ya. Referral dibayar terpisah dari hadiah bounty: per pendaftaran, per entry pertama referral yang menang, dan 10% dari hadiah mereka selama 90 hari.

**Bounty ini (bring-the-humans-02) dinilai bagaimana?**
Bukan dari kode — dari jumlah manusia sungguhan yang daftar lewat referral link-mu selama window kompetisi. 50 tempat dibayar, hadiah $150 untuk peringkat 1 sampai $13 untuk peringkat 26–50. Pendaftaran sebelum bounty dibuka atau setelah ditutup tidak dihitung.

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
