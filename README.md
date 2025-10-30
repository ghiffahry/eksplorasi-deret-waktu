# 📈 Eksplorasi Deret Waktu: Analisis Pola, Tren, dan Anomali (2020–2025)

[![Python](https://img.shields.io/badge/Python-3.12%2B-blue)](https://www.python.org/)
[![Data Science](https://img.shields.io/badge/Focus-Time_Series_Analysis-orange)](https://github.com/topics/time-series-analysis)

## 🧭 Deskripsi Proyek

Repositori ini berisi eksplorasi komprehensif terhadap data deret waktu dengan fokus pada **identifikasi pola, tren, anomali, serta analisis dampak kejadian ekonomi** terhadap dinamika pergerakan harga.  
Analisis dilakukan untuk memahami **struktur dan pola data** sebelum tahap pemodelan dilakukan.

> ⚠️ *Catatan:* Seluruh analisis bersifat akademis dan eksploratif, bukan rekomendasi investasi.

---

## 🎯 Tujuan Analisis

- 🔍 Mengidentifikasi pola musiman, tren, dan keragaman efek bulan-hari-tanggal kalender
- 📊 Menganalisis pengaruh fenomena ekonomi melalui pendekatan *event study*
- 📈 Mengeksplorasi volatilitas dan mendeteksi pencilan pada data
- 💡 Memberikan rekomendasi model deret waktu yang sesuai dengan karakteristik data

---

## 📁 Dataset

| Variabel | Jenis Data | Periode | Keterangan |
|-----------|-------------|----------|-------------|
| Harga Penutupan | Numerik | 2020–2025 | Data harian |
| Kejadian Ekonomi | Kategorik | 2020–2025 | Variabel dummy (lockdown, suku bunga, pemilu, dll.) |

**Total Observasi:** ±1.400 titik data (frekuensi hari bisnis)

---

## ⚙️ Metodologi Analisis

### 1. Pengenalan Pola
- Analisis musiman dan tren jangka panjang  
- Identifikasi pola harian, bulanan, dan kalender

### 2. Event Study
- Uji-T dua sampel untuk *event window* (±20 hingga ±50 hari)
- Evaluasi signifikansi statistik (p-value < 0.05)

### 3. Analisis Volatilitas
- Rolling mean & standard deviation (window 22 hari)
- Deteksi *volatility clustering* dan pergeseran tren

### 4. Deteksi Anomali
- Metode Z-score dengan beberapa ambang batas (2.0, 2.5, 3.0)
- Identifikasi nilai ekstrem dan pencilan moderat

### 5. Analisis Interaksi
- Heatmap interaksi hari–bulan  
- Analisis perbedaan variansi antar waktu

---

## 📊 Temuan Utama

### 🌀 Pola & Tren
- Pola musiman terlihat jelas pada awal dan akhir tahun  
- Tidak ada perbedaan mencolok antar hari perdagangan  
- Beberapa tanggal kalender menunjukkan fluktuasi konsisten

### 📉 Dampak Kejadian Ekonomi
- Dampak signifikan ditemukan pada periode lockdown dan perubahan suku bunga  
- Sebagian besar kejadian makro lain menunjukkan efek terbatas secara statistik

### 💥 Volatilitas & Pencilan
- Volatility clustering kuat pada 2020–2021 dan 2024–2025  
- Periode 2022–2023 relatif stabil  
- Pencilan ekstrem hanya muncul saat terjadi *market shock*

---

## 🤖 Rekomendasi Pemodelan

| Kategori | Model yang Disarankan | Keterangan |
|-----------|----------------------|-------------|
| Volatilitas | **GARCH Family** | Menangkap fluktuasi variansi |
| Nonlinear Time Series | **LSTM + Dropout** | Memodelkan pola kompleks dan nonlinier |
| Musiman dengan Variabel Eksternal | **SARIMAX** | Menangkap efek musiman dan kejadian ekonomi |

**Kurang Disarankan:** ARIMA sederhana dan model linear murni (karena data heteroskedastik & nonlinier)

---

## 🚀 Arah Pengembangan Lanjutan

- Implementasi GARCH untuk *volatility forecasting*  
- Eksperimen *LSTM with attention mechanism*  
- Integrasi variabel makroekonomi tambahan  
- Sistem pemantauan real-time untuk deteksi anomali

---

## ⚠️ Disclaimer

Analisis ini dibuat untuk **tujuan edukasi dan riset akademik**.  
Tidak ada bagian dari repositori ini yang dimaksudkan sebagai rekomendasi investasi atau keputusan finansial.

---

📚 **Tags:** `#TimeSeries` `#EDA` `#Volatility` `#AnomalyDetection` `#DataScience`  
