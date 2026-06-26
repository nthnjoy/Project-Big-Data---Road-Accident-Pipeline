[README.md](https://github.com/user-attachments/files/29371864/README.md)
# 🚦 Road Accident Big Data Pipeline

> **PA3 Kelompok 10** — Institut Teknologi Del  
> Mata Kuliah: Big Data

---

## 📌 Tentang Proyek

Repository ini berisi implementasi lengkap pipeline big data untuk menganalisis data kecelakaan lalu lintas di UK (United Kingdom). Pipeline mencakup seluruh alur dari ingest data mentah hingga visualisasi dashboard interaktif, dengan memanfaatkan teknologi big data seperti PySpark dan penyimpanan NoSQL MongoDB Atlas.

---

## 👥 Anggota Kelompok

| Nama | NIM |
|------|-----|
| Whisnu Saragih | 11423045 |
| Nathanael Tampubolon| 11423044 |
| Imel Sinaga | 11423057 |
| Leoni Sibuea | 11423055 |
| Hizkia Sipayung | 11423002 |

> *Lengkapi NIM dan nama anggota sesuai data kelompok.*

---

## 📂 Struktur Repository

```
Project-Big-Data---Road-Accident-Pipeline/
│
├── Big Data.ipynb                  # Notebook utama pipeline
├── Road Accident Data.zip          # Dataset mentah (UK Road Accident)
├── accident_clean.zip              # Dataset setelah preprocessing
├── Jurnal_BigData_Kelompok10.pdf   # Jurnal ilmiah proyek
├── Laporan_BigData_Kelompok10.pdf  # Laporan lengkap proyek
├── PPT_BigData_Kelompok10.pdf      # Slide presentasi
└── README.md
```

---

## 🗄️ Dataset

- **Sumber:** UK Road Accident Data
- **Ukuran:** 307.973 baris × 21 kolom
- **Periode:** 2021 – 2022
- **Fitur utama:** `Accident_Index`, `Accident Date`, `Accident_Severity`, `Latitude`, `Longitude`, `Weather_Conditions`, `Road_Surface_Conditions`, `Vehicle_Type`, `Number_of_Casualties`, dll.

---

## 🔄 Alur Pipeline

```
Raw Data (Google Drive)
        ↓
  Fase 1-3: Mount Drive & Konfigurasi Path
        ↓
  Fase 4: Dataset Profiling (Pandas)
        ↓
  Fase 5-6: Preprocessing & Cleaning (PySpark)
        ↓
  Fase 7-8: Feature Engineering & EDA
        ↓
  Fase 9-10: Clustering & Hotspot Analysis
        ↓
  Fase 11: Upload ke MongoDB Atlas (NoSQL)
        ↓
  Fase 12: Dashboard Streamlit via Ngrok
```

---

## 🛠️ Teknologi yang Digunakan

| Teknologi | Kegunaan |
|-----------|----------|
| **Google Colab** | Environment eksekusi notebook |
| **Google Drive** | Penyimpanan dataset raw & processed |
| **PySpark** | Pemrosesan data berskala besar |
| **Pandas** | Profiling & analisis data |
| **MongoDB Atlas** | Penyimpanan dokumen NoSQL |
| **Streamlit** | Dashboard visualisasi interaktif |
| **Ngrok** | Tunnel publik untuk dashboard |
| **Scikit-learn** | Clustering & machine learning |

---

## 📊 Ringkasan Temuan

- **Total casualties:** 417.883
- **Total vehicles involved:** 563.302
- **Severity distribution:** Slight (85.5%) · Serious (13.2%) · Fatal (1.3%)
- **Top kota:** Birmingham, Leeds, Manchester, Bradford, Westminster
- **Kendaraan terbanyak:** Car (239.794 kasus)

---

## 🚀 Cara Menjalankan

### 1. Clone repository
```bash
git clone https://github.com/nthnjoy/Project-Big-Data---Road-Accident-Pipeline.git
```

### 2. Buka di Google Colab
- Upload atau buka `Big Data.ipynb` di [Google Colab](https://colab.research.google.com/)
- Mount Google Drive kamu

### 3. Siapkan dataset
- Ekstrak `Road Accident Data.zip`
- Letakkan `Road Accident Data.csv` di path:
  ```
  /content/drive/MyDrive/<folder_proyek>/data/raw/
  ```

### 4. Jalankan cell secara berurutan
- Mulai dari Fase 1 (Mount Drive) hingga Fase 12 (Dashboard)

### 5. Akses Dashboard
- Setelah Fase 12 berjalan, salin link **ngrok** yang muncul di output
- Buka link tersebut di browser

---

## 📁 Penyimpanan Data

| Tahap | Lokasi |
|-------|--------|
| Data mentah | `data/raw/Road Accident Data.csv` |
| Data setelah preprocessing | `data/processed/` |
| Output analisis & clustering | `data/output/` |
| NoSQL (dokumen) | MongoDB Atlas — collection `accident_documents` |
| Hasil clustering | MongoDB Atlas — collection `hotspot_cluster_summary`, `hotspot_predictions` |

---

## 📄 Dokumen Pendukung

- 📘 [Jurnal BigData Kelompok 10](./Jurnal_BigData_Kelompok10.pdf)
- 📋 [Laporan BigData Kelompok 10](./Laporan_BigData_Kelompok10.pdf)
- 🖥️ [Slide Presentasi](./PPT_BigData_Kelompok10.pdf)

---

## 📝 Lisensi

Proyek ini dibuat untuk keperluan akademik di **Institut Teknologi Del**.  
© 2024 PA3 Kelompok 10 — All rights reserved.
