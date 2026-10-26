# 📊 PPD Kota Tinggi Student Health Surveillance & BMI Analysis (SQL)

## 📌 Project Overview
Projek ini menganalisis rekod kecergasan fizikal dan taburan Indeks Jisim Badan (BMI) melibatkan **12,000+ pelajar sekolah** merentasi lebih 70 buah institusi pendidikan di bawah seliaan **Pejabat Pendidikan Daerah (PPD) Kota Tinggi, Johor**. 

Objektif utama analisis ini adalah untuk mengukur prevalens isu berat badan (obesiti dan kekurangan berat badan) serta membina model keutamaan sekolah berisiko bagi menyokong perancangan intervensi kesihatan murid.

---

## 🛠️ Tech Stack & Methodology
- **Language / Engine:** SQLite / Standard SQL
- **Dataset:** 12,296 rekod murid (SEGAK / BMI Kementerian Pendidikan Malaysia)
- **Key SQL Concepts:**
  - Multi-condition Aggregations (`CASE WHEN`, `COUNT`, `SUM`)
  - Subqueries & Relative Percentages
  - Window Functions (`DENSE_RANK() OVER`)
  - Common Table Expressions (CTEs)
  - Data Filtering & Segmentation (`HAVING`, `PARTITION`)

---

## 🔍 Key Findings & SQL Highlights

### 1. Taburan Keseluruhan Status BMI Murid
- **70.02%** murid berada dalam kategori **Berat Badan Normal**.
- Sebanyak **22.32%** murid tergolong dalam kategori berisiko tinggi (**11.74% Obes** dan **10.58% Berlebihan Berat Badan**).
- **7.61%** murid diklasifikasikan sebagai **Kurus**.

### 2. Jurang Prevalens Obesiti Mengikut Jantina
- Murid lelaki menunjukkan peratusan obesiti yang lebih ketara (**13.91%**) berbanding murid perempuan (**9.28%**).
- Trend ini membantu pegawai merangka program aktiviti fizikal berfokus mengikut jantina di peringkat kokurikulum.

### 3. Analisis Sosio-Geografi (Bandar vs Luar Bandar)
- Murid di sekolah kawasan luar bandar dan bandar dinilai secara berasingan untuk mengenal pasti jurang akses aktiviti sihat dan corak pemakanan.

### 4. Senarai Sekolah Berkeutamaan Tinggi (Top 5 Priority)
Menggunakan fungsi `DENSE_RANK()`, 5 buah sekolah dengan nisbah obesiti melebihi 20% berjaya disenarai-pendek untuk lawatan program intervensi khas (ditapis bagi sekolah $\ge 50$ murid).

---

## 📁 Repository Structure
```text
├── bmi_ppd_kotatinggi.csv    # Anonymized dataset murid PPD Kota Tinggi
├── analysis_queries.sql      # Skrip kueri SQL analitik
└── README.md                 # Dokumentasi & rumusan hasil analisis
