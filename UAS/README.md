<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.

## Learning Laravel

Laravel has the most extensive and thorough [documentation](https://laravel.com/docs) and video tutorial library of all modern web application frameworks, making it a breeze to get started with the framework.

In addition, [Laracasts](https://laracasts.com) contains thousands of video tutorials on a range of topics including Laravel, modern PHP, unit testing, and JavaScript. Boost your skills by digging into our comprehensive video library.

You can also watch bite-sized lessons with real-world projects on [Laravel Learn](https://laravel.com/learn), where you will be guided through building a Laravel application from scratch while learning PHP fundamentals.

## Agentic Development

Laravel's predictable structure and conventions make it ideal for AI coding agents like Claude Code, Cursor, and GitHub Copilot. Install [Laravel Boost](https://laravel.com/docs/ai) to supercharge your AI workflow:

```bash
composer require laravel/boost --dev

php artisan boost:install
```

Boost provides your agent 15+ tools and skills that help agents build Laravel applications while following best practices.

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).



# Aplikasi Blog CMS + Halaman Publik - UAS Pemrograman Web

**Nama:** [Naufal Ghali Rahadi]  
**NIM:** [240605110161]  
**Mata Kuliah:** Pemrograman Web  
**Semester:** Genap 2025/2026  
**Dosen:** A’la Syauqi M.Kom.

---

## 📌 Deskripsi Proyek

Aplikasi Blog ini merupakan **sistem manajemen konten (CMS)** lengkap yang dilengkapi dengan **halaman publik** untuk pengunjung. Dibangun menggunakan **Laravel 11** dan **Bootstrap 5**. Aplikasi ini memungkinkan penulis (admin) untuk mengelola artikel, penulis, dan kategori artikel, sedangkan pengunjung dapat membaca artikel terbaru, menyaring berdasarkan kategori, serta melihat artikel terkait.

Proyek ini memenuhi seluruh spesifikasi **Ujian Akhir Semester (UAS)** yang meliputi:
- Halaman publik dengan 5 artikel terbaru dan widget kategori
- Filter artikel berdasarkan kategori
- Halaman detail artikel dengan 5 artikel terkait dari kategori yang sama
- CMS (login, CRUD artikel, penulis, kategori) yang dilindungi autentikasi
- Tampilan bersih, sederhana, elegan, dan responsif

> **Catatan:** Proyek ini merupakan pengembangan dari Modul 10 (CMS) dengan penambahan fitur publik sesuai UAS.

---

## 🔧 Teknologi yang Digunakan

- **Framework:** Laravel 11
- **Frontend:** Bootstrap 5, Font Awesome 6, CSS3
- **Database:** MySQL (db_blog)
- **Bahasa Pemrograman:** PHP 8.2+
- **Tools:** Laragon, Composer, Git, Visual Studio Code

---

## ⚙️ Fitur Aplikasi

### 🔐 Autentikasi (Login & Registrasi)
- Login dengan username dan password
- Registrasi akun penulis baru
- Proteksi halaman CMS dengan middleware `auth`

### 📝 CMS (Sistem Manajemen Konten)
| Fitur | Keterangan |
|-------|-------------|
| Manajemen Artikel | Tambah, edit, hapus artikel (dengan upload gambar) |
| Manajemen Penulis | Tambah, edit, hapus penulis (dengan upload foto) |
| Manajemen Kategori | Tambah, edit, hapus kategori artikel |
| Dashboard | Menampilkan statistik, 5 artikel terbaru milik penulis yang login, dan waktu login |

### 🌐 Halaman Publik (Tanpa Login)
| Halaman | Fungsi |
|---------|--------|
| Beranda | Menampilkan 5 artikel terbaru, widget kategori di samping |
| Filter Kategori | Menyaring artikel berdasarkan kategori yang dipilih |
| Detail Artikel | Menampilkan isi lengkap artikel + 5 artikel terkait (kategori sama) |
| Daftar Kategori | Menampilkan semua kategori dengan jumlah artikel |
| Halaman Tentang | Informasi statis tentang blog |

### 🧭 Navigasi
- Menu **Beranda**, **Artikel** (sama dengan beranda), **Kategori**, **Tentang**
- Tombol **Login Admin** / **Dashboard** di pojok kanan atas (berubah sesuai status login)
- Breadcrumb di halaman detail artikel
- Tombol **Kembali ke Beranda** di halaman detail

---

## 📁 Struktur Database (db_blog)

Tabel yang digunakan sesuai dengan soal UTS dan Modul 10 (tanpa perubahan struktur):

| Tabel | Kolom utama |
|-------|--------------|
| `penulis` | id, nama_depan, nama_belakang, user_name, password, foto |
| `kategori_artikel` | id, nama_kategori, keterangan |
| `artikel` | id, id_penulis, id_kategori, judul, isi, gambar, hari_tanggal |

Relasi:  
- `artikel.id_penulis` → `penulis.id` (ON DELETE RESTRICT)  
- `artikel.id_kategori` → `kategori_artikel.id` (ON DELETE RESTRICT)

---

## 📁 Struktur Folder (Laravel)

Hanya direktori utama yang relevan:

```
aplikasi-blog/
├── app/
│ ├── Http/
│ │ ├── Controllers/
│ │ │ ├── ArtikelController.php
│ │ │ ├── PenulisController.php
│ │ │ ├── KategoriArtikelController.php
│ │ │ ├── LoginController.php
│ │ │ ├── RegisterController.php
│ │ │ ├── DashboardController.php
│ │ │ ├── PublicController.php
│ │ │ └── PublicArticleController.php
│ │ └── Middleware/
│ └── Models/
│ ├── User.php
│ ├── Artikel.php
│ ├── Penulis.php
│ └── KategoriArtikel.php
├── resources/
│ └── views/
│ ├── layouts/
│ │ ├── app.blade.php (layout CMS)
│ │ └── public.blade.php (layout publik)
│ ├── artikel/
│ ├── penulis/
│ ├── kategori/
│ ├── dashboard/
│ ├── login/
│ ├── auth/
│ └── public/
│ ├── home.blade.php
│ ├── show.blade.php
│ ├── categories.blade.php
│ └── about.blade.php
├── routes/
│ └── web.php
├── public/
│ └── storage/ (symlink ke storage/app/public)
├── storage/
│ └── app/public/
│ ├── foto/ (foto profil penulis)
│ └── gambar/ (gambar artikel)
├── .env
└── composer.json
