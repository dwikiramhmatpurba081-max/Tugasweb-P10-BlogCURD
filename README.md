# Blog CRUD Laravel

Aplikasi blog sederhana untuk Tugas Rutin 10. Fitur mencakup CRUD postingan, validasi form, pencarian, pagination, soft delete dan pemulihan, serta unggah gambar.

## Menjalankan aplikasi

1. Pastikan PHP 8.2+, Composer, dan ekstensi PHP SQLite serta GD aktif.
2. Pasang dependency dan siapkan konfigurasi:

   ```powershell
   composer install
   Copy-Item .env.example .env
   php artisan key:generate
   New-Item database\database.sqlite -ItemType File
   php artisan migrate
   php artisan storage:link
   php artisan serve
   ```

3. Buka `http://127.0.0.1:8000`.

Jika file database sudah ada, lewati perintah `New-Item`. File gambar disimpan pada disk `public` di `storage\app\public\posts`.

## Pengujian

Jalankan semua pengujian dengan:

```powershell
php artisan test
```

Database pengujian menggunakan SQLite in-memory.
