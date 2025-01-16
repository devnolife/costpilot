
# **CostPilot**

**CostPilot** adalah aplikasi berbasis web untuk merencanakan dan mengelola proyek, dengan kemampuan untuk menghitung estimasi biaya dan waktu secara otomatis berdasarkan deskripsi proyek. Aplikasi ini juga menyediakan fitur pembuatan **Business Requirements Document (BRD)** yang otomatis, yang bisa langsung diunduh oleh pengguna. Proyek ini dibangun menggunakan **Next.js** dan **Schadan UI**.

## **Fitur Utama:**

- **Login Pengguna & Admin:**
  - Login untuk pengguna biasa dan admin dengan kontrol akses berbasis peran.
  
- **Pembuatan BRD Otomatis:**
  - Pengguna dapat memasukkan deskripsi proyek, dan aplikasi otomatis menghasilkan BRD lengkap dengan estimasi biaya dan waktu.
  
- **Manajemen Proyek:**
  - Pengguna dapat memilih proyek yang ingin dikerjakan, serta melihat riwayat proyek mereka.
  
- **Pengelolaan Pengguna dan Proyek untuk Admin:**
  - Admin dapat mengelola pengguna, proyek, serta mengelola BRD yang dihasilkan.

- **Estimasi Otomatis:**  
  - Aplikasi secara otomatis menghitung estimasi biaya dan durasi proyek berdasarkan input deskripsi proyek.

## **Prasyarat:**
Untuk menjalankan aplikasi ini, Anda memerlukan:
- **Node.js** (versi 14 atau lebih tinggi)
- **npm** atau **yarn** (untuk manajemen dependensi)
- **PostgreSQL** (untuk database)
- **Docker** (opsional, untuk penggunaan produksi)

## **Instalasi:**

1. **Clone Repositori:**
   ```bash
   git clone https://github.com/devnolife/costpilot.git
   cd costpilot
   ```

2. **Instalasi Dependensi:**
   Pastikan Anda berada di dalam direktori proyek dan instal semua dependensi yang diperlukan.
   ```bash
   npm install
   # atau menggunakan yarn
   yarn install
   ```

3. **Konfigurasi Database:**
   - Pastikan Anda sudah mengonfigurasi PostgreSQL dan membuat database yang sesuai.
   - Sesuaikan file konfigurasi database pada **.env**.
   
   Contoh:
   ```
   DATABASE_URL=postgresql://username:password@localhost:5432/project_planner_estimator
   ```

4. **Menjalankan Aplikasi dalam Mode Pengembangan:**
   ```bash
   npm run dev
   # atau menggunakan yarn
   yarn dev
   ```

   Aplikasi akan berjalan di [http://localhost:3000](http://localhost:3000).

## **Struktur Proyek:**

```
/project-planner-estimator
├── /components         # Komponen UI untuk aplikasi
├── /pages              # Halaman aplikasi (Next.js routing)
├── /public             # Gambar dan aset statis
├── /styles             # Gaya CSS dan tema untuk UI
├── /utils              # Utilitas tambahan (seperti helper fungsi)
├── .env                # File konfigurasi lingkungan
├── next.config.js      # Pengaturan untuk Next.js
├── package.json        # Dependensi dan skrip npm
└── README.md           # Dokumentasi proyek
```

## **Penggunaan:**

### **Halaman Utama (Landing Page):**
Pada halaman utama, pengguna dapat melihat penjelasan singkat tentang aplikasi, serta memilih untuk mendaftar atau login. Pengguna dapat memilih untuk membuat BRD otomatis dengan memasukkan deskripsi proyek.

### **Login dan Pendaftaran:**
Pengguna dan admin dapat mendaftar atau login menggunakan email dan password. Admin akan memiliki akses tambahan untuk mengelola pengguna dan proyek.

### **Halaman Profil Pengguna:**
Setelah login, pengguna dapat mengisi data diri mereka dan memilih proyek yang akan mereka kerjakan. Pengguna juga dapat melihat riwayat proyek yang telah mereka kerjakan.

### **Proyek dan Estimasi:**
Pengguna dapat memilih proyek yang akan mereka kerjakan dan mengisi deskripsi proyek. Aplikasi akan otomatis menghitung estimasi biaya dan waktu berdasarkan deskripsi tersebut.

### **Halaman Admin:**
Admin dapat mengelola semua pengguna dan proyek. Admin dapat melihat daftar pengguna, mengubah status pengguna, serta mengelola proyek yang ada.

### **Pembuatan BRD Otomatis:**
Setelah memasukkan deskripsi proyek, aplikasi akan menghasilkan **BRD (Business Requirements Document)** secara otomatis, yang mencakup rincian biaya, waktu, dan sumber daya yang dibutuhkan.

---

## **Pengujian:**

Untuk melakukan pengujian aplikasi, Anda dapat menjalankan skrip pengujian yang sudah dikonfigurasi:

```bash
npm run test
# atau menggunakan yarn
yarn test
```

## **Pengaturan Lingkungan:**

### **Variabel Lingkungan:**
Di file `.env`, Anda dapat menambahkan variabel lingkungan yang dibutuhkan:

- `DATABASE_URL` — URL untuk database PostgreSQL.
- `NEXT_PUBLIC_API_URL` — URL untuk API eksternal (jika ada).
  
Contoh:
```
DATABASE_URL=postgresql://user:password@localhost:5432/project_planner_estimator
NEXT_PUBLIC_API_URL=https://api.example.com
```

## **Teknologi yang Digunakan:**
- **Next.js** — Framework React untuk aplikasi server-side rendered (SSR).
- **Schadan UI** — UI toolkit untuk membangun antarmuka pengguna yang interaktif dan responsif.
- **PostgreSQL** — Database yang digunakan untuk menyimpan data pengguna, proyek, dan BRD.
- **Docker (Opsional)** — Untuk membuat aplikasi berjalan di lingkungan produksi.

## **Kontribusi:**
Jika Anda ingin berkontribusi pada proyek ini, silakan ikuti langkah-langkah berikut:
1. Fork repositori ini.
2. Buat cabang baru (`git checkout -b feature-xyz`).
3. Lakukan perubahan dan komit (`git commit -am 'Add new feature'`).
4. Push cabang ke repositori Anda (`git push origin feature-xyz`).
5. Buat pull request ke repositori utama.

## **Lisensi:**
Proyek ini dilisensikan di bawah **MIT License**.
