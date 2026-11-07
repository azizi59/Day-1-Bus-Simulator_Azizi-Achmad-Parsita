# Day-1-Bus-Simulator_Azizi-Achmad-Parsita
Azizi Achmad Parsita

## GitHub Repository
Repository (repo) = tempat penyimpanan sebuah proyek di GitHub.
Bisa dianggap seperti folder proyek online, tetapi memiliki fitur khusus untuk pengembangan software.
Di dalam repository biasanya terdapat:
  - Source code
  - File konfigurasi
  - Dokumentasi (README.md)
  - Gambar atau aset proyek
  - File lainnya yang dibutuhkan proyek

## Fungsi Repository
- Menyimpan proyek secara online.
- Menyimpan riwayat perubahan kode menggunakan Git.
- Memungkinkan kita melihat perubahan yang dilakukan dari waktu ke waktu.
- Berkolaborasi dengan orang lain dalam satu proyek.
- Memudahkan backup kode agar tidak hanya tersimpan di komputer.
- Memungkinkan orang lain untuk melihat, menggunakan, atau berkontribusi pada proyek.
- Menjadi tempat utama untuk mengelola proyek menggunakan fitur GitHub seperti:
  - Branches → membuat versi/cabang pengembangan.
  - Commits → menyimpan perubahan kode.
  - Pull Requests → mengajukan perubahan untuk digabungkan.
  - Issues → mencatat bug, tugas, atau masalah.

## Bagian 1: Prompt Engineering

**Definisi:** cara merancang instruksi agar AI memberi jawaban yang tepat, relevan, dan layak digunakan. Prompt bisa berupa pertanyaan sederhana, kata kunci, instruksi rumit, atau potongan kode.

**Konteks adalah kunci.** Prompt "Create student task planner" terlalu umum. Prompt yang menjelaskan siapa penggunanya, fitur yang diinginkan, dan batasannya akan menghasilkan output yang jauh lebih sesuai.

**Struktur prompt yang baik:**
| Elemen | Fungsi | Contoh dari slide |
|---|---|---|
| Role | Peran AI | "You are helping me build a beginner-friendly student task planner" |
| Task | Tujuan | Buat task planner untuk mahasiswa tahun pertama |
| Context | Requirements dan constraints | Tampilkan daftar tugas, filter, gunakan HTML/CSS/vanilla JS, tanpa library tambahan |
| Format | Bentuk output | Kode lengkap per file, cara menjalankan, cara menguji |

Prompt contoh ditutup dengan instruksi: *jangan klaim aplikasi berfungsi sebelum perilakunya diverifikasi.*

**Taktik tambahan (sumber: Google Cloud):**
- Gunakan kata kerja aksi untuk menentukan tindakan
- Tentukan panjang dan format output
- Tentukan target audiens
- Sertakan fakta dan data yang relevan
- Referensikan dokumen atau sumber tertentu
- Definisikan istilah kunci

**Keuntungan prompt engineering:** performa model meningkat, bias dan respons ofensif berkurang, kontrol dan prediktabilitas naik, pengalaman pengguna lebih baik.

## Bagian 2: Git dan GitHub

**Git** adalah version control system (VCS) yang melacak siapa, kapan, dan apa yang diubah dalam file. Dibuat oleh Linus Torvalds tahun 2005. Sifatnya terdistribusi (DVCS) dan bekerja secara lokal.

**GitHub** adalah platform berbasis web untuk menyimpan repository Git secara online dan mendukung kolaborasi. (Alternatif lain di slide: Bitbucket dan GitLab.)

**Tiga area dalam Git workflow:**
1. **Working directory**: salinan satu versi proyek yang sedang dikerjakan di komputer
2. **Staging area (index)**: menampung perubahan yang akan masuk ke commit berikutnya
3. **Git directory (repository)**: menyimpan metadata dan object database proyek; inilah yang disalin saat `clone`

Alurnya: *checkout* dari repository ke working directory → *stage* perubahan → *commit* ke repository.

## Perintah Git Penting

| Perintah | Fungsi |
|---|---|
| `git init` | Memulai repo baru |
| `git clone "url"` | Mengambil repo dari GitHub |
| `git add .` / `git add -A` / `git add --all` | Memindahkan file ke staging area |
| `git commit -m 'message'` | Menyimpan perubahan ke repository |
| `git remote add <name> <url>` | Menghubungkan repo lokal ke remote |
| `git push origin main` | Mengirim branch ke remote |
| `git pull origin main` | Mengambil perubahan lalu merge ke branch saat ini |

Catatan: `git add *` hanya menambahkan file baru atau yang dimodifikasi, bukan yang dihapus. Slide juga memuat lelucon klasik: *"In case of fire: 1. git commit, 2. git push, 3. leave building."*

## Setup

**Git:**
1. Install Git sesuai perangkat
2. Cek dengan `git --version`
3. Atur identitas: `git config --global user.name "..."` dan `user.email "..."`
4. Cek konfigurasi: `git config --global --list`

**VS Code:** install, lalu buka Command Palette (Ctrl/Cmd+Shift+P), cari "Shell Command: Install 'code' command in PATH", dan cek dengan `code --version`.

**Koneksi SSH ke GitHub (contoh macOS):**
1. Buat key: `ssh-keygen -t ed25519 -C "email@domain.com"` (Enter untuk lokasi default, isi passphrase atau kosongkan)
2. Jalankan SSH agent: `eval "$(ssh-agent -s)"`
3. Edit `~/.ssh/config` dengan blok `Host github.com` (AddKeysToAgent, UseKeychain, IdentityFile)
4. Tambahkan key ke agent: `ssh-add --apple-use-keychain ~/.ssh/id_ed25519`
5. Salin public key (`pbcopy < ~/.ssh/id_ed25519.pub`), lalu tambahkan di GitHub → Settings → SSH and GPG keys → New SSH key
6. Verifikasi: `ssh -T git@github.com`. Jika berhasil, muncul pesan *"Hi username! You've successfully authenticated..."*

Penjelasan Ed25519 (Edwards-curve Digital Signature Algorithm): algoritma tanda tangan digital berbasis kurva eliptik Curve25519 (dibuat Daniel J. Bernstein, 2011) yang aman dan cepat.

**Checklist akhir:** `git --version`, `git config --global user.name/email`, `code --version`, `ssh -T git@github.com`.

## Praktik Hari Ini: Student Task Planner

Alur kerja yang dipraktikkan:
1. Install platform AI (Claude, Antigravity, ChatGPT)
2. Tulis prompt untuk membuat web/aplikasi
3. Tambahkan ke Git dengan `git init`
4. Commit dan push ke GitHub
5. Lakukan perubahan
6. Commit dan push lagi

## Pengetahuan Baru
- Tau cara menggunakan github
- Tau manfaat menggunakan github

## Pendapat Pribadi
Acara Day-1 cukup seru & materi ini bermanfaat sebagai modal menjadi developer yang bisa memanage pengembangan projek nya dengan baik.
