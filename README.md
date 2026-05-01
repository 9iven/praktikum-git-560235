# praktikum-git-560235

## Deskripsi Proyek
Proyek ini adalah tugas praktikum mata kuliah Pemrograman dan Pengembangan Web (PPW). Proyek ini berisi halaman profil sederhana menggunakan HTML dan CSS yang dikelola dengan *version control system* *Git* dan repositori *GitHub*. Tujuan utama proyek ini adalah menerapkan alur kerja *Git* yang terstruktur, seperti pembuatan *branch*, penyelesaian *merge conflict*, pembuatan *pull request*, dan manipulasi riwayat *commit* menggunakan *interactive rebase*.

## Dokumentasi Perintah Git
Berikut adalah daftar perintah *Git* yang digunakan selama praktikum beserta penjelasan fungsinya:

*   `git init` : Menginisialisasi *repository* *Git* baru di *folder* lokal agar perubahan *file* dapat dilacak.
*   `git clone [url]` : Mengunduh (menyalin) *repository* dari *server* *GitHub* ke komputer lokal.
*   `git add [nama-file]` atau `git add .` : Memasukkan perubahan *file* ke dalam *staging area* sebelum disimpan ke riwayat *commit*.
*   `git commit -m "[pesan]"` : Menyimpan perubahan secara permanen ke *repository* lokal beserta pesan yang mengikuti standar *Conventional Commits*.
*   `git push origin [nama-branch]` : Mengunggah *commit* dari komputer lokal ke *repository* *GitHub*.
*   `git pull origin [nama-branch]` : Mengambil *update* kode terbaru dari *GitHub* dan menggabungkannya ke *branch* lokal yang sedang aktif.
*   `git log --oneline --graph` : Menampilkan riwayat *commit* dan visualisasi *branch* secara ringkas dalam satu baris.
*   `git checkout -b [nama-branch]` : Membuat *branch* baru sekaligus langsung berpindah ke *branch* tersebut.
*   `git checkout [nama-branch]` : Berpindah ke *branch* lain yang sudah ada.
*   `git merge [nama-branch]` : Menggabungkan *branch* lain ke dalam *branch* yang sedang aktif.
*   `git rebase -i HEAD~3` : Melakukan *interactive rebase* untuk menyatukan (*squash*) tiga *commit* terakhir menjadi satu *commit* agar riwayat lebih rapi.

## Lampiran Dokumentasi Proses Praktikum

Berikut adalah dokumentasi proses penyelesaian *issue*, pembuatan *pull request*, penyelesaian *conflict*, dan pengelolaan *repository* selama praktikum:

---

### 1. Tugas 1: Inisialisasi & Commit History

<br>

![Log Git](dokumentasi_gambar/gitlog.png)

<br>

*Tangkapan layar riwayat commit lokal menggunakan perintah `git log --oneline --graph` untuk melihat alur branch dan commit secara ringkas.*

<br>
---

### 2. Tugas 2 dan 4 (Issues): Branching, Pull Request, dan Issue

<br>

![Integrasi Issue dan PR](dokumentasi_gambar/gabungintugas4ISSUEdan2PR.png)

<br>

*Tampilan GitHub yang menunjukkan bahwa ada 3 issue (untuk tugas 4) juga dibuat sesuai PR tugas 2 agar nanti otomatis tertutup (closed) setelah pull request di-merge.*

<br>

![Compare dan PR](dokumentasi_gambar/comparedanPR.png)

<br>

*Tampilan saat membuat pull request untuk membandingkan kode dari branch fitur ke branch utama.*

<br>


![3 Pull Requests](dokumentasi_gambar/3PULLREQUESTS.png)

<br>

*Daftar tiga pull request yang berhasil dibuat dari masing-masing branch (feature/navbar, feature/footer, dan hotfix/typo).*

<br>

![Menutup Issue](dokumentasi_gambar/sekaligusmenutupISSUE.png)

<br>

*Penggunaan format "Closes #1" pada deskripsi pull request untuk menutup issue secara otomatis. Sekaligus mengerjakan tugas 4.*

<br>

![Squash and Merge](dokumentasi_gambar/squashnmergeutkFEAT.png)

<br>

*Pemilihan opsi Squash and merge untuk menggabungkan branch fitur agar riwayat commit di main tetap bersih.*

<br>

![Hapus Branch](dokumentasi_gambar/branchdelet.png)

<br>

*Proses penghapusan branch dari GitHub setelah pull request selesai di-merge.*

<br>

![Pull Setelah Tugas 2](dokumentasi_gambar/setelahtugas2jgnlupaPULLbiarupdate.png)

<br>

*Proses `git pull origin main` di terminal lokal untuk mengambil update terbaru dari GitHub sebelum lanjut ke tugas berikutnya.*

<br>

![Branch Protection](dokumentasi_gambar/branchprotection.png)

<br>

*Pengaturan Branch Protection Rule di GitHub agar branch utama wajib melalui pull request sebelum di-merge.*

<br>
---

### 3. Tugas 3: Konflik & Rebase

<br>

![Eksperimen Branch A dan B](dokumentasi_gambar/experimenAB.png)

<br>

*Proses pembuatan branch experiment/color-A dan experiment/color-B untuk menyiapkan simulasi merge conflict.*

<br>

![Bypass Rule](dokumentasi_gambar/bypassAB.png)

<br>

*Penggunaan opsi bypass di GitHub untuk melakukan merge pada branch eksperimen pertama tanpa harus menunggu ulasan.*

<br>

![Konflik A dan B](dokumentasi_gambar/conflictAB.png)

<br>

*Pesan error di terminal yang menunjukkan terjadinya merge conflict pada file style.css.*

<br>

![Resolve Manual di VS Code](dokumentasi_gambar/manualconflictresolveVSC.png)

<br>

*Proses penyelesaian konflik secara manual di VS Code dengan memilih kode yang benar dan menghapus batas konflik (<<<<<<<, =======, >>>>>>>).*

<br>

![Push Setelah Fix](dokumentasi_gambar/setelahfixABmakaPUSH.png)

<br>

*Perintah git commit dan git push untuk menyimpan hasil perbaikan konflik ke GitHub.*

<br>

![Log Rebase (3 to 1)](dokumentasi_gambar/gitlog3rebaseto1.png)

<br>

*Tiga commit terpisah di branch feature/dark-mode sebelum dilakukan rebase.*

<br>

![Editor Rebase 2](dokumentasi_gambar/rebaseedit1.png)

<br>

*Tampilan editor saat proses interactive rebase untuk mengubah perintah `pick` menjadi `squash`.*

<br>

![Editor Rebase 1](dokumentasi_gambar/rebaseedit2.png)

<br>

*Tampilan editor untuk menggabungkan pesan commit menjadi satu pesan akhir yang lebih rapi.*

<br>

![Log Hasil Rebase](dokumentasi_gambar/rebase.png)

<br>

*Hasil akhir riwayat commit setelah rebase, di mana tiga commit berhasil digabung menjadi satu.*

<br>
---

### 3. Tugas 4: Dokumentasi, Invite, dan Release

<br>

*README.md sesuai yang ada disini. Dosen dan Asisten sudah terinvite. Tahap release v1.0.0 di GitHub mengikuti Releases → Draft new release → buat tag v1.0.0 → isi changelog → Publish release.*

