# Laporan Proyek Machine Learning - Daffa Rayhan Riadi

## Project Overview

Pada bagian ini, kamu perlu menuliskan latar belakang yang relevan dengan proyek yang diangkat.

Kehamilan merupakan suatu proses kehidupan yang dialami oleh wanita, menurut Federasi Obstetri Ginekologi Internasional. Kehamilan didefinisikan sebagai fertilisasi atau penyatuan dari spermatozoa dan ovum, dilanjutkan dengan nidasi atau implantasi. Lama kehamilan dibagi menjadi tiga triwulan yaitu 280 hari (40 minggu atau 9 bulan 7 hari)”.

Angka Kematian Ibu menjadi indikator pembangunan kesehatan dan indikator pemenuhan hak reproduksi perempuan serta kualitas pemanfaatan kesehatan secara umum.

**Rubrik/Kriteria Tambahan (Opsional)**:
- Jelaskan mengapa proyek ini penting untuk diselesaikan.
- Menyertakan hasil riset terkait atau referensi. Referensi yang diberikan harus berasal dari sumber yang kredibel dan author yang jelas.
  
  Format Referensi: [Judul Referensi](https://scholar.google.com/) 

## Business Understanding
### Problem Statements
Berdasarkan pada latar belakang diatas, permasalahan yang dapat diselesaikan pada proyek ini adalah sebagai berikut: 
Menjelaskan pernyataan masalah:
- Bagaimana cara menganalisa data kesehatan janin?
- Bagaimana cara memproses data kesehatan janin sehingga dapat di latih dengan baik oleh model?
- Bagaiana cara membangun model machine learning yang dapat memprediksi kesehatan janin dengan baik?

### Goals

Tujuan dibuatnya proyek ini adalah sebagai berikut:
- Mendapatkan analisa yang cukup untuk memahami data kesehatan janin.
- melakukan persiapan pada data agar dapat dengan mudah dipahami dengan baik oleh model Machine Learning yang dibuat.
- Dapat memprediksi kesehatan janin dengan akurat.

## Solution statements
Solusi yang dapat diterapkan agar goals diatas terpenuhi adalah sebagai berikut:
- Melakukan analisa pada data untuk dapat memahami data yang ada dengan menerapkan teknik visualisasi data. Analisa yang dapat dilakukan yaitu, antara lain:
  - Menangani missing value pada data.
  - Memeriksa korelasi antar data penting untuk memahami hubungan data target dan data fitur.
- Melakukan pemrosesan pada data seperti:
  - Mengatasi outlier pada data dengan menerapkan IQR Method.
  - Normalisasi data pada fitur numerik.
- Membangun model yang dapat memprediksi bilangan kontinu sesuai dengan permasalahan yang ingin diselesaikan. Beberapa algoritma yang akan digunakan pada model regresi proyek ini yaitu, sebagai berikut:
  - Support Vector Machine
  - K-Nearest Neighbours
  - Random Forest
- Menerapkan teknik Grid Search untuk mendapatkan parameter-parameter dengan performa terbaik pada masing-masing model.

## Data Understanding
Sesuai dengan **Domain Proyek** diatas, saya mengambil dataset mengenai kesehatan janin. Pada kali ini saya menggunakan dataset yang saya ambil dari kaggle. Dataset ini memiliki 2126 baris sample data dan 22 kolom yang dimana 1 kolom akan menjadi target saya kali ini bernama **fetal_health**.  kolom **fetal_health** ini memiliki 3 kelas didalamnya yaitu normal, suspect dan pathologi. Dataset tersebut dapat di untuh di website kaggle: [Fetal Health Classification](https://www.kaggle.com/datasets/andrewmvd/fetal-health-classification). 

Variabel-variabel pada Fetal Health Classification dataset adalah sebagai berikut:
- **baseline value**: Detak Jantung Janin Dasar
- **accelerations**: Jumlah percepatan per detik
- **fetal_movemen**t: Jumlah gerakan janin per detik
- **uterine_contractions**: Jumlah kontraksi uterus per detik
- **light_decelerations**: Jumlah Deselerasi Ringan per detik
- **severe_decelerations**: Jumlah Deselerasi Parah per detik
- **prolongued_decelerations**: Jumlah Deselerasi Berkepanjangan per detik
- **abnormal_short_term_variability**: Persentase waktu dengan variabilitas jangka pendek yang abnormal
- **mean_value_of_short_term_variability**: Nilai rata-rata variabilitas jangka pendek
- **percentage_of_time_with_abnormal_long_term_variability**: Persentase waktu dengan variabilitas jangka panjang yang abnormal
- **mean_value_of_long_term_variability**: Nilai rata-rata variabilitas jangka panjang
- **histogram_width**: Lebar histogram dibuat menggunakan semua nilai dari record
- **histogram_min**: Nilai minimum histogram
- **histogram_max**: Nilai maksimum histogram
- **histogram_number_of_peaks**: Jumlah puncak dalam histogram ujian
- **histogram_number_of_zeroes**: Jumlah nol dalam histogram ujian
- **histogram_mode**: Mode Histogram
- **histogram_mean**: Rata-Rata Histogram
- **histogram_median**: Median Histogram
- **histogram_variance**: Variasi histogram
- **histogram_tendency**: Tren histogram
- **fetal_health: Fetal health**: 1 - Normal 2 - Suspect 3 - Pathological

**Rubrik/Kriteria Tambahan (Opsional)**:
- Melakukan beberapa tahapan yang diperlukan untuk memahami data, contohnya teknik visualisasi data beserta insight atau exploratory data analysis.

## Data Preparation
Berikut merupakan tahapan dalam mempersiapkan data untuk keperluan pelatihan model:

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan proses data preparation yang dilakukan
- Menjelaskan alasan mengapa diperlukan tahapan data preparation tersebut.

## Modeling
Tahapan ini membahas mengenai model sisten rekomendasi yang Anda buat untuk menyelesaikan permasalahan. Sajikan top-N recommendation sebagai output.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menyajikan dua solusi rekomendasi dengan algoritma yang berbeda.
- Menjelaskan kelebihan dan kekurangan dari solusi/pendekatan yang dipilih.

## Evaluation
Pada bagian ini Anda perlu menyebutkan metrik evaluasi yang digunakan. Kemudian, jelaskan hasil proyek berdasarkan metrik evaluasi tersebut.

Ingatlah, metrik evaluasi yang digunakan harus sesuai dengan konteks data, problem statement, dan solusi yang diinginkan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan formula metrik dan bagaimana metrik tersebut bekerja.

**---Ini adalah bagian akhir laporan---**

_Catatan:_
- _Anda dapat menambahkan gambar, kode, atau tabel ke dalam laporan jika diperlukan. Temukan caranya pada contoh dokumen markdown di situs editor [Dillinger](https://dillinger.io/), [Github Guides: Mastering markdown](https://guides.github.com/features/mastering-markdown/), atau sumber lain di internet. Semangat!_
- Jika terdapat penjelasan yang harus menyertakan code snippet, tuliskan dengan sewajarnya. Tidak perlu menuliskan keseluruhan kode project, cukup bagian yang ingin dijelaskan saja.
