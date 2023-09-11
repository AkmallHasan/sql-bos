# Roadmap Belajar SQL 

## 1. Introduction

### Pengertian Basis Data Relasional 
Basis data relasional adalah basis data yang menyimpan dan menyusun data secara terstruktur, sehingga memungkinkan suatu data 
diproses berdasarkan hubungannya antar data dalam suatu table. Data disimpan didalam masing-masing table yang ada dalam database 
dan dibuat unique berdasarkan unique tiap baris dalam table. Dalam setiap table terdiri atas masing-masing kolom yang menunjukan 
suatu kategori dan masing-masing baris yang menunjukan data. 

Basis data relational berasal dari sebuah konsep relasi- hubungan data tuple yang tersusun dari data baris dan kolom yang saling 
berhubungan. basis data relasional menggunakan key untuk membuat link antar table. 
- primary key : nilai unique untuk mengidentikasi data per baris dalam tabel
- foreign key : suatu kolom atau kombinasi kolom yang digunakan untuk membuat atau memaksa 2 tabel atau lebih menjadi terhubung.

### Kelebihan dan Kekurangan RDBMS
Kelebihan
+ Data menjadi tersturktur, RDBMS menjadikan data terstuktur menurut baris dan kolom sehingga effisien dan fleksible digunakan
+ Fitur ACID, RDBMS dapat diandalkan untuk tujuan aplikasi khusus
+ Normalisasi Data, terhindar dari redudansi data 
+ Scalability, memungkinkan untuk menambah penyimpanan yang lebih luas
+ Data terintegrasi, data akurat dan dapat diandalkan karena banyak aturan yang dapat ditetapkan
+ Aman, terdapat berbagai fitur keamanan yang disediakan

Kekurangan
- Kompleks, sulit diolah khususnya untuk data yang sangat besar memerlukan pengetahuan yang mumpuni untuk pengolahan
- Memerelukan Biaya, lisensi yang tidak murah untuk RDBMS berbayar
- Fixed Schema, semakin banyak skema yang digunakanakan semakin sulit dan memakan waktu untuk pengolahan
- Tidak cocok digunakan untuk data yang tidak terstruktur

## 2. Basic SQL Syntax
SQL memiliki banyak perintah yang digunakan untuk berinteraksi dengan basis data yang digunakan, antara lain :

**1. Membuat dan Menghapus Basis Data**
Hal yang pertama dilakukan dalam pengolahan basis data adalah membuat basis data nya terlebih dahulu. Untuk pembuatan basis data gunakan perintah CREATE beserta nama basis datanya dan jika ingin menghapus gunakan perintah DROP beserta nama basis datanya. Berikut perintah yang umum digunakan ketika menjalankan database pertama kali,

<div align="center">
| Command | Description |
| --- | --- |
| CREATE DATABASE `name_database` | Membuat basis data  |
| DROP DATABASE `name_database` | Menghapus basis data |
</div>

**2. Manipulasi Tabel dalam Basis Data**
Setelah Basis Data dibuat, selanjutnya membuat table. Dalam sebuah RDBMS dapat terdiri dari satu atau beberapa RDBMS. Umumnya pembuatan tabel selalu disesuaikan dengan tujuan penggunaan aplikasi basis data tersebut. Untuk membuat tabel gunakan perintah CREATE TABLE dan DROP TABLE jika ingin menghapus. Tujuan dari pembuatan tabel yaitu untuk tempat susunan data sesuai dengan kolom dan baris yang tersedia. Karena tujuannya lebih spesifik menjadikan terdapat berbagai perintah untuk memanipulasi data tabel. Barikut perintah yang umum digunakan ketika manipulasi data tabel.

<div align="center">
| Command | Description |
| --- | --- |
| CREATE TABLE `name_table` (`name_columnX` `typedata_columnX` `defaultvalue_columnX`) | Membuat table  |
| DROP TABLE `name_table` | Menghapus table |
| DESCRIBE  `name_table` | Melihat Struktur table |
</div>

**3. Memasukan Data ke dalam Tabel** 
Setelah database beserta kolom berhasil dibuat, selanjutnya kita memasukan data ke dalam masing-masing kolom pada tabel. Perlu diketahui bahwa kita tidak dapat memasukan data tanpa membuat tabel terlebih dahulu. Untuk memasukan data gunakan perintah INSERT, apabila terjadi kesalahan maka tidak perlu menghapus tabel, cukup hapus data yang salah dengan menggunakan perintah DELETE. Jika kolom dalam suatu tabel tidak disebutkan saat pengisian data dalam tabel, maka kolom tersebut tidak akan terisi dan secara otomatis akan bernilai `NULL Values` kecuali pada kolom tersebut tersedia default value. 

Apabila sewaktu-waktu terjadi penambahan data terhadap tabel yang pernah dibuat gunakan perintah UPDATE untuk menambahkan data baru tersebut. Berikut perintah-perintah yang digunakan dalam memanipulasi data,

| Command | Description |
| --- | --- |
| INSERT INTO `name_table` ( `name_column1`,`name_column2`, `name_column3`) VALUES (`ValuesColumn1`,`ValuesColumn2`,`ValuesColumn3`)| Memasukan data |



| DROP TABLE `name_table` | Menghapus table |
| DESCRIBE  `name_table` | Melihat Struktur table |
| ALTER TABLE  `name_table` ADD COLUMN `name_column` | Menambah kolom |
| ALTER TABLE  `name_table` DROP COLUMN `name_column` | Menghapus kolom |
| ALTER TABLE  `name_table` RENAME COLUMN `name_column_old` TO `name_column_new`  | Mengubah Nama kolom |















SELECT = Perintah ini digunakan untuk mengambil data dalam basis data. Perintah ini umumnnya akan menyebutkan nama kolom yang 
ingin diambil datanya  dan penggunaaan tanda * untuk mengambil seluruh data kolom dalam table. 

2. FROM = Perintah ini biasa digunakan setelah perintah SELECT. Perintah ini akan merujuk pada table yang digunakan.
3. WHERE = Jika data ingin kita ambil merupakan data yang spesifik, maka perintah ini digunakan untuk filter data atau mengambil 
data yang lebih spesifik daripada sekedar mengambil data dalam satu kolom sekaligus
4. INSERT INTO = Perintah ini digunakan untuk memasukan data ke dalam table
5. UPDATE = Perintah ini digunakan untuk mengubah data yang ada. 
6. DELETE = perintah ini digunakan untuk menghapus data 


## 3. Data Definition Language
## 4. Data Manipulation Language
## 5. Aggregate Queries
## 6. Data Constraints
## 7. JOIN Queries
## 8. Sub Queries
## 9. Advanced SQL Functions
## 10. Views
## 11. Indexes
## 12. Transactions
## 13. Data Integrity and Security
## 14. Stored Procedures and Functions
## 15. Performance Optimization
## 16. Advanced SQL Concepts

