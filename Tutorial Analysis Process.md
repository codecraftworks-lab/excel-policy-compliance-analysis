📊 **Policy Compliance Analysis – End-to-End Excel Tutorial**

Dokumen ini adalah tutorial proses analisis data berbasis Excel yang siap dipublikasikan di GitHub (README.md atau Wiki). Fokusnya: bagaimana mengubah data mentah kebijakan/compliance menjadi insight yang bisa dipakai manajemen untuk mengambil keputusan.
Studi kasus menggunakan dataset kaggle yaitu Policy Compliance (4.000 baris, 12 kolom), namun metodologi bersifat generik dan bisa diterapkan ke dataset lain.

🎯 **Tujuan Analisis**

Tujuan utama analisis ini adalah:
1. Mengukur tingkat kepatuhan (compliance rate)
2. Mengidentifikasi area bermasalah (department / kategori / periode)
3. Menemukan akar masalah non‑compliance
4. Menyajikan hasil dalam dashboard Excel yang ringkas & eksekutif

Output akhir:
1. Data bersih (clean dataset)
2. Pivot Table analitis
3. Dashboard Excel siap presentasi

🧠 **Gambaran Proses Analisis (Big Picture)**

Alur kerja analisis mengikuti prinsip profesional data analytics:
1. Data Understanding & Profiling
2. Data Cleansing & Preparation
3. Feature Engineering (kolom turunan)
4. Pivot Table Modeling
5. Visualisasi (Pivot Chart)
6. Dashboard Design
7. Insight & Rekomendasi Bisnis

1️⃣ Data Understanding & Profiling
Apa yang dicek?
● Jumlah baris & kolom
● Tipe data (numeric, teks, tanggal)
● Missing values (%)
● Duplikasi baris
● Nilai unik pada kolom kategorikal

**Kenapa penting?**
● Pivot Table sangat sensitif terhadap:
● Tipe data salah
● Kategori tidak konsisten
● Nilai kosong

Kalau tahap ini dilewati → dashboard akan “cantik tapi bohong”.

**Tools**
● Excel filter
● COUNTBLANK, COUNTA
● Power Query → Column Profile
