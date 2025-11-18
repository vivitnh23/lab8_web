# lab8_web
# Nama : Vivit Nurul Hidayah
# NIM : 312410110
# Kelas : TI.24.A.1
# Mata Kuliah : Pemrograman Web
# Dosen : Agung Nugroho S.Kom, M.Kom

# **Praktikum 8 — PHP & Database MySQL**

Repository ini berisi hasil praktikum mengenai penggunaan PHP dan MySQL untuk membangun aplikasi CRUD sederhana. Materi praktik meliputi pembuatan database, koneksi ke MySQL, dan implementasi fitur Create, Read, Update, Delete pada data barang.

---

## **Tujuan Praktikum**

* Memahami konsep dasar database dan MySQL.
* Mengimplementasikan CRUD menggunakan PHP.
* Membuat aplikasi CRUD sederhana berbasis web.

---

## **Langkah-langkah Praktikum**

### **1. Persiapan**

* Gunakan text editor seperti VSCode.
* Jalankan Apache & MySQL melalui XAMPP Control Panel.
* Buat folder baru bernama `lab8_php_database` pada direktori `htdocs`.

---

### **2. Membuat Database**

Masuk ke phpMyAdmin melalui `http://localhost/phpmyadmin/` lalu buat database:

```
CREATE DATABASE latihan1;
```

### **3. Membuat Tabel**

Buat tabel `data_barang` untuk menyimpan data barang:

```
CREATE TABLE data_barang (
  id_barang int(10) auto_increment Primary Key,
  kategori varchar(30),
  nama varchar(30),
  gambar varchar(100),
  harga_beli decimal(10,0),
  harga_jual decimal(10,0),
  stok int(4)
);
```

### **4. Menambahkan Data Awal**

```
INSERT INTO data_barang (kategori, nama, gambar, harga_beli, harga_jual, stok)
VALUES
('Elektronik', 'HP Samsung Android', 'hp_samsung.jpg', 2000000, 2400000, 5),
('Elektronik', 'HP Xiaomi Android', 'hp_xiaomi.jpg', 1000000, 1400000, 5),
('Elektronik', 'HP OPPO Android', 'hp_oppo.jpg', 1800000, 2300000, 5);
```

---

## **5. Membuat Program CRUD**

### **a. Koneksi ke Database**

File: **koneksi.php**
Berisi konfigurasi koneksi MySQL menggunakan `mysqli_connect`.

### **b. Menampilkan Data (Read)**

File: **index.php**
Menampilkan seluruh data dari tabel `data_barang` dalam bentuk tabel HTML.

### **c. Menambah Data (Create)**

File: **tambah.php**
Menggunakan form input untuk menambahkan data baru, termasuk upload gambar.

### **d. Mengubah Data (Update)**

File: **ubah.php**
Mengambil data berdasarkan `id_barang`, menampilkan form edit, dan menyimpan perubahan.

### **e. Menghapus Data (Delete)**

File: **hapus.php**
Menghapus data berdasarkan ID, kemudian redirect kembali ke halaman utama.

---

## **Struktur Folder**

```
lab8_php_database/
│── index.php
│── tambah.php
│── ubah.php
│── hapus.php
│── koneksi.php
│── style.css
└── gambar/
```

---

## **Laporan Praktikum**

* Membuat repository **Lab8Web**.
* Mengikuti seluruh langkah praktikum dari pembuatan database hingga CRUD.
* Menyertakan screenshot hasil setiap tahap.
* Menuliskannya dalam file `README.md`.
* Melakukan commit dan mengunggah ke repository GitHub.

---

# Output Index.php
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/602b47c1-f97b-455b-9cb2-a251d33c057c" />

# Output Tambah.php
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/65729134-ffdd-462c-a95c-0cab42ee01ac" />

# Output Ubah.php
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/be2b8505-4f07-4a4f-9d93-6cf029cc91fc" />


