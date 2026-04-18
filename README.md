# Analisis Kepuasan Pengguna pada Aplikasi SATU SEHAT Mobile dengan Metode Naïve Bayes Berbasis Klasifikasi Teks dan Rating

## 👤 Identitas
* **Nama:** Nicolas Evan
* **NPM:** 2306229626
* **Program Studi:** Statistika (Angkatan 2023)
* **Instansi:** Universitas Indonesia

## 📌 Deskripsi Proyek
Proyek ini bertujuan untuk menganalisis tingkat kepuasan pengguna aplikasi **SATU SEHAT Mobile** melalui klasifikasi teks ulasan berbasis rating. Mengingat volume ulasan yang mencapai lebih dari 100.000 data, proyek ini mengimplementasikan algoritma **Naïve Bayes** dan pembobotan **TF-IDF** untuk memetakan persepsi publik ke dalam kategori sentimen Positif dan Negatif secara otomatis dan terukur.

## 📊 Dataset
Dataset yang digunakan berasal dari Kaggle: [Review Aplikasi SATU SEHAT Mobile](https://www.kaggle.com/datasets/nuricahyono/satusehat).
* **Jumlah Data:** +- 100.000 ulasan.
* **Pelabelan:** * Sentimen Negatif: Rating 1-2.
  * Sentimen Positif: Rating 4-5.
  * Rating 3 dieliminasi untuk menjaga ketajaman klasifikasi.

## 🛠️ Alur Metodologi
1. **Prapemrosesan Teks:** *Case folding*, *cleansing*, *normalization*, *tokenizing*, dan *stopword removal*.
2. **Ekstraksi Fitur:** Menggunakan *Term Frequency-Inverse Document Frequency* (TF-IDF) Vectorizer.
3. **Pemodelan:** Klasifikasi menggunakan algoritma *Naïve Bayes* dengan *Laplace Smoothing* ($\alpha=1$).
4. **Evaluasi:** Mengukur kinerja melalui *Accuracy*, *Precision*, dan *Recall* menggunakan *Confusion Matrix*.

## 📈 Hasil dan Temuan
Model berhasil mencapai performa yang sangat andal untuk data ulasan publik:
* **Akurasi Total:** 82,4%
* **Recall (Sentimen Negatif):** 96% (Sangat sensitif dalam mendeteksi keluhan teknis).
* **Precision (Sentimen Positif):** 94,1%

### Insight Utama (N-Gram):
* **Keluhan Utama:** Terpusat pada isu teknis pasca pembaruan aplikasi, seperti *"tidak bisa login"*, *"sertifikat vaksin"*, dan kendala *"setelah update"*.
* **Apresiasi Utama:** Berfokus pada nilai kemanfaatan aplikasi dengan dominasi frasa *"sangat membantu"* dan *"sangat bermanfaat"*.
