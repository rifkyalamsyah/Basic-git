## Konfigurasi Awal GIT

- Username & Email

  `git config --global user.name "Rifky Alamsyah"`
  
  `git config -- global user.email rifkyalamsyah30@gmail.com`
  
  Kemudian periksa konfigurasinya dengan perintah:
  
  `git config --list`
  
  *Apabila berhasil tampil, berarti konfigurasi berhasil.
  
  
  
  ## Membuat Repositori

- Membuat Repositori

  `git init`

   Contohnya:

   `mkdir myproject`

   `cd myproject`

   `git init`

    *Perintah ini akan membuat repositori pada direktori
    
   
   ## Note

  - .gitignore

    .gitignore merupakan sebuah file yang berisi daftar nama-nama file dan direktori yang akan diabaikan oleh Git.

    Perubahan apapun yang kita lakukan terhadap file dan direktori yang sudah masuk ke dalam daftar .gitignore tidak akan dicatat oleh Git.

    Cara mengunakan .gitignore, buat saja sebuah file bernama .gitignore dalam root direktori proyek/repositori.

    `/vendor/`

    `/upload/`

    `/cache`

    `test.js`

    Pada contoh file .gitignore di atas, saya memasukan direktori `vendor, upload, cache dan file test.js` File dan direktori tersebut akan diabaikan oleh Git.

    *Pembuatan file .gitignore sebaiknya dilakukan di awal pembuatan repositori.



## Perintah dasar GIT

- git config
  
  Salah satu perintah git yang paling banyak digunakan adalah git config, yang bisa digunakan untuk mengatur konfigurasi tertentu sesuai keinginan pengguna, seperti email, algoritma untuk diff, username, format file, dll. Contohnya, perintah berikut bisa digunakan untuk mengatur email:

  `git config --global user.email rifkyalamsyah30@gmail.com`
  

- git init

   Perintah ini digunakan untuk membuat repositori baru. Caranya:

  `git init`

- git add
  
  Perintah git add bisa digunakan untuk menambahkan file ke index. Contohnya, perintah berikut ii akan menambahkan file bernama temp.txt yang ada di direktori lokal ke index:

  `git add index.txt`

- git clone
  
  Perintah git clone digunakan untuk checkout repositori. Jika repositori berada di remove server, gunakan:
  
  `git clone`
  
  contohnya:
  
  `git clone https://github.com/rifkyalamsyah/Basic-git.git`

- git commit

  Perintah git commit digunakan untuk melakukan commit pada perubahan ke head. Ingat bahwa perubahan apapun yang di-commit tidak akan langsung ke remote repository. Gunakan:
  
  `git commit -m "first commit"`
  
- git status

  Perintah git status menampilkan daftar file yang berubah bersama dengan file yang ingin di tambahkan atau di-commit. Gunakan:
  
  `git status`
  
- git push
    
  git push adalah perintah git dasar lainnya. Push akan mengirimkan perubahan ke master branch dari remote repository yang berhubungan dengan direktori kerja Anda. Misalnya:
  
  `git push origin master`
  
- git checkout

  Perintah git checkout bisa digunakan untuk membuat branch atau untuk berpindah diantaranya. Misalnya, perintah berikut ini akan membuat branch baru dan berpindah ke dalamnya:
  
  `command git checkout -b <nama-branch>`
  
  contohnya: 
  
  `command git checkout -b master`
  
  Untuk berpindah dari branch satu ke lainnya, gunakan:
  
  `git checkout <branch-name>`
  
  contohnya:
  
  `git checkout master`
  
- git remote

  Perintah git remote akan membuat user terhubung ke remote repository. Perintah berikut ini akan menampilkan repository yang sedang dikonfigurasi:
  
  `git remote -v`
  
  Perintah ini membuat user bisa menghubungkan repository lokal ke remote server:
  
  `git remote origin https://github.com/rifkyalamsyah/Basic-git.git`
  
- git branch

  Perintah git branch bisa digunakan untuk me-list, membuat atau menghapus branch. Untuk menampilkan semua branch yang ada di repository, gunakan:
  
  `git branch`
  
  untuk menghapus branch:
  
  `git branch -d <branch-name>`
  
  contohnya:
  
  `git branch -d master`

- git pull 

  Perintah git branch bisa digunakan untuk me-list, membuat atau menghapus branch. Untuk menampilkan semua branch yang ada di repository, gunakan:
  
  `git pull`
  
- git merge

  Perintah merge digunakan untuk menggabungkan sebuah branch ke branch aktif. Gunakan:
  
  `git merge <branch-name>`
  
  contohnya:
  
  `git merge master`
  
- git diff

  Perintah git diff digunakan untuk menampilkan conflicts. Untuk melihat conflicts dengan file dasar, gunakan:
  
  `git diff --base <file-name>`
  
  Perintah berikut digunakan untuk menampilkan conflicts diantara branch yang akan di-merge:
  
  `git diff <source-branch> <target-branch>`
  
  Untuk menampilkan semua conflict yang ada, gunakan:
  
  `git diff`
  
- git tag 

  Tagging digunakan untuk mmenandai commits tertentu. contohnya:
  
  `git tag 1.1.0 <insert-commitID-here>`
  
- git log

  Dengan menjalankan perintah ini akan menampilkan daftar commits yang ada di branch beserta detail-nya. contoh outputnya:
  
  `commit 3ab5ba48b597d4ab2c65c39e253d6fd33d2881b2 (HEAD -> master, origin/master)`
  
  `Author: Rifky Alamsyah <rifkyalamsyah30@gmail.com>`
  
  `Date:   Thu Jul 15 11:23:11 2021 +0700`
  
- git reset

  Untuk me-reset index dan bekerja dengan kondisi commit paling baru, gunakan perintah git reset:
  
  `git reset -- hard HEAD`
  
- git rm 

  Gunakan perintah ini untuk menghapus file dari index dan direktori kerja. Contohnya:
  
  `git rm index.txt`
  
- git stash

  Mungkin inilah salah satu perintah dasar git yang jarang di gunakan, namun bisa membantu menyimpan perubahan yangtidak langsung di-commit, namun hanya sementara. Contohnya:
  
  `git stash`
  
- git show

  Untuk menampilkan informasi tentang objek pada git, gunakan git show:
  
  `git show`
  
- git fetch

  Perintah ini digunakan untuk menampilkan semua object dari remote repository yang tidak berada di direktori kerja lokal. Contohnya:
  
  `git fetch origin`
  
- git ls-tree

  Untuk menampilkan susunan object berdasarkan nama dan mode setiap item, dan nilai blob SHA-1, gunakan perintah git ls-tree. Contohnya:
  
  `git ls-tree HEAD`
  
- git cat-file
  
  Menggunakan nilai SHA-1, menampilkan tipe object dengan menggunakan perintah git cat-file. Contohnya:

  `git cat-file –p d670460b4b4aece5915caf5c68d12f560a9fe3e4`
  
- git prep
  
  git prep mengizinkan pengguna mencari frase dan/atau kata yang berada di dalam direktori. Contohnya, untuk mencari www.rifkyalamsyah.com di dalam semua file, gunakan:

  `git grep "www.rifkyalamsyah.com"`

- gitk
  
  gitk adalah tampilan grafis dari repository lokal yang bisa dipanggil dengan menjalankan perintah:

  `gitk`
  
- git instaweb

  Dengan perintah git instaweb, web server bisa dijalan berdampingan dengan repository lokal. Nantinya web browser akan langsung diarahkan ke server tersebut. Contohnya:
  
  `git instaweb –httpd=webrick`

- git gc
  
  Untuk mengoptimasi repository melalui garbage collection, yang akan membersihkan file yang tidak dibutuhkan dan mengoptimasinya, gunakan:
  
  `git gc`
  
- git archive

  Perintah git archive memungkinkan user membuat file zip atau tar yang mengandung susunan repository. Contohnya:
  
  `git archive --format=tar master`

- git prune

  Melalui perintah git prune, object yang tidak memiliki incoming pointers akan dihapus. Gunakan:
  
  `git prune`

- git fsck

  Untuk membuat pengecekan keseluruhan dari file system git, gunakan perintah git fsck. Object yang corrupt akan dikenali:

  `git fsck`

- git rebase

  Perintah ini digunakan untuk menerapkan ulang commit di branch yang lain. Contohnya:

  `git rebase master` 
  
