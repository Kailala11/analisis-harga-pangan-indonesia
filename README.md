# 📊 Analisis Harga Pangan Indonesia 2024-2025

Project analisis data harga pangan strategis Indonesia berdasarkan data **PIHPS (Pusat Informasi Harga Pangan Strategis)** Bank Indonesia.

---

##  Tujuan Project

1. **Menganalisis trend** harga 10 komoditas pangan strategis Indonesia
2. **Mengidentifikasi pola** musiman dan volatilitas harga
3. **Memberikan insight** untuk konsumen, pedagang, dan pembuat kebijakan
4. **Visualisasi interaktif** melalui dashboard

---

##  Struktur Project

```
analisis-harga-pangan/
│
├── data/
│   ├── harga_pangan_harian_2024_2025.csv      # Data harian lengkap
│   ├── harga_pangan_bulanan_summary.csv       # Summary bulanan
│   └── statistik_harga_pangan.csv             # Statistik deskriptif
│
├── visualizations/
│   ├── trend_harga_5_komoditas.png            # Trend 5 komoditas utama
│   ├── volatilitas_komoditas.png              # Perbandingan volatilitas
│   ├── korelasi_harga.png                     # Heatmap korelasi
│   └── distribusi_cabai_bulanan.png           # Box plot cabai (2025)
│
├── analysis.py                                 # Script analisis utama
├── dashboard.html                              # Dashboard interaktif (React)
└── README.md                                   # Dokumentasi ini
```

---

##  Dataset

### Sumber Data
- **PIHPS Bank Indonesia** (https://www.bi.go.id/hargapangan)
- **Periode**: Januari 2024 - November 2025
- **Frekuensi**: Data harian
- **Cakupan**: Nasional (82 kota/kabupaten sampel)

### Komoditas yang Dianalisis

| No | Komoditas | Satuan | Volatilitas |
|----|-----------|--------|-------------|
| 1 | Beras Premium | Rp/kg | Rendah (2%) |
| 2 | Beras Medium | Rp/kg | Rendah (2%) |
| 3 | Minyak Goreng Kemasan | Rp/kg | Sedang (8%) |
| 4 | Cabai Merah Besar | Rp/kg | **Tinggi (25%)** |
| 5 | Cabai Rawit Merah | Rp/kg | **Tinggi (22%)** |
| 6 | Bawang Merah | Rp/kg | Tinggi (18%) |
| 7 | Bawang Putih Bonggol | Rp/kg | Sedang (12%) |
| 8 | Telur Ayam Ras | Rp/kg | Sedang (10%) |
| 9 | Daging Ayam Ras | Rp/kg | Sedang (8%) |
| 10 | Gula Pasir Premium | Rp/kg | Rendah (5%) |

---

## 🛠️ Tools & Libraries

### Python Libraries
```python
pandas          # Data manipulation
numpy           # Numerical operations
matplotlib      # Visualizations
seaborn         # Statistical visualizations
```

### Dashboard
- **React** + **Recharts** (visualisasi interaktif)
- **Tailwind CSS** (styling)
- **Lucide React** (icons)

---

##  Cara Menjalankan Project

### 1. Install Dependencies

```bash
# Install Python libraries
pip install pandas numpy matplotlib seaborn
```

### 2. Jalankan Analisis

```bash
python analysis.py
```

**Output:**
- 4 file visualisasi (.png)
- 3 file data CSV
- Statistik dan insight di console

### 3. Lihat Dashboard Interaktif

Buka file `dashboard.html` di browser atau deploy ke:
- **GitHub Pages** (gratis)
- **Netlify** (gratis)
- **Vercel** (gratis)

---

##  Hasil Analisis

### 1. Trend Harga Umum

- **Inflasi pangan**: Rata-rata +5.2% (Jan 2024 - Nov 2025)
- **Kenaikan tertinggi**: Cabai Merah (+23.5%)
- **Paling stabil**: Beras Premium (+3.1%)

### 2. Volatilitas Komoditas

| Kategori | Komoditas | Koefisien Variasi |
|----------|-----------|-------------------|
| **Sangat Volatile** | Cabai Merah | 24.8% |
|  | Cabai Rawit | 21.5% |
|  | Bawang Merah | 17.9% |
| **Stabil** | Beras Premium | 1.8% |
|  | Gula Pasir | 4.3% |

### 3. Pola Musiman

####  Musim Hujan (Des - Feb)
- Cabai: **+35-40%** dari harga normal
- Bawang: **+20-25%** dari harga normal
- Sayuran lain: **+15-20%** dari harga normal

####  Ramadan & Lebaran (Mar - Apr)
- **Semua komoditas**: +15-20%
- Lonjakan tertinggi: Daging Ayam (+25%)
- Demand meningkat 30-40%

#### Panen Raya (Jul - Agu)
- Cabai & Bawang: **-20-30%** (harga terendah)
- **Waktu terbaik** untuk stocking

### 4. Korelasi Antar Komoditas

**Korelasi Tinggi (>0.7):**
- Cabai Merah ↔ Cabai Rawit: **0.89**
- Bawang Merah ↔ Bawang Putih: **0.76**
- Beras Premium ↔ Beras Medium: **0.95**

**Insight**: Komoditas sejenis cenderung bergerak searah karena faktor supply-demand yang sama.

---

##  Business Insights & Rekomendasi

### Untuk KONSUMEN 

1. **Waktu Terbaik Belanja:**
   - Cabai & Bawang: **Juli - Agustus** (panen raya)
   - Daging & Telur: **Oktober - November** (sebelum HBKN)
   - Beras & Gula: **Kapan saja** (harga stabil)

2. **Strategi Hemat:**
   - Stok bahan pokok 2-3 minggu sebelum Ramadan
   - Diversifikasi protein (telur lebih murah dari ayam)
   - Beli cabai kering saat harga tinggi

### Untuk PEDAGANG/RETAILER 

1. **Manajemen Stok:**
   - Tingkatkan stok cabai 30% menjelang musim hujan
   - Buffer stock bawang merah minimal 1 bulan
   - Hedging harga untuk komoditas volatile

2. **Strategi Pricing:**
   - Margin lebih besar pada produk volatile (risiko tinggi)
   - Fokus volume pada produk stabil (beras, gula)
   - Dynamic pricing saat peak season

3. **Timing Pembelian:**
   - Beli cabai/bawang saat panen raya (hemat 20-30%)
   - Kontrak long-term dengan supplier untuk stabilitas

### Untuk PEMERINTAH 

1. **Intervensi Harga:**
   - **Prioritas**: Cabai & Bawang (volatilitas tinggi)
   - Operasi pasar saat lonjakan >30%
   - Buffer stock minimal 10% dari konsumsi nasional

2. **Infrastruktur:**
   - Cold storage di sentra produksi cabai
   - Perbaikan distribusi untuk kurangi disparitas regional
   - Sistem early warning price shock

3. **Kebijakan:**
   - Subsidi pupuk untuk petani cabai/bawang
   - Asuransi harga untuk petani (price floor)
   - Import cabai saat harga >Rp 80.000/kg

---

##  Visualisasi & Analisis

Project ini menghasilkan 4 visualisasi utama yang menunjukkan pola harga pangan Indonesia:

### 1. Trend Harga (Time Series)
Visualisasi trend harga 5 komoditas utama dari Januari 2024 - November 2025.

**Key Insights:**
- Cabai merah menunjukkan fluktuasi ekstrem dengan volatilitas 25%
- Beras sangat stabil (kebijakan subsidi pemerintah efektif)
- Spike harga jelas terlihat saat periode Ramadan & Lebaran 2024-2025
- Pola musiman konsisten: harga tertinggi saat musim hujan, terendah saat panen raya

### 2. Volatilitas Komoditas
Perbandingan tingkat volatilitas (Koefisien Variasi) antar komoditas.

**Key Insights:**
- Cabai merah 12x lebih volatile dibanding beras (24.8% vs 1.8%)
- Top 3 volatile: Cabai merah (24.8%), Cabai rawit (21.5%), Bawang merah (17.9%)
- Hortikultura umumnya lebih volatile dari pangan pokok karena storage life pendek
- Beras & gula paling stabil karena subsidi dan buffer stock pemerintah

### 3. Heatmap Korelasi
Matriks korelasi menunjukkan hubungan pergerakan harga antar komoditas.

**Key Insights:**
- Korelasi tinggi antar komoditas sejenis: Cabai merah ↔ Cabai rawit (0.89)
- Beras premium ↔ Beras medium berkorelasi sangat kuat (0.95)
- Beras tidak berkorelasi dengan sayuran (supply chain & demand driver berbeda)
- Protein (telur & ayam) berkorelasi sedang (0.72)

### 4. Distribusi Harga Bulanan (Cabai)
Box plot menunjukkan distribusi dan variasi harga cabai merah per bulan di 2025.

**Key Insights:**
- Variasi harga terbesar: Desember-Februari (musim hujan mengganggu supply)
- Harga paling stabil: Juli-Agustus (periode panen raya)
- Range harga bisa mencapai 40-50% dalam bulan yang sama
- Best buying period: Juli-Agustus (harga -30% dari rata-rata)

---

**📈 Dashboard Interaktif**

Seluruh visualisasi tersedia dalam bentuk dashboard interaktif di file `dashboard.html`. 
Dashboard menyediakan:
- Filter komoditas & periode waktu
- Real-time metrics (harga, perubahan, volatilitas)
- Perbandingan harga antar provinsi
- Interactive charts dengan tooltip

**Cara akses:**
1. Buka file `dashboard.html` di browser
2. Atau akses online: [Live Dashboard URL]

---

##  Metodologi

### 1. Data Collection
- Survei harian oleh Bank Indonesia
- 164 pasar tradisional di 82 kota
- Harga eceran (pedagang → konsumen)

### 2. Data Processing
- Cleaning: Remove outliers (>3 std dev)
- Aggregation: Daily → Monthly average
- Normalization: Price indexing vs baseline

### 3. Analysis Techniques
- **Descriptive Statistics**: Mean, median, std dev, CV
- **Time Series**: Trend analysis, seasonal decomposition
- **Correlation Analysis**: Pearson correlation matrix
- **Volatility Measurement**: Coefficient of variation

### 4. Visualization
- Line charts: Time series trends
- Bar charts: Comparative analysis
- Heatmaps: Correlation patterns
- Box plots: Distribution analysis

---

##  Limitasi & Future Work

### Limitasi
1. Data merupakan rata-rata nasional (tidak detail regional)
2. Tidak include faktor eksternal (cuaca, kebijakan)
3. Tidak ada data biaya produksi/margin

### Future Improvements
1. **Regional Analysis**: Analisis per provinsi/kota
2. **Predictive Model**: Machine learning untuk forecast harga
3. **Sentiment Analysis**: Twitter/news untuk prediksi shock
4. **Real-time Dashboard**: Auto-update dari API PIHPS
5. **Mobile App**: Notifikasi price alert untuk konsumen

---

##  Author

**[Kaila]**
- Email: [kailahidayatussakinah@gmail.com]
- GitHub: [github.com/Kailala11]

---

##  License & Attribution

- Data source: **PIHPS Bank Indonesia** (https://www.bi.go.id/hargapangan)
- Project ini dibuat untuk portfolio data analyst
- Free to use for educational purposes

---

##  Acknowledgments

- Bank Indonesia untuk data PIHPS
- Badan Pangan Nasional (Bapanas)
- Python & React communities

---

## Contact & Feedback

Punya pertanyaan atau feedback? Hubungi:
- Email: [kailahidayatussakinah@gmail.com]


**⭐ Jangan lupa Star repo ini kalau bermanfaat!**

---

*Last Updated: November 2025*
