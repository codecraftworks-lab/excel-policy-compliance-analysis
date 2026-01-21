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
1. Jumlah baris & kolom
2. Tipe data (numeric, teks, tanggal)
3. Missing values (%)
4. Duplikasi baris
5. Nilai unik pada kolom kategorikal

Kenapa penting?
Pivot Table sangat sensitif terhadap:
1. Tipe data salah
2. Kategori tidak konsisten
3. Nilai kosong

Kalau tahap ini dilewati → dashboard akan “cantik tapi bohong”.

Tools
1. Excel filter
2. COUNTBLANK, COUNTA
3. Power Query → Column Profile

2️⃣ Data Cleansing & Preparation
Masalah data yang umum
1. Spasi berlebih (" HR ", "HR")
2. Kapitalisasi tidak konsisten
3. Missing values di kolom penting
4. Angka disimpan sebagai teks
5. Tanggal tidak terbaca Excel

Teknik yang digunakan

A. Power Query (direkomendasikan)
   1. Trim & clean text
   2. Change data type
   3. Replace values
   4. Remove error

B. Rumus Excel (alternatif cepat)
   1. TRIM() → hapus spasi
   2. PROPER() → standarisasi teks
   3. NUMBERVALUE() → teks ke angka
   4. IFERROR() → handle error

Prinsip penting
Jangan menghapus data sembarangan. Jika ragu, buat kategori Unknown.

3️⃣ Feature Engineering (Kolom Turunan)

Kolom turunan mempercepat analisis dan dashboard.
Contoh kolom yang dibuat:
1. Year
2. Month
3. YearMonth
4. Is_Compliant (1 = compliant, 0 = non‑compliant)
5. Compliance_Flag (teks)

Contoh rumus: =IF([@Status]="Compliant",1,0)

4️⃣ **Pivot Table Modeling**
**Pivot 1 – Compliance Overview**
Tujuan: melihat distribusi compliant vs non‑compliant
- Rows: Department / Policy Category
- Columns: Compliance Status
- Values: Count of Record

**Pivot 2 – Trend Analysis**
Tujuan: melihat perubahan compliance dari waktu ke waktu
- Rows: YearMonth
- Values: Compliance Rate

**Pivot 3 – Root Cause (Pareto)**
Tujuan: fokus pada penyebab utama non‑compliance
- Rows: Reason Category
- Values: Count
- Sort: Descending
