# 📦 Tugas Dockerize WordPress

## 👤 Nama dan NIM
- Nama : Ivan Hermansyah
- NIM  : A11.2023.14952

---

📌 1. Deskripsi Project

Project ini adalah implementasi WordPress menggunakan Docker Compose dengan layanan:

- WordPress
- MySQL
- Redis

🚀 2. Tutorial Menjalankan Stack
1. Pastikan sudah menginstal docker, lalu jalankan docker dekstop 
2. Masuk ke folder project melalui terminal laptop: 
   "cd wordpress-docker"
3. Jalankan container:
   "docker-compose up -d"
4. Cek apakah container sudah berjalan:
   "docker ps"
5. Akses wordpress di browser:
   "http://localhost:8000"

📸 3. Screenshot hasil
1. Menjalankan service atau compose (screenshot/service.png)
2. Halaman awal wordpress (screenshot/page_instalasi.png)
3. Tampilan Dashboard Wordpress (screenshot/dashboard.png)
4. Checklist 3 container running (screenshot/info_container.png)
5. Test redis ping (screenshot/redis_ping.png)
6. Test positingan baru di wordpress (screenshot/new_post.png)
7. Konfigurasi redis cache (screenshot/redis_cache.png)

❓ 4. Jawaban Pertanyaan
1. Kenapa perlu volume untuk MySQL?
Volume digunakan agar data database tidak hilang saat container dihentikan atau dihapus.
Tanpa volume, semua data akan ikut terhapus karena container bersifat sementara.

2. Apa fungsi depends_on?
depends_on digunakan untuk menentukan urutan startup container.

3. Bagaimana cara WordPress container connect ke MySQL?
WordPress terhubung ke MySQL melalui environment variable
mysql adalah nama service (hostname otomatis Docker)
Port 3306 adalah port MySQL

Docker otomatis membuat jaringan internal sehingga container bisa saling terhubung

4. Apa keuntungan pakai Redis untuk WordPress?
Redis digunakan sebagai caching system.

Keuntungannya:

Mempercepat loading website
Mengurangi beban database MySQL
Meningkatkan performa WordPress
Cocok untuk website dengan traffic tinggi