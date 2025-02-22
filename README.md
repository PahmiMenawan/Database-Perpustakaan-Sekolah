# Database Perpustakaan Sekolah

Repository ini berisi skema database untuk sistem perpustakaan sekolah yang mencakup tabel-tabel utama, prosedur, dan trigger untuk mengelola data buku, siswa, serta peminjaman.

## 📌 Fitur Database
- **Tabel Buku** (`buku`): Menyimpan data buku yang tersedia di perpustakaan.
- **Tabel Siswa** (`siswa`): Menyimpan data siswa yang dapat meminjam buku.
- **Tabel Peminjaman** (`peminjaman`): Menyimpan riwayat peminjaman buku.
- **Stored Procedure**: Memudahkan pengelolaan peminjaman dan pengembalian buku.
- **Trigger**: Mengotomatiskan pembaruan data terkait peminjaman dan stok buku.

## 📂 Struktur Tabel
### 1️⃣ Tabel `buku`
| Kolom | Tipe Data | Deskripsi |
|-------|----------|-----------|
| idBuku | INT (Primary Key auto_increment) | ID unik untuk setiap buku |
| judulBuku | VARCHAR(50) | Judul buku |
| penulis | VARCHAR(50) | Nama penulis |
| kategori | VARCHAR(50) | Kategori Buku |
| stok | INT | Jumlah buku tersedia |

### 2️⃣ Tabel `siswa`
| Kolom | Tipe Data | Deskripsi |
|-------|----------|-----------|
| idSiswa | INT (Primary Key auto_increment) | ID unik siswa |
| nama | VARCHAR(50) | Nama siswa |
| kelas | VARCHAR(20) | Kelas siswa |

### 3️⃣ Tabel `peminjaman`
| Kolom | Tipe Data | Deskripsi |
|-------|----------|-----------|
| idPeminjaman | INT (Primary Key auto_increment) | ID unik peminjaman |
| idSiswa | INT (Foreign Key) | ID siswa yang meminjam |
| idBuku | INT (Foreign Key) | ID buku yang dipinjam |
| tglPinjam | DATE | Tanggal peminjaman |
| tglKembali | DATE | Tanggal pengembalian |
| statusPinjam | VARCHAR(50) | Status buku |


## 🚀 Instalasi & Penggunaan
1. Clone repository ini:
   ```bash
   git clone https://github.com/PahmiMenawan/Database-Perpustakaan-Sekolah.git
   ```
2. Import database ke MySQL:
   ```bash
   mysql -u root -p < db_perpus.sql
   ```
3. Gunakan database:
   ```sql
   USE db_perpus;
   ```
4. Jalankan query sesuai kebutuhan.

## 📜 Lisensi
Database ini dibuat untuk keperluan edukasi dan dapat digunakan secara bebas.

---
✍️ Dibuat oleh **Zulfahhmi Rizki Aulia**

