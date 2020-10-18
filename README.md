# Latihan 1

# PENGGUNAAN GIT 

### APA ITU GIT ?
* Git adalah salah satu sistem pengontrol versi (Version ControlSystem) pada proyek perangkat lunak yang diciptakan oleh Linus Torvalds.
* Pengontrol versi bertugas mencatat setiap perubahan pada fileproyek yang dikerjakan oleh banyak orang maupun sendiri.
* Git dikenal juga dengan distributed revision control (VCS terdistribusi),artinya penyimpanan database Git tidak hanya berada dalam satutempat saja.


### INSTALASI GIT
* Download Git, buka website resminya Git `(git-scm.com)`.
* Kemudian unduh Git sesuai dengan arsitektur komputer kita. Kalau menggunakan 64bit, unduh yang 64bit. Begitu juga kalau menggunakan 32bit.
* Selamat, Git sudah terinstal di Windows. Untuk mencobanya,silahkan buka CMD atau PowerShell, kemudian ketik perintah

``git --version``

![Anotasi 2020-10-18 131620](https://user-images.githubusercontent.com/72904723/96360755-04c1e480-114a-11eb-8e1a-2e259ae5f836.png)

Menambahkan Global Config
Pada saat pertama kali menggunakan git, perlu dilakukan konfigurasi user.name dan user.email

konfigurasi ini bisa dilakukan untuk global repostiry atau individual repository.

apabila belum dilakukan konfigurasi, akan mengakibatkan terjadi kegagalan saat menjalankan perintah git commit

Config Global Repository

$ git config --global user.name “nama_user"

$ git config --global user.email “nama_user”

![Anotasi 2020-10-18 132356](https://user-images.githubusercontent.com/72904723/96360854-f7f1c080-114a-11eb-856a-fcadabe70f4f.png)

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
![Anotasi 2020-10-18 132621](https://user-images.githubusercontent.com/72904723/96360998-20c68580-114c-11eb-99cd-47449836ee37.png)
* Sehingga terbentuk satu direktori baru dibawahnya, selanjutnya masuk kedalam direktori tersebut dengan perintah cd ``(change directory)``
* direktory aktif menjadi: **d:\labs_pemrograman1\latihan1

### Membuat Reposiory Local

* Jalankan perintah git init, untuk membuat repository local.
`$ git init`
![Anotasi 2020-10-18 132716](https://user-images.githubusercontent.com/72904723/96361201-0392b680-114e-11eb-8566-6dac0b756bd4.png)
* Repository baru berhasil di inisialisasi, dengan terbentuknya satu direktori hidden dengan nama .git
* Pada direktori tersebut, semua perubahan pada `working directory` akan disimpan.

### Menambahkan File baru pada repository

* Untuk membuat file dapat menggunakan text editor, lalu menyimpan filenya pada direktori aktif (repository)
* disini kita akan coba buat satu file bernama README.md (text file)
`$ echo “# Latihan 1” >> README.md`
* File README.md berhasil dibuat.

![Anotasi 2020-10-18 132913](https://user-images.githubusercontent.com/72904723/96361327-f924ec80-114e-11eb-81cd-d51e5ffa25bb.png)

### Menambahkan File baru pada repository

* Untuk menambahkan file yang baru saja dibuat tersebut gunakan perintah git add.
`$ git add README.md`
* File README.md berhasil ditambahkan.

![Anotasi 2020-10-18 133225](https://user-images.githubusercontent.com/72904723/96361427-b9aad000-114f-11eb-9ae2-af615bd9a7cb.png)

### `Commit` (Menyimpan perubahan ke database)

* Untuk menyimpan perubahan yang ada kedalam database repository local, gunakan perintah git commit -m “komentar commit”
`$ git commit -m “File pertama saya”`
* Perubahan berhasil disimpan.

![Anotasi 2020-10-18 133316](https://user-images.githubusercontent.com/72904723/96361474-3047cd80-1150-11eb-8ba1-af05cc05582d.png)

### Membuat repository server

* Server reopsitory yang akan kita gunakan adalah (http://github.com)
* Anda harus membuat akun terlebih dahulu.
* Pada laman github, klik tombol start a project, atau
* Dari menu (icon +) klik New Repository

![Anotasi 2020-10-18 131212](https://user-images.githubusercontent.com/72904723/96361506-83ba1b80-1150-11eb-96b4-664dff3c5965.png)

### Membuat repository server

* Isi nama repositorynya, misal: labpy1.
* lalu klik tombol Create repository

![Anotasi 2020-10-18 132001](https://user-images.githubusercontent.com/72904723/96361571-15298d80-1151-11eb-8d0a-66f24227dc89.png)

### Menambahkan Remote Repository

* Remote Repository merupakan repository server yang akan digunakan untuk menyimpan setiap perubahan pada local repository, sehingga dapat diakses oleh banyak user.
* Untuk menambahkan remote repository server, gunakan perintah git remote add origin [url]
`$ git remote add origin https://github.com/noval1802/LatihanVCS.git`

![Anotasi 2020-10-18 133456](https://user-images.githubusercontent.com/72904723/96361709-2757fb80-1152-11eb-98da-43c7ef81ff0e.png)

### Push (Mengirim perubahan ke server)

* Untuk mengirim perubahan pada local repository ke server gunakan perintah git push.
`$ git push -u origin master`
* Perintah ini akan meminta memasukkan username dan password pada akun github.com

![Anotasi 2020-10-18 133721](https://user-images.githubusercontent.com/72904723/96361735-638b5c00-1152-11eb-9c36-c9c8cbba689a.png)

### Melihat hasilnya pada server repository

* Buka laman github.com, arahkan pada repositorinya.
* Maka perubahan akan terlihat pada laman tersebut.

![Anotasi 2020-10-18 150436](https://user-images.githubusercontent.com/72904723/96361833-53c04780-1153-11eb-85c0-092087bab155.png)

### Clone Repository

* Clone repository, pada dasarnya adalah meng-copy repository server dan secara otomatis membuat satu direktory sesuai dengan nama repositorynya (working directory).
* Untuk melakukan cloning, gunakan perintah `git clone [url]`

![Anotasi 2020-10-18 134736](https://user-images.githubusercontent.com/72904723/96361881-95e98900-1153-11eb-9962-a56768376dd3.png)

### Kegunaan file README.md

* Apabila kita menggunakan github, untuk memberikan penjelasan awal pada project yang kita buat, maka dapat menggunakan sebuah file yang bernama README.md
* Pada file tersebut kita dapat membuat dokumentasi awal dari setiap project yang kita buat untuk memberikan penjelasan atau sekedar cara penggunaan dari aplikasi yang kita kembangkan.
* Penulisan file README.md berbasis teks, dan untuk pemformatannya menggunakan Markdown format.
* untuk lebih jelasnya, dapat anda pelajari cara penggunaan markdown pada url berikut: https://guides.github.com/features/masteringmarkdown/
