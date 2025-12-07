<!-- ================================================================= -->
<!--                     BLUE–TECH PREMIUM README                      -->
<!-- ================================================================= -->

<h1 align="center">
  <img src="https://img.icons8.com/?size=100&id=kD__UGe0Y1x1&format=png&color=007BFF" width="80"/><br>
  <b>Comparative Study of Naive Bayes and KNN for<br>Sentiment Classification Using TF-IDF</b>
</h1>

<p align="center">
  <b>Modern Blue-Tech Edition • NLP • Machine Learning • TF-IDF • Classification</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-007BFF?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/NLP-TF--IDF-005BBB?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Algorithms-Naive%20Bayes%20%7C%20KNN-0A66C2?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Accuracy-97.89%25-1E90FF?style=for-the-badge"/>
</p>

---

## 📘 **Deskripsi Proyek**
Proyek ini bertujuan untuk **menganalisis dan membandingkan performa dua algoritma klasifikasi teks**:

- **Multinomial Naive Bayes**  
- **K-Nearest Neighbor (KNN)**  

Keduanya diuji pada **dataset teks pendidikan** dengan representasi fitur menggunakan **TF-IDF (Term Frequency–Inverse Document Frequency)**.

Dataset berisi dua label utama:

| Label | Keterangan |
|-------|------------|
| **sentiment** | positive, negative |
| **education level** | high, low |

Proyek mengikuti metodologi **CRISP-DM** dari tahap Business Understanding hingga Deployment (Mock-up).

---

## 🧠 **Tujuan Analisis**
1. Mengukur performa Naive Bayes vs KNN pada teks pendidikan.  
2. Menilai efisiensi TF-IDF sebagai metode representasi teks.  
3. Membandingkan akurasi, precision, recall, dan f1-score.  
4. Memberikan insight model mana yang lebih stabil untuk data teks edukasi.  

---

# ======================================================================
# 🔵 **CRISP-DM PIPELINE**
# ======================================================================

---

## 1️⃣ **Business Understanding**
Tujuan utama proyek adalah **mengembangkan sistem klasifikasi sentimen otomatis** yang mampu:

- Menganalisis opini/pendapat terkait konteks pendidikan.
- Mengidentifikasi sentimen positif atau negatif secara akurat.
- Membandingkan performa dua algoritma berbeda pada dataset yang sama.
- Memberikan dasar untuk implementasi sistem analisis sentimen di platform edukasi.

---

## 2️⃣ **Data Understanding**
Dataset memiliki:

- **3.548 baris teks**
- Kolom utama:  
  - `text` – isi kalimat  
  - `education` – kategori high/low  
  - `sentiment` – label positif/negatif  

Analisis awal meliputi:

- Mengecek struktur data  
- Distribusi label (balanced 50% – 50%)  
- Visualisasi pie chart & bar chart  
- Pemeriksaan missing values (0 missing)

---

## 3️⃣ **Data Preparation**
Langkah-langkah pembersihan:

### 🔹 Cleaning Text
- Lowercasing  
- Menghapus angka, URL, simbol, punctuation  
- Menghilangkan extra spaces  

### 🔹 Feature Extraction: TF-IDF
- Mengonversi teks menjadi vektor numerik  
- Menghasilkan ~2.800 fitur per sampel  

### 🔹 Train/Test Split
- 80% training (2.838 data)  
- 20% testing (710 data)

---

## 4️⃣ **Modeling**
Dua algoritma digunakan:

### 🔵 **A. Multinomial Naive Bayes**
- Algoritma probabilistik  
- Cocok untuk TF-IDF + data teks  
- Cepat & akurat

### 🔵 **B. K-Nearest Neighbor (KNN)**  
- Menggunakan parameter: **k = 5**  
- Distance metric: **Euclidean**  
- Mencari tetangga terdekat berdasarkan representasi TF-IDF

---

## 5️⃣ **Evaluation**
Model dievaluasi menggunakan:

- **Accuracy**
- **Precision**
- **Recall**
- **F1-Score**
- **Confusion Matrix**
- **Hyperparameter Exploration (untuk KNN)**

📌 **Hasil Evaluasi Utama:**

| Model | Akurasi | Catatan |
|--------|---------|---------|
| **Naive Bayes** | ⭐ **97.89%** | Lebih stabil, sangat cocok untuk teks |
| **KNN (k=5)** | 94.79% | Lebih lambat & kurang optimal pada vector high-dimensional |

### 📊 *Visualisasi yang disertakan dalam notebook:*
- Dual confusion matrix (raw & normalized)  
- Grafik akurasi KNN vs nilai k  
- Perbandingan akurasi NB vs KNN  

---

## 6️⃣ **Deployment (Mock-Up)**
Sebuah fungsi prediksi dibuat:
prediksi_sentimen("The education system needs more improvement.")

Output:
- Teks asli  
- Teks yang sudah dibersihkan  
- Prediksi Naive Bayes  
- Prediksi KNN  

Contoh hasil:

Prediksi NB : negative
Prediksi KNN : negative


Rencana implementasi ke depan:

- API (FastAPI/Flask)  
- Simple Web Interface  
- Integrasi ke aplikasi pendidikan  

---

# ======================================================================
# 📦 **Struktur Folder**
# ======================================================================

📁 Comparative_Study_of_Naive_Bayes_and_KNN_for_Sentiment_Classification_Using_TF
│
├── 📁 data
│ ├── education_sentiment.csv
│ └── hasil_prediksi_education_sentiment.csv
│
├── 📁 notebooks
│ └── processing.ipynb
│
├── 📁 doc
│ ├── Comparative Study of Naive Bayes and KNN for Sentiment Classification on Educational Text Dataset Using TF.docx
│ └── MUHAMMAD RIZAL HARIS - LK Perancangan Project
│
└── README.md


---

# ======================================================================
# 🧩 **Teknologi yang Digunakan**
# ======================================================================

| Teknologi | Keterangan |
|-----------|------------|
| **Python 3.10+** | Bahasa utama |
| **Pandas** | Data processing |
| **NumPy** | Numerik |
| **Matplotlib / Seaborn** | Visualisasi |
| **Scikit-Learn** | TF-IDF, Naive Bayes, KNN, evaluasi |
| **Jupyter Notebook** | Development |

---

# ======================================================================
# 🏁 **Kesimpulan**
# ======================================================================

1. **Naive Bayes secara konsisten menghasilkan akurasi tertinggi (97.89%)** dibandingkan KNN.  
2. NB lebih cocok untuk dataset teks karena sifatnya yang probabilistik dan efisien pada data sparse TF-IDF.  
3. KNN kurang efektif pada high-dimensional vectors karena overhead komputasi & sensitivitas terhadap noise.  
4. Pipeline CRISP-DM yang diterapkan berhasil menghasilkan alur kerja end-to-end yang rapi dan sistematis.  
5. Fungsi prediksi akhir memungkinkan model digunakan untuk input teks baru.  

📌 **Kesimpulan akhir:**  
> **Naive Bayes adalah algoritma terbaik untuk klasifikasi sentimen pada dataset teks pendidikan berbasis TF-IDF dalam eksperimen ini.**

---

# 🙌 **Kontribusi & Pengembangan ke Depan**
- Penambahan model SVM atau Logistic Regression  
- Implementasi real-time API  
- Dashboard visualisasi sentimen  
- Finetuning hyperparameter yang lebih dalam  

---

<p align="center">
  Made with Me Gonrong Scopus 🤙🤪💙 
</p>


