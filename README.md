# Comparative Study of Naive Bayes and KNN for Sentiment Classification on Educational Text Dataset Using TF-IDF

## 1. Deskripsi Proyek

Proyek ini bertujuan untuk menganalisis dan membandingkan performa dua algoritma klasifikasi teks, yaitu **Multinomial Naive Bayes** dan **K-Nearest Neighbor (KNN)**, dalam melakukan *sentiment analysis* pada teks bertema pendidikan. Representasi teks menggunakan pendekatan **TF-IDF (Term Frequency–Inverse Document Frequency)**.

Eksperimen disusun mengikuti metodologi **CRISP-DM** yang meliputi tahap:
**Business Understanding, Data Understanding, Data Preparation, Modeling, Evaluation, dan Deployment (mock-up fungsi prediksi).**

---

## 2. Tujuan Proyek

1. Mengembangkan pipeline analisis sentimen lengkap untuk teks pendidikan.
2. Membandingkan performa model **Naive Bayes** dan **KNN** pada dataset yang sama.
3. Menghasilkan baseline model yang dapat digunakan sebagai dasar pengembangan sistem analitik pendidikan.
4. Menyusun fungsi prediksi yang dapat digunakan untuk mengklasifikasikan sentimen pada teks baru.

---

## 3. Struktur Proyek

Struktur folder yang digunakan:

```text
project/
│
├── data/
│   ├── education_sentiment.csv
│   └── hasil_prediksi_education_sentiment.csv
│
├── notebooks/
│   └── processing.ipynb
│
└── doc/
    ├── Comparative Study of Naive Bayes and KNN for Sentiment Classification.docx
    └── Lembar Kerja Mahasiswa (LKM).docx
