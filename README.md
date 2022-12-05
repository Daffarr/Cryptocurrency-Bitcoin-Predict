# *Cryptocurrency (Bitcoin) Predict* - Daffa Rayhan Riadi

## Project Overview

Saat ini telah banyak jenis mata uang kripto dan salah satu yang paling terkenal dan meningkati peringkat pertama saat ini adalah **Bitcoin**. **Bitcoin** adalah token Aset Kripto yang dapat digunakan dalam transaksi *peer-to-peer*, atau dibeli dan dijual di bursa dengan nilai spekulatif. **Bitcoin** dan pasar *cryptocurrency* lainnya dapat diperdagangkan setiap saat karena tidak memiliki periode tutup, inilah yang membedakannya dengan pasar lainnya. **Bitcoin** kadang berubah dan berisiko bagi para pedagang. 

Bukan hanya itu saja, banyak juga pengguna atau pemilik **Bitcoin** di Indonesia yang berinvestasi pada mata uang tersebut. Sehingga dampak yang ditimbulkan oleh kripto ini juga tidak bisa dianggap remeh terhadap perekonomian Indonesia. Mengingat negara-negara besar yang membolehkan penggunaan kripto tersebut, memiliki keterkaitan perekonomian yang besar terhadap Indonesia. Oleh karena itu kondisi jatuhnya nilai kripto sangat perlu diwaspadai karena dapat berpotensi akan mengalami krisis selain itu juga resiko arbitrase peraturan.

Selama bertahun-tahun ini prediksi harga pasar telah menarik dan menantang investor serta peneliti.karena banyak ketidakpastian yang terlibat dan banyak variabel yang mempengaruhi pasar. Faktor ketidakpastian yang ada, perlu dikurangi oleh para pedagang untuk meminimalkan risiko. Salah satu cara yang digunakan untuk melakukan hal tersebut adalah prediksi harga **Bitcoin** secara akurat.

Saat melakukan prediksi, di perlukan metode yang tepat. Salah satunya adalah dengan menerapkan ***Machine Learning***. ***Machine Learning*** adalah cabang dari kecerdasan buatan (*AI*) dan ilmu komputer yang berfokus pada penggunaan data dan algoritma untuk meniru cara manusia belajar. Penerapan ***Machine Learning*** membantu dalam proses analisis data besar dan kompleks, sehingga tugas bisa diselesaikan dengan cepat.

Berdasarkan hal tersebut, maka dilakukan penelitian tentang prediksi harga **Bitcoin** menggunakan ***Machine Learning***. Proyek ***Machine Learning*** ini di buat agar dapat memprediksi harga pasar **Bitcoin** di masa mendatang. Dengan penerapan ***Machine Learning*** di harapkan dapat mengurangi tingkat kerugian akibat harga mata uang **Bitcoin** yang tidak stabil.

## *Business Understanding*
### *Problem Statements*
Berdasarkan pada latar belakang diatas, permasalahan yang dapat diselesaikan pada proyek ini adalah sebagai berikut: 
Menjelaskan pernyataan masalah:
- Bagaimana cara menganalisa data kripto jenis mata uang bitcoin?
- Bagaimana cara memproses data bitcoin sehingga dapat di latih dengan baik oleh model?
- Bagaiana cara membangun model *machine learning* yang dapat memprediksi data mata uang bitcoin dengan baik?

### *Goals*

Tujuan dibuatnya proyek ini adalah sebagai berikut:
- Mendapatkan analisa yang cukup untuk memahami data mata uang bitcoin.
- Melakukan persiapan pada data mata uang bitcoin agar dapat dengan mudah dipahami dengan baik oleh model *Machine Learning* yang dibuat.
- Dapat memprediksi nilai mata uang bitcoin dengan akurat.

### *Solution Statements*
Solusi yang dapat diterapkan agar goals diatas terpenuhi adalah sebagai berikut:
- Melakukan analisa pada data untuk dapat memahami data yang ada dengan menerapkan teknik visualisasi data. Analisa yang dapat dilakukan yaitu, antara lain:
  - Menangani missing value pada *dataset*.
  - Memeriksa korelasi antar *dataset* penting untuk memahami hubungan data target dan data fitur.
- Melakukan pemrosesan pada data seperti:
  - Mengatasi *outlier* pada *dataset* dengan menerapkan *IQR Method*.
  - Normalisasi *dataset* yang ada pada fitur numerik.
- Membangun model yang dapat memprediksi bilangan kontinu sesuai dengan permasalahan yang ingin diselesaikan. Beberapa algoritma yang akan digunakan pada model regresi proyek ini yaitu, sebagai berikut:
  - *Support Vector Regression* (*SVR*)
  - *Random Forest Regression* (*RFR*)
  - *K-Nearest Neighbours* (*KNN*)
- Menerapkan teknik *Grid Search* untuk mendapatkan parameter-parameter dengan performa terbaik pada masing-masing model.

## *Data Understanding*
Sesuai dengan Domain Proyek diatas, *dataset* yang digunakan disini adalah *dataset* mata uang **Bitcoin**. *Dataset* ini diambil dari platform [Kaggle](https://www.kaggle.com/). *Dataset* ini berformat ***CSV*** memiliki **2991 baris dan 10 kolom** sample data, yang dimana nanti **1 kolom** akan menjadi **target yaitu kolom *Close***. *Dataset* tersebut dapat di unduh di website kaggle berikut: [*Cryptocurrency Historical Prices*](https://www.kaggle.com/datasets/sudalairajkumar/cryptocurrencypricehistory?select=coin_Bitcoin.csv).

Pada penjelasan diatas disebutkan bahwa *dataset* ini memiliki 10 kolom sample sebagai berikut:
- 1 kolom data yang memiliki tipe data ***Integer*** yaitu **(*SNo*)**.
- 3 kolom data yang memiliki tipe data ***Object* atau *String*** yaitu **(*Name, Symbol, Date*)**.
- 6 kolom data yang memiliki tipe data ***Float*** yaitu **(*High, Low, Open, Close, Volume, Marketcap*)**.
- Tidak terdapat missing value pada *dataset*.

Variabel-variabel pada *Cryptocurrency Historical Prices* *dataset* adalah sebagai berikut:
- ***SNo***: Nomor Seri atau Nomor Baris Pada *Dataset*.
- ***Name***: Nama Mata Uang Kripto.
- ***Symbol***: Simbol Mata Uang Kripto.
- ***Date***: Tanggal Observasi.
- ***Open***: Harga Pembukaan Pada Hari Tertentu.
- ***High***t: Harga Tertinggi Pada Hari Tertentu.
- ***Low***: Harga Terendang Pada Hari Tertentu.
- ***Close***: Harga Penutup Pada Hari Tertentu.
- ***Volume***: Jumlah Transaksi Pada Hari Tertentu.
- ***Marketcap***: Kapitalisasi Pasar Dalam *USD*.

Sebelum melakukan pemrosesan data untuk pelatihan, perlu dilakukan analisa pada data untuk mengetahui keadaan pada data seperti korelasi antar fitur dan *outlier* pada data. Berikut visualisasi data yang menunjukkan korelasi atar fitur dan *outlier* pada data:

- **Data *Outlier***

  Dapat dilihat pada visualisasi dibawah ini, *dataset* memiliki data *outlier* yang cukup banyak, maka untuk menghandle data *outlier* tersebut pada *dataset* ini akan menggunakan *IQR Method* yaitu dengan menghapus data yang berada diluar *interquartile range*. *Interquartile* sendiri adalah *range* yang berada diantara kuartil pertama(25%) dan kuartil ketiga(75%).
  
  <img src="https://user-images.githubusercontent.com/77198942/205610714-64b1946b-9d05-4dbf-b720-7c9d9fbeddab.png" style="background-color:#FFFF" width="500"/>

  Setelah melakukan penanganan *Outlier*, data yang ada di dalam *dataset* akan berkurang menjadi **2696 data**, karena data yang termasuk dalam *outlier* akan dihapus menggunakan *IQR Method*. Dapat kita lihat visualisasi dibawah ini memperlihatkan bahwa data *outlier* masih ada walaupun sedikit. Disini kita tidak akan menghapus lagi data *outlier* yang ada agar tidak mengurangi keberagaman dari *dataset* yang digunakan.
  
  <img src="https://user-images.githubusercontent.com/77198942/205610755-2a164f9c-c8c5-4ea1-8054-9af3da491d4c.png" style="background-color:#FFFF" width="500"/>

- ***Unvariate Analysis***

  Karena target pada *dataset* ini adalah fitur *Close*, maka jika kita lihat korelasi pada fitur *dataset* tersebut pada visualisasi dibawah ini, dapat disimpulkan bahwa disini kenaikan harga dari kripto bitcoin sebanding dengan penurunan sampel data.
  
  <img src="https://user-images.githubusercontent.com/77198942/205610797-cbb6f2b6-7cfc-4fbe-a8e3-f7329809bbfa.png" style="background-color:#FFFF" width="500"/>

- ***Multivariate Analysis***

  Melalui Visualisasi dibawah ini dapat kita lihat bahwa fitur close memiliki korelasi yang tinggi atau baik dengan beberapa fitur yang ada, yakni ***High, Low, Open* dan *Marketcap***. Sedangkan fitur **Volume** dapat kita lihat memiliki korelasi yang cukup rendah.
  
  <img src="https://user-images.githubusercontent.com/77198942/205610845-c94d1eda-7dbc-41ce-b31e-318a03f8f588.png" style="background-color:#FFFF" width="500"/>

  Disini dapat kita lihat secara detail korelasinya nya menggunakan angka, dapat kita lihat rata-rata korelasi yang ada dari fitur *Close* dengan fitur lain seperti *High, Low, Open* dan *Marketcap* itu mencapai angka 0.81, sedangkan volume mencapai angka 0.78, oleh karena itu dapat memungkinkan kita untuk menghapus fitur volume pada *dataset* ini.
  
   <img src="https://user-images.githubusercontent.com/77198942/205610892-c939e4d3-c17f-42e8-8315-30dcdbb57543.png" style="background-color:#FFFF" width="500"/>

## *Data Preparation*
Berikut merupakan tahapan dalam mempersiapkan data untuk keperluan pelatihan model:

- **Menghapus Data Yang Tidak Diperlukan**

  Kolom data **Volume** dihapus karena memiliki korelasi yang rendah. Kemudian Kolom data seperti ***(SNo, Name, Symbol, Date, Marketcap)*** tidak diperlukan untuk pelatihan, karena data tersebut akan mengganggu model dalam mempelajari data. Karena isi dari data tersebut tidak memiliki *value* yang berarti untuk dipelajari oleh model. Sehingga data akan terlihat seperti ini:
  
  | *High*     | *Low*      | *Open*     | *Close*    |
  |----------|----------|----------|----------|
  | 147.488007 | 134.000000 | 134.444000 | 144.539993 |
  | 146.929993 | 134.050003	| 144.000000 | 139.000000 |
  | 139.889999 | 107.720001 | 139.000000 | 116.989998 |
  | 125.599998 | 92.281898 | 116.379997 | 105.209999 |
  | 108.127998 | 79.099998 | 106.250000 | 97.750000 |

- ***Split Dataset***

  Membagi *dataset* menjadi data latih **(x_*train* & y_*train*)** dan data uji **(x_*test* & y_*test*)** sebelum membuat model. Data latih adalah sekumpulan data yang akan digunakan oleh model untuk melakukan pelatihan. Sedangkan data uji adalah sekumpulan data yang akan digunakan untuk memvalidasi kinerja pada model yang telah dilatih. Karena data uji berperan sebagai data baru yang belum pernah dilihat oleh model, maka cara ini efektif untuk memeriksa performa model setelah proses pelatihan dilakukan. Proporsi pembagian *dataset* pada proyek ini menggunakan proporsi pembagian **80:20** yang berarti sebanyak **80% merupakan data latih** dan **20% persen merupakan data uji**.

- **Normalisasi Data**

  Melakukan transformasi pada data fitur-fitur yang akan dipelajari oleh model menggunakan library *MinMaxScaler* ataupun *StandardScaler*. Setelah dibandingkan library *MinMaxScaler* memiliki akurasi sedikit lebih baik, sehingga pada kali ini menggunakan library tersebut. *MinMaxScaler* mentransformasikan fitur dengan menskalakan setiap fitur ke rentang tertentu. Library ini menskalakan dan mentransformasikan setiap fitur secara individual sehingga berada dalam rentang yang diberikan pada set pelatihan, pada library ini memiliki range default antara 0 dan 1. Dengan merenapkan teknik normalisasi data, model akan dengan lebih mudah mengenali pola-pola yang terdapat pada data sehingga akan menghasilkan prediksi yang lebih baik daripada tidak menggunakan teknik normalisasi.

# *Modeling*
Model atau Algoritma yang digunakan pada proyek ini adalah sebagai berikut: 

- ***Support Vector Regression* (*SVR*)**

  Algoritma *supervised learning* yang berguna untuk memprediksi dari nilai kontinu. tujuan dasarnya digunakan untuk menentukan garis keputusan yang sesuai. *SVR* akan mencoba menyesuaikan garis yang paling baik dalam nilai ambang batas. Untuk hyper parameter yang digunakan pada model ini adalah sebagai berikut :
  - *`kernel`* = *`rfr`*, Parameter ini adalah metode yang digunakan untuk mengambil data sebagai input dan mengubahnya menjadi bentuk pemrosesan data yang diperlukan.
  - *`C`* = `100000`, Parameter C ini menukar klasifikasi yang benar dari contoh pelatihan terhadap maksimalisasi *margin* fungsi keputusan. Untuk nilai C yang lebih besar, *margin* yang lebih kecil akan diterima jika fungsi keputusan lebih baik dalam mengklasifikasikan semua titik pelatihan dengan benar. C yang lebih rendah akan mendorong *margin* yang lebih besar, oleh karena itu fungsi keputusan yang lebih sederhana, dengan mengorbankan akurasi pelatihan. Dengan kata lain C berperilaku sebagai parameter regularisasi dalam *SVR*.
  - *`gamma`* = `0.3`, Parameter ini secara intuitif, parameter *gamma* menentukan seberapa jauh pengaruh satu contoh pelatihan mencapai, dengan nilai rendah berarti 'jauh' dan nilai tinggi berarti 'dekat'. Parameter *gamma* dapat dilihat sebagai kebalikan dari radius pengaruh sampel yang dipilih oleh model sebagai vektor pendukung.

  Kelebihan:
  - Model keputusan mudah untuk diperbarui.
  - *SVR* melakukan komputasi yang lebih rendah
  - Memiliki kemampuan generalisasi yang sangat baik, dengan akurasi prediksi yang tinggi
  - Implementasi yang mudah

  Kekurangan:
  - Tidak cocok diimplementasikan untuk data yang besar.
  - Jika jumlah fitur untuk setiap titik data melebihi jumlah sampel data pelatihan, *SVR* berperforma buruk.
  - Model keputusan tidak berkinerja sangat baik ketika kumpulan data memiliki lebih banyak *noise*

- ***Random Forest Regression* (*RFR*)**

  Merupakan Algoritma yang fleksibel dan mudah untuk digunakan. “*Forest*” yang dibangunnya adalah kumpulan *decision tree*, biasanya dilatih dengan metode “*bagging*”. Ide umum dari metode *bagging* adalah kombinasi model pembelajaran meningkatkan hasil keseluruhan. Untuk hyperparameter yang digunakan pada model ini adalah sebagai berikut:
  - *`n_estimator`* = `6`, Parameter ini adalah jumlah *trees* (pohon) di *forest*.
  - *`max_depth`* = `16`, Parameter ini adalah kedalaman atau panjang pohon. Ia merupakan ukuran seberapa banyak pohon dapat membelah (*splitting*) untuk membagi setiap *node* ke dalam jumlah pengamatan yang diinginkan.

- ***K-Nearest Neighbours* (*KNN*)**

  Algoritma *KNN* merupakan algoritma klasifikasi yang bekerja dengan mengambil sejumlah K data terdekat (tetangganya) sebagai acuan untuk menentukan kelas dari data baru. Algoritma ini mengklasifikasikan data berdasarkan kesamaan atau kemiripan atau kedekatannya terhadap data lainnya. Algoritma *KNN* digunakan untuk klasifikasi dan regresi. Pada pembuatan model ini akan menggunaka modul *KNN* yang terlah di sediakan oleh *library scikit-learn*. Untuk hyperparameter yang digunakan pada model ini hanya 1 yaitu :
  - *`n_neighbors`* = `7` Jumlah tetangga untuk yang diperlukan untuk menentukan letak data baru.
  
  Cara kerja Algoritma *KNN* secara umum :
  - Tentukan jumlah tetangga (K) yang akan digunakan untuk pertimbangan penentuan kelas.
  - Hitung jarak dari data baru ke masing-masing *data point* pada *dataset*.
  - Ambil sejumlah K data dengan jarak terdekat, kemudian tentukan kelas dari data baru tersebut.
  
Model dengan solusi terbaik pada proyek ini adalah *Support Vector Regression* (*SVR*). Dimana model ini memiliki nilai error paling rendah dari kedua model lainnya **(*K-Nearest Neighbours* (*KNN*) & *Random Forest Regression* (*RFR*))**

# Evaluasi
Evaluasi untuk proyek *machine learning* kali ini akan menggunakan metrik evaluasi *Mean Squared Error*(*MSE*). *MSE* terdiri atas 2 komponen yaitu bias dan varians. Untuk menentukan uji kebenaran, maka dilakukan dengan mengukur *error*. Analisis yang menghasilkan nilai *MSE* terkecil akan menghasilkan model terbaik.

  $$ *MSE* = { \frac{\displaystyle \sum_{t=1}^n (At-Ft)^2} {n} } $$

Dimana : 
* $At$ = Data Sebenarnya
* $Ft$ = Nilai prediksi dari variabel Y
* $n$ = banyaknya observasi

Setelah melakukan evaluasi menggunakan metrik *mean squared error* pada model dengan menggunakan data uji didapatkan hasil sebagai berikut:

<img src="https://user-images.githubusercontent.com/77198942/205601138-97a8d05b-8762-4e42-a467-bfe7b4647b40.png" style="background-color:#FFFF" width="500"/>

Dari 3 model yang telah dijalankan, dapat dilihat dari visulisasi diatas bahwa *MSE* pada model ***Support Vector Regression* (*SVM*)** merupakan *MSE* yang paling rendah dari kedua model lainnya **(*K-Nearest Neighbours* (*KNN*) & *Random Forest Regression* (*RFR*))**, selain itu jumlah *error* pada saat pengujian tidak berbeda jauh dengan *error* pada saat pelatihan. Hasil ini dapat digunakan untuk membantu para *trader* khusunya pengguna kripto bitcoin Indonesia dalam melakukan transaksi di dalam dunia kripto.

# Conclusion
Kesimpulan dari beberapa pembahasan diatas berdasarkan proyek yang sudah dijalankan, dapat diketahui bahwa Model ***Support Vector Regression* (*SVM*)** adalah yang paling baik dari model yang lainnya.

# References
1. Fatah, H., & Subekti, A. (2018). PREDIKSI HARGA CRYPTOCURRENCY DENGAN METODE K-NEAREST NEIGHBOURS. Jurnal Pilar Nusa Mandiri, 14(2). https://doi.org/10.33480/pilar.v14i2.894
2. Moch Farryz Rizkilloh, & Sri Widiyanesti. (2022). Prediksi Harga Cryptocurrency Menggunakan Algoritma Long Short Term Memory (LSTM). Jurnal RESTI (Rekayasa Sistem Dan Teknologi Informasi), 6(1). https://doi.org/10.29207/resti.v6i1.3630
3. Saputra Endra. (2018). Dampak Cryptocurrency Terhadap Perekonomian Indonesia. Seminar Nasional Royal (SENAR).

