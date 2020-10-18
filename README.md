# PENGGUNAAN GIT

## Pengertian Git
* Git adalah salah satu sistem pengontrol versi(Version Control System) pada proyek perangkat lunak yang diciptakan oleh Linus Torvalds.
* Fungsi utama git yaitu mengatur versi dari source code program, dengan memberi tanda baris dan code mana yang ditambah atau diganti.
* Git juga dikenal dengan distributed revision control (VCS terdistribusi), artinya penyimpanan database Git tidak hanya berada dalam satu tempat saja.

## Instalasi Git
* Download **Git** di website resminnya [git-scm.com](https://git-scm.com).
* Kemudian unduh Git sesuai dengan arsitektur komputer kita. Apakah 64 bit atau 32 bit.
<a data-flickr-embed="true" href="https://www.flickr.com/photos/190675444@N02/50501615856/in/dateposted-public/" title="1gitdownload"><img src="https://live.staticflickr.com/65535/50501615856_375194704e.jpg" width="500" height="243" alt="1gitdownload"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>
* Untuk pengguna linux ``sudo apt-get install git`` & untuk Mac ``brew install git``

* Jika Git sudah terpasang, untuk mencobanya silahkan buka **Terminal** atau **CMD**, kemudian ketik perintah ``git --version.``

  <a data-flickr-embed="true" href="https://www.flickr.com/photos/190675444@N02/50501773597/in/dateposted-public/" title="2gitversi"><img src="https://live.staticflickr.com/65535/50501773597_6bd3cb4024.jpg" width="500" height="251" alt="2gitversi"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>


## Menambahkan Global Config
* Pada saat pertama kali menggunakan git, perlu dilakukan konfigurasi
user.name dan user.email agar tidak terjadi kegagalan saat menjalankan perintah ```git commit```
* konfigurasi ini bisa dilakukan untuk global repository atau individual
repository.
* Untuk Config Global Repository adalah

  ``$ git config --global user.name "nama_user"``

  ``$ git config --global user.email "email_user"``

  <a data-flickr-embed="true" href="https://www.flickr.com/photos/190675444@N02/50501776877/in/dateposted-public/" title="3gitakun"><img src="https://live.staticflickr.com/65535/50501776877_255ee214c9.jpg" width="500" height="251" alt="3gitakun"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

* Hasilnya dapat kita lihat dengan mengetik ``$ git config --list``

  <a data-flickr-embed="true" href="https://www.flickr.com/photos/190675444@N02/50501619646/in/album-72157716514998656/" title="4gitconfig"><img src="https://live.staticflickr.com/65535/50501619646_32d3491c43.jpg" width="500" height="251" alt="4gitconfig"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>


## Membuat Repositori Lokal
* Buka termninal atau CMD, disini saya menggunakan CMD.
* Buat directory baru dengan nama belajargit

  ``$ mkdir belajargit``

* Sehingga terbentuk satu direktori baru dibawahnya, selanjutnya masuk kedalam direktori tersebut dengan perintah cd (change directory)

  ``$ cd belajargit``

* directory aktif menjadi: ``C:\Users\Ilham\belajargit``

  <a data-flickr-embed="true" href="https://www.flickr.com/photos/190675444@N02/50500909043/in/album-72157716514998656/" title="8mkdir"><img src="https://live.staticflickr.com/65535/50500909043_e3902522cf.jpg" width="500" height="251" alt="8mkdir"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

* Jalankan perintah git init, untuk membuat repository local.

  ``$ git init``

  <a data-flickr-embed="true" href="https://www.flickr.com/photos/190675444@N02/50501777657/in/album-72157716514998656/" title="9gitinit"><img src="https://live.staticflickr.com/65535/50501777657_2175cf11d0.jpg" width="500" height="248" alt="9gitinit"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>
* Repository baru berhasil di inisialisasi, dengan terbentuknya satu direktori hidden dengan nama .git (perhatikan tulisan yang berwarna kuning).
* Pada direktori tersebut, semua perubahan pada working directory akan disimpan.

## Membuat File baru pada repositori
* Untuk membuat file dapat menggunakan text editor apa saja, lalu menyimpan filenya pada direktori aktif (repository).
* disini kita coba membuat satu file bernama README.md

  ``$ echo “Ini adalah file pertamaku” >> README.md``

  <a data-flickr-embed="true" href="https://www.flickr.com/photos/190675444@N02/50501777872/in/album-72157716514998656/" title="11readme"><img src="https://live.staticflickr.com/65535/50501777872_c92f5a8675.jpg" width="500" height="253" alt="11readme"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

* File README.md berhasil dibuat. Untuk mengeceknya, pengguna windows dapat mengetik ``dir``, sedangkan pengguna linux cukup mengetik ``ls``

  <a data-flickr-embed="true" href="https://www.flickr.com/photos/190675444@N02/50501621066/in/album-72157716514998656/" title="12dir"><img src="https://live.staticflickr.com/65535/50501621066_8c30f7b8d2.jpg" width="500" height="250" alt="12dir"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>


## Menambahkan File baru pada repositori
* Untuk menambahkan file yang sebelumnya baru saja dibuat, gunakan perintah git add.

  ``$ git add README.md``

* File README.md berhasil ditambahkan.
* Untuk mengeceknya bisa menggunakan ``git status``, maka tulisan berubah menjadi warna hijau.
  <a data-flickr-embed="true" href="https://www.flickr.com/photos/190675444@N02/50501778562/in/album-72157716514998656/" title="13add"><img src="https://live.staticflickr.com/65535/50501778562_cf1524a818.jpg" width="500" height="254" alt="13add"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

## Menyimpan perubahan ke database
* Untuk menyimpan perubahan yang ada kedalam database repositori lokal, gunakan perintah

  ``$ git commit -m 'Commit Pertama'``

* Perubahan berhasil disimpan.
* Cek kembali menggunakan ``git status``, maka output akan menampilkan "Nothing to commit .."

  <a data-flickr-embed="true" href="https://www.flickr.com/photos/190675444@N02/50501621371/in/album-72157716514998656/" title="14.2commit"><img src="https://live.staticflickr.com/65535/50501621371_77a381fd59.jpg" width="500" height="253" alt="14.2commit"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>


## Melihat catatan log
* Gunakan perintah ``git log`` untuk melihat perubahan catatan log pada repositori.

  <a data-flickr-embed="true" href="https://www.flickr.com/photos/190675444@N02/50501778832/in/album-72157716514998656/" title="15log"><img src="https://live.staticflickr.com/65535/50501778832_b5908a05b1.jpg" width="500" height="251" alt="15log"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>


## Membuat repositori server
* Server repositori yang akan kita gunakan adalah http://github.com, sebelum itu kita harus membuat akun terlebih dahulu.
* Pada halaman github, klik tombol start a project, atau
* Dari menu (icon +) klik New Repository.

  <a data-flickr-embed="true" href="https://www.flickr.com/photos/190675444@N02/50501621931/in/album-72157716514998656/" title="16repo"><img src="https://live.staticflickr.com/65535/50501621931_c1d0c7cb6b_w.jpg" width="400" height="217" alt="16repo"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>


## Membuat repositori server
* Isi nama repository nya, misalnya: Repo-Pertamaku
* lalu klik tombol Create repository

  <a data-flickr-embed="true" href="https://www.flickr.com/photos/190675444@N02/50501779487/in/album-72157716514998656/" title="17create"><img src="https://live.staticflickr.com/65535/50501779487_e0a22e71bc_w.jpg" width="400" height="329" alt="17create"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>


## Menambahkan Remote Repositori
* Remote Repository merupakan repositori server yang akan digunakan untuk menyimpan setiap perubahan pada repositori lokal, sehingga dapat diakses oleh banyak pengguna.
* Untuk menambahkan remote repository server, gunakan perintah

  ``$ git remote add origin https://github.com/IlhamLamp/Repo-Pertamaku.git``

  <a data-flickr-embed="true" href="https://www.flickr.com/photos/190675444@N02/50500911633/in/album-72157716514998656/" title="19"><img src="https://live.staticflickr.com/65535/50500911633_b939f89a9c_w.jpg" width="400" height="135" alt="19"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>


## Mengirim perubahan ke server
* Untuk mengirim perubahan pada repositori lokal ke server gunakan perintah git push.

  ``$ git push -u origin master``

* Perintah ini akan meminta memasukkan username dan password pada akun github.com

  <a data-flickr-embed="true" href="https://www.flickr.com/photos/190675444@N02/50500911763/in/album-72157716514998656/" title="20"><img src="https://live.staticflickr.com/65535/50500911763_060e3d7010_w.jpg" width="400" height="291" alt="20"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

* (Setelah memasukkan username dan password)

  <a data-flickr-embed="true" href="https://www.flickr.com/photos/190675444@N02/50501623181/in/album-72157716514998656/" title="21"><img src="https://live.staticflickr.com/65535/50501623181_b6e359face_w.jpg" width="400" height="166" alt="21"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>


## Melihat hasilnya pada server repository
* Buka laman github.com, arahkan ke **Repo-Pertamaku**.
* Maka perubahan akan terjadi pada halaman tersebut.

  <a data-flickr-embed="true" href="https://www.flickr.com/photos/190675444@N02/50501623376/in/album-72157716514998656/" title="22"><img src="https://live.staticflickr.com/65535/50501623376_32072d55ed_w.jpg" width="400" height="182" alt="22"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>


## Clone Repository
* Clone repository, pada dasarnya adalah meng-copy repository server dan secara otomatis membuat satu direktori sesuai dengan nama repositorinya.
* Untuk melakukan cloning, klik **Code**, maka akan muncul

  ``https://github.com/IlhamLamp/Repo-Pertamaku.git``

  <a data-flickr-embed="true" href="https://www.flickr.com/photos/190675444@N02/50500912133/in/album-72157716514998656/" title="23clone"><img src="https://live.staticflickr.com/65535/50500912133_6af1d2e13f_w.jpg" width="400" height="182" alt="23clone"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

* Buka **Terminal** atau **CMD** lalu ketik

  `` git clone https://github.com/IlhamLamp/Repo-Pertamaku.git"``

  <a data-flickr-embed="true" href="https://www.flickr.com/photos/190675444@N02/50501780657/in/album-72157716514998656/" title="24clone"><img src="https://live.staticflickr.com/65535/50501780657_3303bdbdd8_w.jpg" width="400" height="165" alt="24clone"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

* Ketik ``dir`` pada windows dan ``ls`` pada linux untuk melihat hasilnya.

  <a data-flickr-embed="true" href="https://www.flickr.com/photos/190675444@N02/50501780807/in/album-72157716514998656/" title="25"><img src="https://live.staticflickr.com/65535/50501780807_f82ec8798b_w.jpg" width="400" height="180" alt="25"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

* Maka repositori telah berhasil di salin.
