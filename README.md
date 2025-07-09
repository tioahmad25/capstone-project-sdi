# 📊 Capstone Project SDI – Automatic Machine Health Summary Generator using IBM Granite LLM

Selamat datang di repositori proyek Capstone saya untuk program **Student Development Initiative (SDI)** hasil kolaborasi **Hacktiv8** dan **IBM SkillsBuild**. Proyek ini menggabungkan data sensor industri dan kecerdasan buatan (AI) berbasis Large Language Model (LLM) untuk menghasilkan **laporan teknis otomatis** terkait kondisi mesin dalam tiap shift kerja.

---

## 🧠 Deskripsi Proyek

Proyek ini bertujuan untuk:
- Melakukan **analisis data sensor industri** secara otomatis
- Membuat **ringkasan laporan harian** tiap shift menggunakan **LLM IBM Granite**
- Menemukan **insight penting**, seperti anomali, fluktuasi suhu, dan saran perawatan mesin
- Menyediakan sistem **pendukung keputusan** bagi teknisi industri

---

## 🏭 Dataset

Dataset yang digunakan merupakan data sensor dari lingkungan industri otomasi, yang mencatat data suhu, tekanan, dan getaran secara berkala. Terdiri dari 1000 entri dengan fitur sebagai berikut:

| Kolom                       | Deskripsi                                                                 |
|-----------------------------|---------------------------------------------------------------------------|
| `Temperature (°C)`          | Suhu mesin dalam derajat Celcius                                          |
| `Pressure (bar)`            | Tekanan sistem dalam satuan bar                                           |
| `Vibration (mm/s)`          | Getaran dalam milimeter per detik                                         |
| `RMS Vibration`             | Nilai RMS dari getaran                                                    |
| `Mean Temp`                 | Rata-rata suhu                                                            |
| `Fault Label`               | Klasifikasi kondisi mesin (0: No Fault, 1: Bearing Fault, 2: Overheating) |

🔗 Sumber: [Industrial IoT Fault Detection Dataset – Kaggle](https://www.kaggle.com/datasets/ziya07/industrial-iot-fault-detection-dataset)

---

## 🛠️ Teknologi yang Digunakan

- **Python + Pandas**: Pembersihan dan manipulasi data
- **Matplotlib & Seaborn**: Visualisasi data dan insight
- **IBM Granite via Replicate API**: Text generation LLM
- **Langchain**: Wrapper model Granite
- **Google Colab**: Eksekusi pipeline analisis
- **GitHub**: Dokumentasi dan penyimpanan file proyek

---

## ⚙️ Alur Proses Analisis

1. **Data Preprocessing**  
   Dataset diubah ke format per shift (per jam)

2. **Prompt Engineering**  
   Setiap shift dibentuk menjadi prompt untuk LLM

3. **Summarization dengan IBM Granite**  
   Menggunakan model `granite-3.3-8b-instruct` untuk menyusun laporan teknisi

4. **Evaluation & Visualisasi**  
   Insight dari hasil LLM divisualisasikan untuk memudahkan identifikasi masalah

---

## 🖥️ Notebook Utama

File utama proyek ini:

📄 [`Capstone_Project_SDI_(1).ipynb`](./Capstone_Project_SDI_(1).ipynb)

Notebook ini mencakup seluruh proses:
- Pembersihan data
- Prompt builder
- Pemanggilan model Granite
- Evaluasi dan grafik insight

---

## 📊 Hasil Visualisasi

| Visualisasi                                | Deskripsi                                              |
|------------------------------------------- |--------------------------------------------------------|
| `LLM_Temperature_Overlay.png`              | Tren suhu dengan garis vertikal insight LLM            |
| `LLM_Insight_BarChart.png`                 | Jumlah insight: anomali, rekomendasi, dan peringatan   |
| `LLM_Insight_Timeline.png`                 | Waktu insight muncul dalam timeline shift              |

---

## 📦 File Penting

| File                                       | Fungsi                                        |
|--------------------------------------------|-----------------------------------------------|
| `industrial_fault_detection_data_1000.csv` | Dataset mentah sensor industri                |
| `Shift_Report_AI_Summary.csv`              | Ringkasan hasil Granite per shift             |
| `Capstone_Project_SDI_(1).ipynb`           | Notebook utama seluruh proses analisis        |
| `README.md`                                | Dokumentasi proyek                            |

---

## ✨ Insight Utama

- Ditemukan lebih dari **10 shift** yang mengandung insight penting seperti:
  - Anomali suhu ekstrem
  - Rekomendasi inspeksi suhu pendingin
  - Fluktuasi getaran tak wajar
- LLM mampu menghasilkan laporan profesional teknisi dalam hitungan detik
- Proyek ini membuktikan bahwa AI dapat menjadi **asisten pemeliharaan cerdas** di industri manufaktur

---

## 🤝 Kontributor

👨‍💻 **Tio Ahmad Purnomoaji**  
Program Studi Teknik Elektro, Universitas Sebelas Maret  
Peserta SDI Hacktiv8 x IBM SkillsBuild – Wave 3, Batch 5  
📧 Email: tioahmad88@gmail.com  

---

## 📬 Lisensi

Proyek ini dikembangkan untuk tujuan edukatif dalam program Student Development Initiative oleh Hacktiv8 dan IBM. Dataset dan model AI digunakan sesuai dengan lisensi terbuka masing-masing penyedia.

---

Terima kasih telah mengunjungi repositori ini 🙏  
Jika kamu menyukai proyek ini, silakan ⭐️ dan fork!
