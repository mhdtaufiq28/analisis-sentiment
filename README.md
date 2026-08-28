# 📊 Analisis Sentimen: Opini Publik terhadap Kebijakan Relokasi Pulau Rempang

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)

Repositori ini berisi kode sumber dan dokumentasi untuk proyek Tugas Akhir program S1 Teknik Informatika. Penelitian ini berfokus pada pengembangan sistem klasifikasi sentimen otomatis untuk menganalisis opini masyarakat di media sosial X (sebelumnya Twitter) terkait **kebijakan relokasi penduduk Pulau Rempang** sebagai bagian dari Proyek Strategis Nasional (PSN). 

Pendekatan yang digunakan mengkombinasikan metode leksikal (InSet Lexicon) untuk pelabelan otomatis dan *Machine Learning* (Naïve Bayes) untuk klasifikasi.

## 📝 Deskripsi Proyek

Opini publik di media sosial seringkali tidak terstruktur, beragam, dan tersebar luas, sehingga menyulitkan proses klasifikasi secara manual dan objektif. Proyek ini memecahkan masalah tersebut dengan membangun *pipeline* klasifikasi sentimen (Pro dan Kontra) yang efisien dan akurat, yang dapat diterapkan pada isu-isu sosial lainnya.

### Alur Penelitian:
1. **Pengumpulan Data (*Crawling*):** Sebanyak 1.000 tweet relevan ditarik dari media sosial X.
2. **Penyaringan & Prapemrosesan:** Data disaring berdasarkan enam kriteria utama:
   - Penggunaan Bahasa Indonesia.
   - Kebermaknaan konten.
   - Panjang teks minimal 25 kata.
   - Relevansi dengan kata kunci *"Rempang"*.
   - Penghapusan duplikasi data.
   - Penghilangan tweet yang hanya berisi metadata.
3. **Pelabelan Otomatis:** Menggunakan kamus **InSet Lexicon**.
4. **Ekstraksi Fitur Teks:** Menggunakan metode **Term Frequency-Inverse Document Frequency (TF-IDF)**.
5. **Pemodelan Klasifikasi:** Melatih model menggunakan algoritma **Naïve Bayes Classifier**.
6. **Evaluasi:** Menggunakan *Confusion Matrix*, *Classification Report*, dan *10-fold Cross-Validation*.

## 🛠️ Teknologi yang Digunakan

- **Bahasa Pemrograman:** Python 3.x
- **Ekstraksi Fitur:** TF-IDF (Scikit-Learn)
- **Algoritma Machine Learning:** Multinomial Naïve Bayes
- **Lexicon:** InSet Lexicon (Indonesian Sentiment Lexicon)
- **Evaluasi Model:** Scikit-Learn (Cross-validation, Confusion Matrix, Classification Report)

## 📂 Struktur Direktori

```text
📦 analisis-sentiment-rempang
 ┣ 📂 data
 ┃ ┣ 📜 raw_tweets_rempang.csv    # Data hasil crawling (1.000 tweet)
 ┃ ┗ 📜 clean_labeled_data.csv    # Data bersih yang telah dilabeli InSet Lexicon
 ┣ 📂 notebooks
 ┃ ┣ 📜 01_data_crawling_and_filtering.ipynb
 ┃ ┣ 📜 02_lexicon_labeling.ipynb
 ┃ ┣ 📜 03_tfidf_feature_extraction.ipynb
 ┃ ┗ 📜 04_naive_bayes_modeling_evaluation.ipynb
 ┣ 📂 models
 ┃ ┗ 📜 naive_bayes_model.pkl     # Model klasifikasi yang telah dilatih
 ┣ 📜 requirements.txt            # Daftar dependensi library
 ┗ 📜 README.md
```

## 📚 Referensi & Dokumentasi Skripsi

Dokumen naskah Skripsi / Tugas Akhir lengkap dapat diakses pada Repositori UIN Suska Riau:
- 📄 **Tautan Repositori:** https://repository.uin-suska.ac.id/89488/
