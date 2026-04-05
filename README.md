<div align="center">

# LAPORAN PRAKTIKUM

# APLIKASI CRUD DATA MAHASISWA

## CODING ON THE SPOTMANAJEMEN STOK

<img src="logotelu.jpeg" alt ="logo" width = "300"> 

### Disusun Oleh

**Iqbal Bawani**
2311102130
IF-11-04

### Dosen Pengampu

**Cahyo Prihantoro, S.Kom., M.Eng.**

### LABORATORIUM HIGH PERFORMANCE

FAKULTAS INFORMATIKA
UNIVERSITAS TELKOM PURWOKERTO
2026

</div>

---

# Dasar Teori

## 1. Aplikasi Web

Aplikasi web adalah perangkat lunak yang berjalan pada server dan dapat diakses melalui browser menggunakan protokol HTTP/HTTPS. Aplikasi web terdiri dari dua bagian utama yaitu frontend (client-side) dan backend (server-side). Frontend bertugas menampilkan antarmuka kepada pengguna, sedangkan backend bertugas mengelola logika aplikasi dan database.

---

## 2. CodeIgniter

CodeIgniter adalah framework PHP berbasis MVC (Model-View-Controller) yang digunakan untuk membangun aplikasi web secara terstruktur. Dengan konsep MVC, aplikasi dipisahkan menjadi:

* Model → mengelola data
* View → tampilan
* Controller → logika aplikasi

Keunggulan CodeIgniter:

* Ringan dan cepat
* Mudah dipelajari
* Dokumentasi lengkap

---

## 3. Bootstrap

Bootstrap adalah framework CSS yang digunakan untuk membuat tampilan web yang responsif dan menarik. Bootstrap menyediakan komponen seperti tombol, form, tabel, dan grid system.

---

## 4. CRUD (Create, Read, Update, Delete)

CRUD adalah operasi dasar dalam pengolahan data:

* Create → menambah data
* Read → menampilkan data
* Update → mengubah data
* Delete → menghapus data

---

## 5. jQuery

jQuery adalah library JavaScript yang digunakan untuk mempermudah manipulasi DOM dan AJAX.

---

## 6. DataTables jQuery Plugin

DataTables adalah plugin jQuery yang digunakan untuk menampilkan data dalam bentuk tabel interaktif dengan fitur:

* Pencarian (search)
* Pengurutan (sorting)
* Pagination

---

## 7. JSON (JavaScript Object Notation)

JSON adalah format pertukaran data yang ringan dan digunakan dalam aplikasi ini untuk menampilkan data pada DataTables melalui AJAX.

---

## 8. MySQL sebagai Penyimpanan Data

MySQL adalah sistem manajemen basis data yang digunakan untuk menyimpan data mahasiswa. Data disimpan dalam tabel dan diakses melalui model pada CodeIgniter.

---
## Struktur Aplikasi

```bash
COTS/                       # Root direktori utama project
│
├── app/                    # Folder utama logika aplikasi (CodeIgniter)
│   ├── Config/             # Konfigurasi sistem
│   │   └── Routes.php      # Pengaturan routing URL
│   │
│   ├── Controllers/        # Controller (pengatur alur aplikasi)
│   │   └── Mahasiswa.php   # Mengelola request CRUD dan JSON DataTables
│   │
│   ├── Models/             # Model (akses database)
│   │   └── MahasiswaModel.php  # Query database tabel mahasiswa
│   │
│   └── Views/              # Tampilan (UI)
│       └── mahasiswa/      # Folder khusus fitur mahasiswa
│           ├── index.php   # Halaman utama (DataTables + JSON)
│           ├── form.php    # Halaman tambah data mahasiswa
│           └── edit.php    # Halaman edit data mahasiswa
│
├── public/                 # Folder public (entry point aplikasi)
│   └── index.php           # File utama untuk menjalankan aplikasi
│
├── writable/               # Folder untuk cache, log, dll
│
├── .env                    # Konfigurasi database & environment
│
├── mahasiswa.sql           # File database MySQL (tabel mahasiswa)
│
└── README.md               # Dokumentasi project
```

---

## Keterangan Struktur

* **Config/Routes.php**
  Mengatur rute URL agar dapat mengakses controller dengan benar.

* **Controllers/Mahasiswa.php**
  Mengatur alur aplikasi, menerima request dari user, dan memproses CRUD.

* **Models/MahasiswaModel.php**
  Menghubungkan aplikasi dengan database MySQL dan menjalankan query.

* **Views/mahasiswa/**
  Berisi tampilan aplikasi:

  * `index.php` → halaman tabel DataTables
  * `form.php` → halaman tambah data
  * `edit.php` → halaman edit data

* **public/**
  Folder yang diakses oleh browser.

* **.env**
  Digunakan untuk konfigurasi koneksi database.

* **mahasiswa.sql**
  Berisi struktur tabel database yang digunakan dalam aplikasi.

---


## Cara Menjalankan Aplikasi

1. Buka folder project di VS Code

2. Jalankan server CodeIgniter:

```bash
php spark serve
```

3. Buka browser:

```bash
http://localhost:8080/mahasiswa
```

---

## Kode Program

### Controller (Mahasiswa.php)

Mengatur proses CRUD dan pengambilan data JSON.

### Model (MahasiswaModel.php)

Mengelola database dan field yang digunakan.

### View

Menampilkan halaman form, tabel, dan edit.

---

## Alur CRUD Aplikasi

### Create

User menginput data melalui form kemudian disimpan ke database.

### Read

Data ditampilkan menggunakan DataTables berbasis JSON.

### Update

User mengubah data melalui halaman edit.

### Delete

User menghapus data melalui tombol delete.

---

## Screenshot Website

1. Halaman Tabel Data
   (Tambahkan screenshot)

2. Halaman Tambah Data
   (Tambahkan screenshot)

3. Halaman Edit Data
   (Tambahkan screenshot)

---

## Kesimpulan

Aplikasi CRUD Data Mahasiswa berhasil dibuat menggunakan CodeIgniter dan telah memenuhi seluruh kriteria tugas, yaitu penggunaan Bootstrap, jQuery, DataTables, serta implementasi JSON.

---

## Referensi

1. https://codeigniter.com
2. https://getbootstrap.com
3. https://jquery.com
4. https://datatables.net

---

## Link Gdrive

https://drive.google.com/drive/folders/1oOSQffoSW49_lcFSTZ1C25vm2YYmrc4Z?usp=sharing
