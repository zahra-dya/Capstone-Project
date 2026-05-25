# Dashboard Analisis Performa Siswa - SNBP

Aplikasi dashboard interaktif berbasis Streamlit untuk menganalisis performa akademik siswa, jam belajar, waktu tidur, dan pengaruhnya terhadap nilai ujian. Project ini dibuat untuk memenuhi tugas Capstone Project.

Data yang dianalisis dalam dashboard ini diambil langsung dari repositori GitHub publik agar mempermudah proses deployment dan pengujian secara real-time.

## Fitur Utama

- **Ringkasan Data (KPI)**: Menampilkan total siswa, rata-rata nilai ujian, rata-rata jam belajar, jam tidur, serta jumlah siswa yang berisiko mengalami *burnout*.
- **Grafik Analisis**:
  - Distribusi nilai ujian siswa.
  - Pengaruh jam belajar terhadap nilai (dikelompokkan berdasarkan gender).
  - Hubungan waktu tidur vs nilai ujian (tren regresi).
  - Pengaruh durasi bermain media sosial vs nilai ujian.
  - Deteksi risiko akademik (*Normal*, *Understudy*, *Burnout Risk*).
- **Insight Otomatis**: Rekomendasi atau kesimpulan singkat berdasarkan rata-rata statistik siswa.
- **Tabel Data**: Pratinjau data mentah yang dapat difilter secara langsung melalui sidebar.

## Struktur Project

```text
capstonecl/
├── CAPSTONE/
│   ├── DASHBOARD/
│   │   ├── .streamlit/        # Konfigurasi tema Streamlit
│   │   ├── dashboard.py       # File utama aplikasi Streamlit
│   │   └── requirements.txt   # Library/dependensi Python
│   ├── data_cleaned.csv       # Dataset yang sudah dibersihkan
│   └── student_performance.csv# Dataset asli
└── README.md                  # Dokumentasi project
```

## Cara Menjalankan di Lokal

1. **Persiapan**: Pastikan komputer sudah terinstal Python (versi 3.9 ke atas direkomendasikan).
2. **Install Library**: Buka terminal di folder utama project ini, lalu jalankan perintah berikut:
   ```bash
   pip install -r CAPSTONE/DASHBOARD/requirements.txt
   ```
3. **Jalankan Aplikasi**: Setelah instalasi selesai, jalankan perintah ini:
   ```bash
   streamlit run CAPSTONE/DASHBOARD/dashboard.py
   ```
   Aplikasi otomatis akan terbuka di browser Anda pada alamat `http://localhost:8501`.

## Panduan Deploy ke Streamlit Share

Jika ingin meng-online-kan dashboard ini secara gratis:
1. Push seluruh folder project ini ke akun GitHub Anda.
2. Masuk ke [share.streamlit.io](https://share.streamlit.io) menggunakan akun GitHub Anda.
3. Klik **New app**, lalu isi form sebagai berikut:
   - **Repository**: Nama repositori GitHub Anda.
   - **Branch**: `main` atau `master`.
   - **Main file path**: `CAPSTONE/DASHBOARD/dashboard.py`.
4. Klik **Deploy!** dan tunggu beberapa menit hingga aplikasi selesai di-build.
