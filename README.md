# Week-4_1-Seeders-pada-tabel-users-dan-khs
Untuk memulai materi migration , siapkan beberapa tools berikut :

    1. XAMPP / SQLyog
    2. VsCode / IDE yang lain
    3. Langkah-langkah sebelum membuat migration:
      1) Buat folder service-user
      2) Buka terminal lalu masuk ke folder service-user dengan perintah CD(change directory)
      3) Jika sudah ketikkan perintah-perintah berikut :
      4) npx express-generator --no-view (Jika tidak ingin menggunakan view)
      5) npm i
      6) npm i nodemon
      7) npm dotenv --save
      8) npm i --save sequelize sequelize-cli
      9) npx sequelize init (Berfungsi untuk memunculkan folder default dari sequelize)
      10) npm i mysql2 --save
Jika sudah, waktunya membuat migration. Berikut ini adalah cara membuat migration: 
      1) Buat file .env di folder yang sama seperti file app.js. Pada file .env isikan sesuai pada file di repository. 
      2) Rename file config.json yang ada pada folder config menjadi config.js dan edit seperti file config.js yang ada pada repository. 
      3) Edit file index.js pada folder models, edit sesuai file index.js di repository ini (ada di folder models juga). 
      4) Edit file app.js seperti pada file app.js diatas. 
      5) Pada terminal ketikkan npx sequelize migration:create --name=(nama file migration) -> create-table-users yang nantinya berfungsi untuk membuat file migration untuk tabel users 
      6) Pada terminal ketikkan npx sequelize migration:create --name=(nama file migration) -> create-table-khs yang nantinya berfungsi untuk membuat file migration untuk tabel khs 
      7) Isi kedua file migration seperti pada file yang ada di folder migrations i repository ini. 
      8) Jika sudah hidupkan xampp/mysql dan buat database dengan nama service_users 
      9) Selanjutnya ketikkan npx sequelize db:migrate untuk membuat table di database dengan migrate
Selanjutnya untuk membuat seeders, caranya adalah sebagai berikut:
      1) npx i bcrypt --save ( Untuk menginstall libary bcrypt yang berfungsi untuk mengenkripsi data password nantinya).
      2) npx sequelize seed:create --name=(nama file seed yang ingin dibuat) -> create-seed-users untuk mengisi data pada kolom yang ada di tabel users.
      3) npx sequelize seed:create --name=(nama file seed yang ingin dibuat) -> create-seed-khs untuk mengisi data pada kolom yang ada di tabel khs.
     */ CATATAN/*
     Sejauh ekplorasi saya tentang seed, kita bisa mengisi data pada 2 tabel bersamaan
