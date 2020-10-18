# latihan1
#   # PENGGUNAAN GIT 


### APA ITU GIT 
* Git adalah salah satu sistem pengontrol versi (Version ControlSystem) pada proyek perangkat lunak yang diciptakan oleh Linus Torvalds.
* Pengontrol versi bertugas mencatat setiap perubahan pada fileproyek yang dikerjakan oleh banyak orang maupun sendiri.
* Git dikenal juga dengan distributed revision control (VCS terdistribusi),artinya penyimpanan database Git tidak hanya berada dalam satutempat saja.


### INSTALASI GI
* Download Git, buka website resminya Git `(git-scm.com)`.
* Kemudian unduh Git sesuai dengan arsitektur komputer kita. Kalau menggunakan 64bit, unduh yang 64bit. Begitu juga kalau menggunakan 32bit.
* Selamat, Git sudah terinstal di Windows. Untuk mencobanya,silahkan buka CMD atau PowerShell, kemudian ketik perintah

``git --version``

![Screenshot 2020-10-18 141255](https://user-images.githubusercontent.com/72906441/96361435-d810cb80-114f-11eb-947a-060390174a7a.png)


### Menambahkan Global Config
* Pada saat pertama kali menggunakan git, perlu dilakukan konfigurasi ``user.name dan user.email``
* konfigurasi ini bisa dilakukan untuk global repostiry atau individual repository.

* apabila belum dilakukan konfigurasi, akan mengakibatkan terjadi kegagalan saat menjalankan perintah `git commit`

* Config Global Repository

`$ git config --global user.name “nama_user"`

`$ git config --global user.email “nama_user”`

![Screenshot 2020-10-18 004340](https://user-images.githubusercontent.com/72905634/96363727-ccd78480-10ea-11eb-8252-72338449b025.png)


### Perintah Dasar Git

* `git init`, perintah untuk membuat repository local
* `git add`, perintah untuk menambahkan file baru, atau perubahan pada file pada staging sebelum proses commit.
* `git commit`, perintah untuk menyimpan perubahan kedalam database git.
* `git push -u origin master`, perintah untuk mengirim perubahan pada repository local menuju server repository.
* `git clone [url]`, perintah untuk membuat working directory yang diambil dari repositry sever.
* `git remote add origin [url]`, perintah untuk menambahkan remote server/reopsitory server pada local repositry ``(working directory)``
* `git pull`, perintah untuk mengambil/mendownload perubahan terbaru dari server repository ke local repository


### Membuat Reposiory Local

* Buka direktory aktif, misal: d:\labs_pemrograman1 (buka menggunakan Windows Explorer)
* klik kanan pada direktory aktif tersebut, dan pilih menu Git Bash, sehingga muncul git bash commad
* Buat direktory project praktikum pertama dengan nama latihan1
``$ mkdir latihan1
$ cd latihan1``
* Sehingga terbentuk satu direktori baru dibawahnya, selanjutnya masuk kedalam direktori tersebut dengan perintah cd ``(change directory)``
* direktory aktif menjadi: **d:\labs_pemrograman1\latihan1


![Screenshot 2020-10-18 145520](https://user-images.githubusercontent.com/72906441/96361989-55d6d600-1154-11eb-97fa-c1ef65d1d057.png)

### Membuat Reposiory Local

* Jalankan perintah git init, untuk membuat repository local.
`$ git init`
* Repository baru berhasil di inisialisasi, dengan terbentuknya satu direktori hidden dengan nama .git
* Pada direktori tersebut, semua perubahan pada `working directory` akan disimpan.


![Screenshot 2020-10-18 145554](https://user-images.githubusercontent.com/72906441/96362066-e8777500-1154-11eb-9759-c5ea58aae306.png)

### Menambahkan File baru pada repository

* Untuk membuat file dapat menggunakan text editor, lalu menyimpan filenya pada direktori aktif (repository)
* disini kita akan coba buat satu file bernama README.md (text file)
`$ echo “# Latihan 1” >> README.md`
* File README.md berhasil dibuat.


![Screenshot 2020-10-18 145705](https://user-images.githubusercontent.com/72906441/96362129-56bc3780-1155-11eb-9fdb-5e4774f8f7be.png)


### Menambahkan File baru pada repository

* Untuk menambahkan file yang baru saja dibuat tersebut gunakan perintah git add.
`$ git add README.md`
* File README.md berhasil ditambahkan.


![Screenshot 2020-10-18 145747](https://user-images.githubusercontent.com/72906441/96362233-05f90e80-1156-11eb-99e1-f34d491360f0.png)


### `Commit` (Menyimpan perubahan ke database)

* Untuk menyimpan perubahan yang ada kedalam database repository local, gunakan perintah git commit -m “komentar commit”
`$ git commit -m “File pertama saya”`
* Perubahan berhasil disimpan.


![Screenshot 2020-10-18 145817](https://user-images.githubusercontent.com/72906441/96362265-56706c00-1156-11eb-9278-51c528868fb1.png)


### Membuat repository server

* Server reopsitory yang akan kita gunakan adalah (http://github.com)
* Anda harus membuat akun terlebih dahulu.
* Pada laman github, klik tombol start a project, atau
* Dari menu (icon +) klik New Repository

![Screenshot 2020-10-18 004854](https://user-images.githubusercontent.com/72905634/96363882-c4cc1480-10eb-11eb-88ce-fb454e078bf7.png)

### Membuat repository server

* Isi nama repositorynya, misal: labpy1.
* lalu klik tombol Create repository

![Screenshot 2020-10-18 004939](https://user-images.githubusercontent.com/72905634/96363897-e3321000-10eb-11eb-884b-5615fa1e8f14.png)

### Menambahkan Remote Repository

* Remote Repository merupakan repository server yang akan digunakan untuk menyimpan setiap perubahan pada local repository, sehingga dapat diakses oleh banyak user.
* Untuk menambahkan remote repository server, gunakan perintah git remote add origin [url]
`$ git remote add origin https://github.com/Taufikrauf/latihan1.git`

![Screenshot 2020-10-18 005624](https://user-images.githubusercontent.com/72905634/96363933-4c198800-10ec-11eb-85e5-4b4fca4daa08.png)

### Push (Mengirim perubahan ke server)

* Untuk mengirim perubahan pada local repository ke server gunakan perintah git push.
`$ git push -u origin master
* Perintah ini akan meminta memasukkan username dan password pada akun github.com


![Screenshot 2020-10-18 150334](https://user-images.githubusercontent.com/72906441/96362962-69d20600-115b-11eb-877a-787b8146a4c6.png)


### Melihat hasilnya pada server repository

* Buka laman github.com, arahkan pada repositorinya.
* Maka perubahan akan terlihat pada laman tersebut.


![Screenshot 2020-10-18 154320](https://user-images.githubusercontent.com/72906441/96363127-7571fc80-115c-11eb-96dd-1112d4797d36.png)


### Clone Repository

* Clone repository, pada dasarnya adalah meng-copy repository server dan secara otomatis membuat satu direktory sesuai dengan nama repositorynya (working directory).
* Untuk melakukan cloning, gunakan perintah `git clone [url]`


![Screenshot 2020-10-18 161507](https://user-images.githubusercontent.com/72906441/96363266-60e23400-115d-11eb-895f-0e0aa1da5406.png)


### Kegunaan file README.md

* Apabila kita menggunakan github, untuk memberikan penjelasan awal pada project yang kita buat, maka dapat menggunakan sebuah file yang bernama README.md
* Pada file tersebut kita dapat membuat dokumentasi awal dari setiap project yang kita buat untuk memberikan penjelasan atau sekedar cara penggunaan dari aplikasi yang kita kembangkan.
* Penulisan file README.md berbasis teks, dan untuk pemformatannya menggunakan Markdown format.
* untuk lebih jelasnya, dapat anda pelajari cara penggunaan markdown pada url berikut: https://guides.github.com/features/masteringmarkdown/
