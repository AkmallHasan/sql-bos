# Roadmap Belajar SQL 

# 1. Introduction

## Pengertian Basis Data Relasional 
Basis data relasional adalah basis data yang menyimpan dan menyusun data secara terstruktur, sehingga memungkinkan suatu data 
diproses berdasarkan hubungannya antar data dalam suatu table. Data disimpan didalam masing-masing table yang ada dalam database 
dan dibuat unique berdasarkan unique tiap baris dalam table. Dalam setiap table terdiri atas masing-masing kolom yang menunjukan 
suatu kategori dan masing-masing baris yang menunjukan data. 

Basis data relational berasal dari sebuah konsep relasi- hubungan data tuple yang tersusun dari data baris dan kolom yang saling 
berhubungan. basis data relasional menggunakan key untuk membuat link antar table. 
- primary key : nilai unique untuk mengidentikasi data per baris dalam tabel
- foreign key : suatu kolom atau kombinasi kolom yang digunakan untuk membuat atau memaksa 2 tabel atau lebih menjadi terhubung.

## Kelebihan dan Kekurangan RDBMS
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

# 2. Basic SQL Syntax
SQL memiliki banyak perintah yang digunakan untuk berinteraksi dengan basis data yang digunakan, antara lain :

## 1. SQL Keywords

### **A. Membuat dan Menghapus Basis Data**

Hal yang pertama dilakukan dalam pengolahan basis data adalah membuat basis data nya terlebih dahulu. Untuk pembuatan basis data gunakan perintah CREATE beserta nama basis datanya dan jika ingin menghapus gunakan perintah DROP beserta nama basis datanya. Berikut perintah yang umum digunakan ketika menjalankan database pertama kali,

<div align="center">
  
| Command | Description |
| :--- | :--- |
| CREATE DATABASE `name_database` | Membuat basis data  |
| DROP DATABASE `name_database` | Menghapus basis data |

</div>

### **B. Manipulasi Tabel dalam Basis Data**

Setelah Basis Data dibuat, selanjutnya membuat table. Dalam sebuah RDBMS dapat terdiri dari satu atau beberapa RDBMS. Umumnya pembuatan tabel selalu disesuaikan dengan tujuan penggunaan aplikasi basis data tersebut. Untuk membuat tabel gunakan perintah CREATE TABLE dan DROP TABLE jika ingin menghapus. Tujuan dari pembuatan tabel yaitu untuk tempat susunan data sesuai dengan kolom dan baris yang tersedia. Karena tujuannya lebih spesifik menjadikan terdapat berbagai perintah untuk memanipulasi data tabel. Barikut perintah yang umum digunakan ketika manipulasi data tabel.

<div align="center">
  
| Command | Description |
| :--- | :--- |
| CREATE TABLE `name_table` (`name_columnX` `typedata_columnX` `defaultvalue_columnX`) | Membuat table  |
| DROP TABLE `name_table` | Menghapus table |
| DESCRIBE  `name_table` | Melihat Struktur table |
| `name_columnX` `typedata_columnX` NOT NULL | Menghindari data NULL pada tiap kolom|
| `name_columnX` `typedata_columnX` NOT NULL DEFAULT | Memasukan Nilai Otomatis |

</div>

### **C. Memasukan Data ke dalam Tabel** 

Setelah database beserta kolom berhasil dibuat, selanjutnya kita memasukan data ke dalam masing-masing kolom pada tabel. Perlu diketahui bahwa kita tidak dapat memasukan data tanpa membuat tabel terlebih dahulu. Untuk memasukan data gunakan perintah INSERT, apabila terjadi kesalahan maka tidak perlu menghapus tabel, cukup hapus data yang salah dengan menggunakan perintah DELETE. Jika kolom dalam suatu tabel tidak disebutkan saat pengisian data dalam tabel, maka kolom tersebut tidak akan terisi dan secara otomatis akan bernilai `NULL Values` kecuali pada kolom tersebut tersedia default value. Apabila sewaktu-waktu terjadi penambahan data terhadap tabel yang pernah dibuat gunakan perintah UPDATE untuk menambahkan data baru tersebut. Berikut perintah-perintah yang digunakan dalam memanipulasi data,

<div align="center">
  
| Command | Description |
| :--- | :--- |
| INSERT INTO `name_table` ( `name_column1`,`name_column2`, `name_column3`) VALUES (`ValuesColumn1`,`ValuesColumn2`,`ValuesColumn3`)| Memasukan data |
| DELETE FROM `name_table` WHERE `spesific row with operation` | Menghapus data |
| UPDATE `name_table` SET `spesific column with operation` WHERE `spesific row with operation`| Menambahkan data |

</div>

## 2. Tipe Data
Tipe Data dalam SQL ada banyak sekali, berikut adalah tipe data yang umum digunakan, antara lain:

### 1. Tipe Data Character

Tipe data ini biasa disimpan dalam bentuk text, number dan symbol. Tipe data ini terdiri dari 3 jenis yaitu char, varchar dan text. 
- char**, tidak peduli seberapa banyak data yang disimpan hanyalah storage dengan nilai awal. digunakan pada data yang sudah pasti panjang datanya
- **varchar**, penyimpanan bergantung pada banyak atau sedikitnya data yang dimasukan. lebih banyak digunakan karena optimal dalam pengguaan data yang sedikit
- **text**, memiliki panjang data yang tidak terbatas. Jarang digunakan karena tipe data ini terlalu besar untuk digunakan, hanya pada keadaan tertentu saja. 

### 2. Tipe Data Numeric

Tipe data ini secara garis besar terdiri atas dua jenis yaitu,
- **Intergers**, yaitu tipe data untuk bilangan bulat termasuk bilangan positive dan negative.
- **Fixed-Point & Floating Point**, yaitu tipe data untuk nilai pecahan (desimal). Fixed Point menggunakan jumlah digit desimalnya tetap sehingga presisi dapat dikontrol dan biasa digunakan untuk perhitungan keuangan. contohnya tipe Desimal dan Numeric . Sedangkan pada Floating Point jumlah digit desimalnya mengikuti standar IEEE 754 ang mendefinisikan format untuk merepresentasikan angka dalam bentuk mantissa (fraksional) dan eksponen (pangkat 10). Floating-point dapat mewakili kisaran nilai yang sangat besar atau sangat kecil, yang sering digunakan dalam perhitungan ilmiah dan teknik. contohnya Real dan Double Precision.

### 3. Tipe Data Datetime

Tipe data datetime digunakan untuk melakukan pengolahan data tanggal. beberapa jenis tipe data datetime,
- **timestamp** digunakan untuk mengolah data tanggal beserta waktu jam.
- **date** digunakan untuk data tanggal
- **time** digunakan untuk data waktu jam
- **interval** digunakan sebagai selisih antar periode waktu tertentu

### 4. Tipe Data Boolean

Tipe data Boolean adalah tipe data kebenaran karena hanya berisi dua hasil TRUE atau FALSE

### 5. Tipe Data ENUM

Tipe data ENUM adalah tipe data yang digunakan untuk memilih satu opsi dari beberapa opsi yang telah dibuat/ditentukan. 


## 3. Operators




### 4. Statements




