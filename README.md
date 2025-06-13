# SITS CCTV MAPS WEB APP

## Pemasangan Dependensi

1. Pastikan Anda memiliki **Node.js** dan **npm** (Node Package Manager) yang sudah terinstal di perangkat Anda.
2. Jalankan perintah berikut untuk menginstal seluruh dependensi yang diperlukan:
   ```bash
   npm install
   ```

## Daftar Dependencies Utama

- **Express.js**: Framework untuk membangun server backend.
- **PostgreSQL + PostGIS**: Database utama dengan dukungan fitur geospasial.
- **Sequelize**: ORM untuk memudahkan pengelolaan database.
- **dotenv**: Mengelola variabel lingkungan secara aman.
- **Jest**: Framework untuk pengujian unit.
- **ESLint**: Alat untuk memastikan kualitas kode.

## Teknologi yang Digunakan

- **Backend**: Node.js, Express.js
- **Database**: PostgreSQL + PostGIS
- **ORM**: Sequelize
- **Testing**: Jest
- **Manajemen Environment**: dotenv
- **Linting**: ESLint

## Instalasi & Konfigurasi PostgreSQL + PostGIS

1. **Instal PostgreSQL**:
   - Unduh PostgreSQL dari [situs resmi](https://www.postgresql.org/download/).
   - Ikuti panduan instalasi sesuai sistem operasi Anda.

2. **Tambahkan Ekstensi PostGIS**:
   - Setelah PostgreSQL terinstal, buka terminal PostgreSQL (`psql`) dan jalankan:
     ```sql
     CREATE EXTENSION postgis;
     ```

3. **Konfigurasi Database**:
   - Buat database baru:
     ```sql
     CREATE DATABASE sitscctv_location;
     ```
   - Tambahkan ekstensi PostGIS ke database:
     ```sql
     \c sitscctv_location
     CREATE EXTENSION postgis;
     ```

4. **Konfigurasi Koneksi Database**:
   - Pastikan file `.env` berisi informasi berikut:
     ```
     DB_HOST=localhost
     DB_PORT=25129
     DB_NAME=sitscctv_location
     DB_USER=postgres
     DB_PASSWORD=1234567
     ```

## Cara Menjalankan Project

1. Pastikan seluruh dependensi sudah terinstal.
2. Jalankan migrasi database:
   ```bash
   npx sequelize-cli db:migrate
   ```
3. Jalankan server backend:
   ```bash
   node server
   ```
4. Jalankan client (frontend):
   ```bash
   npm start
   ```
5. Akses API server melalui `http://localhost:5000/api/cctv`.
6. Akses client melalui `http://localhost:3000`.

## Fitur Tambahan

- **Pengujian**:
  Jalankan pengujian unit dengan perintah:
  ```bash
  npm test
  ```

- **Linting**:
  Pastikan kualitas kode dengan menjalankan:
  ```bash
  npm run lint
  ```

---

*Dokumentasi ini dapat dikembangkan sesuai kebutuhan tim atau perubahan pada struktur project.*
