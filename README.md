# 📊 Sentiment Analysis of Wuthering Waves Reviews on Google Play Store

Proyek ini bertujuan untuk menganalisis sentimen dari ulasan pengguna terhadap game **Wuthering Waves** yang tersedia di Google Play Store. Proses dimulai dari pengambilan data melalui scraping, pra-pemrosesan teks, hingga klasifikasi sentimen menggunakan pendekatan leksikon berbahasa Indonesia.

---

## 📁 Struktur Proyek

```
Sentiment-Analysis-Wuthering-Waves/
│
├── Scraping.ipynb              # Notebook untuk mengambil data review dari Google Play Store
├── Preprocess.ipynb            # Notebook untuk preprocessing teks dan analisis sentimen
├── wuwa_clean.csv              # Dataset hasil scraping dan pembersihan awal
├── README.md                   # Dokumentasi proyek ini
├── requirements.txt		# Berisi library yang dibutuhkan untuk mengakses project ini
```

---

## 🔧 Tools & Library

- Python 3
- [google-play-scraper](https://github.com/danieliu/play-scraper)
- pandas, numpy
- NLTK
- Sastrawi (stemmer Bahasa Indonesia)
- matplotlib, wordcloud
- Requests, re, string

---

## 🧾 Langkah-langkah Proyek

### 1. 📥 Scraping Data

- Mengambil hingga 1000 ulasan paling relevan dari aplikasi dengan ID `com.kurogame.wutheringwaves.global` (Wuthering Waves).
- Data difilter untuk menghapus kolom tidak penting dan duplikat.

### 2. 🧹 Preprocessing Teks

Dilakukan beberapa tahap pembersihan dan normalisasi data:

- Menghapus tanda baca, angka, link, mention, hashtag, dan whitespace tidak penting.
- Konversi ke huruf kecil.
- Penggantian kata-kata *slang* khas game/chat ke bentuk standar.
- Tokenisasi dan penghapusan *stopwords* Bahasa Indonesia dan Inggris.
- *Stemming* menggunakan library Sastrawi.

### 3. 🏷️ Analisis Sentimen

- Menggunakan pendekatan **lexicon-based** dengan dua kamus kata:
  - `lexicon_positive.csv`
  - `lexicon_negative.csv`
- Klasifikasi sentimen dilakukan menjadi:
  - `positive`
  - `negative`
  - `neutral`

### 4. 📊 Visualisasi

- Pie chart untuk distribusi sentimen.
- Word Cloud untuk melihat kata-kata yang sering muncul:
  - Seluruh data
  - Sentimen positif
  - Sentimen negatif
  - Sentimen netral

---

## 🔍 Hasil Sementara

- Sentimen terbanyak: **Positive** (42%)
- Visualisasi menunjukkan kata-kata yang umum dalam setiap kategori sentimen.

---

## 📝 Catatan

- Analisis ini bersifat leksikal dan belum menggunakan machine learning.
- Kamus leksikon positif/negatif berasal dari sumber publik di GitHub.

---

## 💡 Pengembangan Selanjutnya

- Menggunakan model supervised seperti Naive Bayes, SVM, atau LSTM untuk klasifikasi sentimen.
- Mendeteksi aspek sentimen (aspect-based sentiment analysis).
- Perbandingan ulasan berdasarkan versi aplikasi atau waktu rilis update.

---

## 📚 Referensi

- Google Play Scraper: https://pypi.org/project/google-play-scraper/
- Kamus Sentimen: [angelmetanosaa/dataset](https://github.com/angelmetanosaa/dataset)
- Sastrawi Stemmer: https://github.com/sastrawi/sastrawi

---

## 🧑‍💻 Author

[Lalu Olfata Vedora Zurji](https://github.com/olfataVz)
