# Analisis Dampak Aktivitas Pariwisata dan Pertumbuhan Ekonomi terhadap Volume Penumpang Trans Metro di Bandung
**Kelompok 16**

---
# Analisis Faktor-Faktor yang Memengaruhi Penumpang TransMetro Bandung (2020-2023)

Projek ini bertujuan untuk menganalisis bagaimana variabel ekonomi (**PDRB**) dan tren minat masyarakat (**Google Trends Wisata**) memengaruhi volume penumpang bus TransMetro Bandung menggunakan metode Regresi Linear Berganda.

---

## Kamus Data (Dataset Description)

Tabel berikut menjelaskan rincian kolom yang terdapat dalam dataset `data_final_bersih.csv` beserta satuan dan perannya.

| Nama Kolom | Peran | Satuan | Deskripsi |
| :--- | :--- | :--- | :--- |
| `date` | Indeks | Waktu | Periode data bulanan (Format: YYYY-MM-DD). |
| `Jumlah Penumpang Transmetro (Orang)` | **Variabel Y** | Orang | Total volume penumpang bus TransMetro Bandung. |
| `Rata-Rata Pencarian Terhadap Wisata Kota Bandung (Orang)` | **Variabel X1** | Indeks (0-100) | Data minat pencarian dari Google Trends (Skala Relatif). |
| `PDRB` | **Variabel X2** | Miliar Rp | Produk Domestik Regional Bruto Kota Bandung (Harga Berlaku). |
| `Rata-Rata Penumpang per Koridor` | Pendukung | Orang | Distribusi rata-rata penumpang per rute operasional. |
| `Pertumbuhan PDRB Tahun ke Tahun (%)` | Analisis | Persen (%) | Pertumbuhan ekonomi tahunan (YoY). |
| `Pertumbuhan Penumpang Tahun ke Tahun (%)` | Analisis | Persen (%) | Pertumbuhan jumlah penumpang secara tahunan (YoY). |
| `Pertumbuhan Wisata Tahun ke Tahun (%)` | Analisis | Persen (%) | Pertumbuhan minat pencarian wisata secara tahunan (YoY). |

---

## Model Regresi Linear Berganda (OLS)

Berdasarkan hasil analisis statistik, hubungan antara variabel dirumuskan dalam persamaan berikut:

### 1. Persamaan Regresi
$$\text{Penumpang} = -132.499 + 575,273(X_1) + 0,060(X_2)$$

### 2. Ringkasan Statistik
| Metrik Statistik | Nilai | Interpretasi |
| :--- | :--- | :--- |
| **R-Squared** | 0,488 | Model menjelaskan 48.8% variasi jumlah penumpang. |
| **Adj. R-Squared** | 0.466 | Akurasi model setelah penyesuaian jumlah variabel. |
| **F-Statistic (Sig)** | 0.000 | Model secara simultan berpengaruh signifikan. |
| **P-Value (X1 & X2)** | < 0.05 | Kedua variabel independen signifikan secara parsial. |

---

## Visualisasi Hasil Analisis

Berikut adalah grafik pendukung yang dihasilkan dari pengolahan data:

### 1. Matriks Korelasi (Heatmap)
Digunakan untuk melihat seberapa kuat hubungan antar variabel sebelum dilakukan regresi.
<img width="2783" height="2366" alt="heatmap_korelasi_final(1)" src="https://github.com/user-attachments/assets/ddbb626b-974d-44ed-b9f1-cae2971144b8" />

### 2. Hubungan PDRB vs Penumpang (Scatter Plot)
Menunjukkan tren linear positif: ketika ekonomi (PDRB) naik, mobilitas penumpang cenderung meningkat secara stabil.
<img width="2140" height="1638" alt="plot_pdrb_penumpang" src="https://github.com/user-attachments/assets/a58de3c0-d1df-41d0-a1be-9928cff0e24c" />

### 3. Tren Minat Wisata (Google Trends)
Menunjukkan fluktuasi minat wisata yang sempat anjlok tajam pada masa PPKM 2021.
<img width="2140" height="1638" alt="plot_wisata_penumpang" src="https://github.com/user-attachments/assets/6a78858f-0b99-47de-8af6-c1bfbf8331ce" />


---

## 🚀 Kesimpulan
Model ini membuktikan bahwa **PDRB (Ekonomi)** adalah pendorong yang paling konsisten bagi volume penumpang, sedangkan **Wisata** memberikan dampak yang signifikan namun lebih sensitif terhadap kebijakan mobilitas eksternal.

---
