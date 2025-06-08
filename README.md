# Laporan Proyek Machine Learning - Sekar Ayu Widhastri

## Project Overview
Obesitas merupakan salah satu tantangan kesehatan masyarakat global yang paling signifikan abad ini. Peningkatan prevalensi obesitas tidak hanya terjadi di negara maju, tetapi juga di negara berkembang, termasuk wilayah Amerika Latin seperti Meksiko, Peru, dan Kolombia. Perubahan gaya hidup modern—seperti meningkatnya konsumsi makanan tinggi kalori, menurunnya aktivitas fisik akibat urbanisasi dan digitalisasi, serta pola makan yang tidak sehat—telah menjadi pemicu utama melonjaknya angka kelebihan berat badan dan obesitas di populasi dewasa maupun remaja.

Dampak obesitas sangat luas. Selain meningkatkan risiko berbagai penyakit kronis seperti diabetes tipe 2, penyakit kardiovaskular, hipertensi, gangguan muskuloskeletal, dan beberapa jenis kanker, obesitas juga berdampak pada kualitas hidup, produktivitas kerja, dan beban biaya kesehatan jangka panjang yang ditanggung sistem kesehatan publik.

Menurut laporan World Health Organization (WHO, 2020), lebih dari 1,9 miliar orang dewasa di seluruh dunia mengalami kelebihan berat badan pada tahun 2016, dengan sekitar 650 juta orang di antaranya diklasifikasikan sebagai obesitas [1]. Di Meksiko, prevalensi obesitas di kalangan orang dewasa telah mencapai lebih dari 70%, menjadikannya salah satu negara dengan angka obesitas tertinggi di dunia [2].

Peningkatan tren obesitas yang konsisten dan multidimensional menandakan bahwa upaya pencegahan dan penanggulangan tidak cukup hanya mengandalkan pendekatan konvensional. Diperlukan strategi berbasis data dan teknologi yang mampu mengidentifikasi individu dengan risiko tinggi serta memberikan rekomendasi yang tepat dan terpersonalisasi.

Dataset: [Estimation of Obesity Levels Dataset](https://archive.ics.uci.edu/dataset/544/estimation+of+obesity+levels+based+on+eating+habits+and+physical+condition)

## Mengapa Masalah Harus Diselesaikan
### Urgensi Masalah
- Obesitas meningkatkan angka morbiditas dan mortalitas akibat penyakit tidak menular.
- Memberikan tekanan besar terhadap sistem pelayanan kesehatan, baik dari sisi biaya maupun sumber daya manusia.
- Berdampak pada produktivitas kerja dan kualitas hidup masyarakat secara umum.
- Penelitian Barboza et al. (2020) menunjukkan bahwa faktor pola makan tinggi kalori, kurang olahraga, dan riwayat keluarga merupakan penyumbang utama prevalensi obesitas di Amerika Latin [2].

## Strategi Penyelesaian
- Pengembangan model prediktif, yaitu menggunakan algoritma K-Nearest Neighbor, Random Forest, dan AdaBoost untuk klasifikasi tingkat obesitas dengan akurasi tinggi.
- Praproses data meliputi encoding data kategorikal, normalisasi, serta validasi kualitas data sintetis menggunakan referensi metode dari Chawla et al. (2002) [3].
- Evaluasi model menggunakan metrik akurasi yaitu Precision, Recall, dann F1-score
- Personalisasi intervensi dengan membuat rekomendasi berbasis hasil prediksi seperti pola diet dan aktivitas fisik yang sesuai.
- Relevansi kebijakan publik yaitu dengan menyediakan insight berbasis data untuk mendukung intervensi kesehatan masyarakat dan kampanye nasional melawan obesitas.

## Riset Terkait
Beberapa studi terdahulu mendukung efektivitas pendekatan machine learning dalam prediksi obesitas:
- DeGregory et al. (2018) menemukan bahwa metode _machine learning_ seperti Random Forest mampu memprediksi obesitas dengan akurasi > 85%, menunjukkan potensi tinggi dalam aplikasi klinis [4].
- Chawla et al. (2002) memperkenalkan teknik SMOTE yang efektif untuk meningkatkan performa klasifikasi pada dataset yang tidak seimbang [3].
- Barboza et al. (2020) mengonfirmasi bahwa pendekatan kuantitatif sangat penting untuk memahami penyebab obesitas di Amerika Latin, terutama terkait faktor sosial dan perilaku [2].

## Referensi
1. WHO. “Obesity and overweight,” 2020.  
2. Barboza et al. “Obesity in Latin America,” *Journal of Public Health in Latin America*, 2020.  
3. Chawla et al. “SMOTE,” *Journal of AI Research*, 2002.  
4. DeGregory et al. “A review of ML in obesity,” *Obesity Reviews*, 2018.

## Business Understanding
Isu obesitas semakin menjadi perhatian utama di berbagai negara, khususnya di Amerika Latin, di mana perubahan gaya hidup, pola makan tidak sehat, dan kurangnya aktivitas fisik menjadi faktor pemicu utama. Peningkatan angka obesitas dapat berdampak serius terhadap kualitas hidup, risiko penyakit kronis, dan beban biaya kesehatan. Oleh karena itu, penting bagi institusi kesehatan dan pemerintah untuk memiliki sistem prediktif yang mampu mengidentifikasi risiko obesitas secara dini berdasarkan kebiasaan makan dan kondisi fisik masyarakat.

Dataset ini menyediakan data demografis, kebiasaan makan, serta aktivitas fisik individu yang dapat dimanfaatkan untuk membangun model prediktif dan mendukung pengambilan keputusan yang lebih akurat dalam upaya pencegahan obesitas.

### Problem Statements
- **Pernyataan Masalah 1**

Bagaimana pengaruh kebiasaan makan seperti konsumsi sayuran, makanan berkalori tinggi, dan jumlah makan utama terhadap tingkat obesitas seseorang?
- **Pernyataan Masalah 2**

Sejauh mana gaya hidup, seperti frekuensi aktivitas fisik dan penggunaan perangkat elektronik, memengaruhi risiko obesitas?
- **Pernyataan Masalah 3**

Dapatkah kita membangun model klasifikasi yang akurat untuk memprediksi tingkat obesitas seseorang berdasarkan atribut demografis dan kebiasaan hidup?

### Goals
- **Menjawab Pernyataan Masalah 1**

Melakukan analisis korelasi dan visualisasi antara pola makan (misalnya: frekuensi konsumsi sayuran, makanan berkalori tinggi, jumlah makan utama) dengan level obesitas untuk mengidentifikasi faktor makanan yang paling berpengaruh terhadap obesitas.

- **Menjawab Pernyataan Masalah 2**

Menganalisis hubungan antara gaya hidup (seperti olahraga, penggunaan gadget, transportasi harian) dengan kategori obesitas untuk memberikan wawasan tentang perilaku sehari-hari yang berisiko tinggi terhadap obesitas.

- **Menjawab Pernyataan Masalah 3**

Mengembangkan model machine learning (misalnya: Random Forest, Boosting, SVM) untuk mengklasifikasikan individu ke dalam level obesitas yang sesuai berdasarkan data demografis dan perilaku, dengan tujuan akhir mendapatkan akurasi prediksi yang tinggi serta interpretabilitas yang baik.

### Solution Approach
- **Solution Statement 1: _Baseline_ Model dengan Algoritma Klasik**

Pertama, dilakukan pembangunan baseline model menggunakan algoritma klasifikasi klasik seperti KNN dan Random Forest Classifier. Model ini bertujuan memberikan dasar awal untuk evaluasi performa, sekaligus membantu memahami pengaruh masing-masing fitur terhadap level obesitas. Evaluasi dilakukan menggunakan metrik akurasi, precision, recall, dan F1-score untuk mengamati distribusi kesalahan klasifikasi.

- **Solution Statement 2: _Ensemble Learning_ untuk Meningkatkan Akurasi**

Setelah _baseline_ diperoleh, langkah selanjutnya adalah membangun model yang lebih kompleks menggunakan metode _ensemble learning_ seperti AdaBoost. Model ini dipilih karena kemampuannya dalam menangkap hubungan non-linear serta performa yang baik pada data tabular dengan banyak fitur kategorikal dan numerik. Kinerja model dievaluasi menggunakan metrik akurasi, precision, recall, dan F1-score.

- **Solution Statement 3: Hyperparameter Tuning untuk Model Optimasi**

Untuk lebih mengoptimalkan kinerja model, dilakukan hyperparameter tuning menggunakan teknik seperti Grid Search dan Random Search (dengan Optuna). Parameter seperti jumlah estimators, max_depth, learning_rate, dan minimum sample split disesuaikan guna memperoleh kombinasi terbaik yang meningkatkan generalisasi model. Efektivitas tuning diukur melalui peningkatan metrik evaluasi dan stabilitas skor validasi silang.

## Data Understanding
Dataset yang digunakan dalam proyek ini adalah "Estimation of Obesity Levels Based on Eating Habits and Physical Condition" yang tersedia secara publik di UCI Machine Learning Repository.
- Informasi Dataset

Jumlah data: 2.111 baris data (_individual records_)

- Jumlah fitur: 16 fitur (variabel independen) + 1 label target (Obesity level)

Asal data: 77% data sintetis dihasilkan menggunakan SMOTE di Weka, dan 23% berasal dari survei web aktual.

- Tipe data: Gabungan antara data kategorikal serta numerik

Kondisi data: Tidak ada _missing value_.

Dataset ini mencakup informasi seputar kebiasaan makan, aktivitas fisik, serta kondisi kesehatan dasar yang mempengaruhi risiko obesitas. Data dikumpulkan dari tiga negara di Amerika Latin: Meksiko, Peru, dan Kolombia.

### Variabel pada Dataset
Berikut adalah daftar variabel/fitur beserta deskripsinya:
| Fitur | Deskripsi |
|---|---|
| Gender | Jenis kelamin (Male, Female) |
| Age | Usia (tahun) |
| Height | Tinggi badan (meter) |
| Weight | Berat badan (kg) |
| family_history_with_overweight | Riwayat keluarga obesitas (yes, no) |
| FAVC | Konsumsi makanan tinggi kalori (yes, no) |
| FCVC | Konsumsi sayur (skala 1-3) |
| NCP | Jumlah makanan utama (1-4 kali) |
| CAEC | Konsumsi makanan antar waktu |
| SMOKE | Merokok (yes, no) |
| CH2O | Konsumsi air harian (liter, 1-3) |
| SCC | Memantau kalori (yes, no) |
| FAF | Aktivitas fisik mingguan (jam) |
| TUE | Waktu penggunaan teknologi (jam) |
| CALC | Konsumsi alkohol |
| MTRANS | Transportasi yang digunakan |
| NObeyesdad | Label tingkat obesitas (target) |

## Exploratory Data Analysis (EDA)
Beberapa langkah eksplorasi data yang dilakukan:
### Univariate Analysis (Fitur Kategorik)
1. Distribusi Gender
- Dataset ini memiliki distribusi gender yang relatif seimbang, dengan laki-laki (Male) mencakup 52% dan perempuan (Female) sebesar 48% dari total sampel. Distribusi yang hampir merata ini mengurangi risiko bias terhadap salah satu gender dalam model klasifikasi atau prediksi. Namun, tetap penting untuk memantau apakah terdapat perbedaan pola obesitas berdasarkan gender di tahap analisis selanjutnya, terutama dalam kaitannya dengan fitur-fitur numerik seperti Weight, FCVC, dan CALC. Grafik batang yang dihasilkan menunjukkan jumlah absolut sampel untuk masing-masing gender. Ini memberikan gambaran awal tentang keseimbangan demografis dataset yang akan berpengaruh terhadap generalisasi model.

  ![image](https://github.com/user-attachments/assets/5a3e7620-1598-437a-b87c-5f9c90cb5620)

2. Distribusi Responden dengan Keluarga yang Memiliki Riwayat Obesitas
- Sebagian besar responden (85%) memiliki riwayat keluarga dengan kelebihan berat badan, menunjukkan bahwa faktor genetik atau lingkungan keluarga kemungkinan memainkan peran penting dalam risiko obesitas pada populasi ini. Hanya 15% responden yang tidak memiliki riwayat obesitas dalam keluarga, yang menjadi kelompok penting untuk dianalisis lebih lanjut untuk melihat pengaruh faktor non-genetik (seperti pola makan, aktivitas fisik, dll). Distribusi yang sangat timpang ini perlu diperhatikan saat membangun model prediktif, karena ketidakseimbangan kelas dapat menyebabkan bias prediksi terhadap kelompok mayoritas.

  ![image](https://github.com/user-attachments/assets/a856e6bc-c104-4922-8381-51f073d23476)

3. Distribusi Responden yang Mengonsumsi Makanan Tinggi Kalori
- Sebagian besar responden (88.7%) sering mengonsumsi makanan tinggi kalori, yang merupakan faktor risiko utama penyebab kegemukan dan obesitas. Hanya 11.3% dari responden yang tidak sering mengonsumsi makanan tinggi kalori, menunjukkan bahwa kebiasaan makan berkalori tinggi merupakan pola umum dalam dataset ini. Distribusi ini menunjukkan adanya potensi korelasi yang kuat antara FAVC dan status obesitas. Fitur ini sangat relevan untuk dimasukkan dalam model klasifikasi obesitas.

  ![image](https://github.com/user-attachments/assets/d7011b81-ba50-40f2-9793-2c3cf6440d03)
  
4. Distribusi Responden yang Mengkonsumsi _Snack_
- Mayoritas responden (86.8%) kadang-kadang makan di antara jam makan utama, menunjukkan perilaku makan selingan cukup umum.Sebanyak 12% responden (gabungan Frequently dan Always) memiliki kebiasaan makan selingan yang lebih sering atau bahkan konstan, yang bisa berdampak pada peningkatan asupan kalori harian. Hanya 1.2% yang menyatakan tidak pernah makan di antara jam makan, menunjukkan bahwa makan selingan merupakan kebiasaan luas dalam populasi ini.

  ![image](https://github.com/user-attachments/assets/8bea7463-fb29-4e5f-b19c-8fc0be57ff63)

5. Distribusi Responden yang Merokok
- Sebagian besar responden (97.9%) tidak merokok, menunjukkan bahwa dalam dataset ini, kebiasaan merokok sangat jarang ditemukan. Hanya 2.1% responden yang menyatakan memiliki kebiasaan merokok, sehingga fitur ini memiliki distribusi yang sangat tidak seimbang (imbalanced).

  ![image](https://github.com/user-attachments/assets/32d22de3-7678-43c7-abd1-b90b42135783)

6. Distribusi Responden dengan Kebiasaan Memantau Asupan Kalori
- Mayoritas responden (95.2%) tidak memantau asupan kalori yang mereka konsumsi sehari-hari. Hanya 4.8% responden yang memiliki kebiasaan memantau kalori, menandakan bahwa kesadaran terhadap pengelolaan pola makan masih rendah dalam populasi ini.

  ![image](https://github.com/user-attachments/assets/c1d0b59a-eaac-4eb5-a589-9da3dd662c31)

7. Distribusi Responden dengan Kebiasaan Konsumsi Alkohol
- Sebagian besar responden (72.8%) melaporkan mengonsumsi alkohol sesekali, menandakan kebiasaan sosial atau insidental. 24.1% responden tidak mengonsumsi alkohol sama sekali, yang merupakan kelompok potensial untuk dianalisis terkait gaya hidup sehat. Hanya 3.1% yang mengonsumsi alkohol secara sering, sehingga perlu perhatian khusus terhadap efek jangka panjang pada berat badan dan metabolisme.

  ![image](https://github.com/user-attachments/assets/01a13cb3-7a6b-4590-b20c-b5404397c02c)

8. Distribusi Transportasi Responden
- Mayoritas responden (81.8%) menggunakan transportasi umum sebagai moda utama. Ini dapat menunjukkan pola aktivitas fisik yang moderat tergantung dari jumlah jalan kaki yang terlibat. Penggunaan mobil pribadi sebesar 14.7% bisa diasosiasikan dengan gaya hidup lebih sedentari, yang mungkin berdampak pada risiko obesitas. Hanya 3.4% responden yang memilih moda aktif seperti berjalan kaki atau bersepeda, yang menunjukkan aktivitas fisik harian rendah secara umum.

  ![image](https://github.com/user-attachments/assets/60b09c5a-dcb7-4f2f-96ab-c3f93f6f8cbb)

9. Distribusi Label Obesitas pada Responden
- Obesity_Type_III (kategori obesitas paling parah) merupakan kategori terbesar (22.9%) dalam dataset, menandakan bahwa sebagian besar responden mengalami obesitas berat. Jika ketiga tipe obesitas digabungkan (Type I, II, dan III), maka 52.5% dari total responden mengalami obesitas, menunjukkan urgensi masalah ini dalam populasi yang diteliti. Hanya 14.1% responden berada pada berat badan normal, sedangkan 10.5% tergolong kekurangan berat badan. Tingginya persentase pada kategori obesitas dapat menjadi fokus utama dalam model prediksi dan rekomendasi intervensi kesehatan.

  ![image](https://github.com/user-attachments/assets/271cfe9d-6b3d-4ef6-88c7-d53f531ee05a)

### Univariate Analysis (Fitur Numerik)

![image](https://github.com/user-attachments/assets/6dc96afb-a175-4ffa-8790-8c8db2e0b9c5)

- **Age**: Distribusi tidak merata dengan puncak signifikan di kisaran 20-25 tahun, menunjukkan mayoritas data berasal dari kelompok usia muda.
- **Height**: Distribusi agak simetris di sekitar 1.6-1.8 meter, dengan puncak di 1.7 meter, menunjukkan tinggi badan yang cukup konsisten.
- **Weight**: Distribusi melebar dengan puncak di 60-80 kg, menunjukkan variasi berat badan yang cukup besar.
- **FCVC**: Distribusi sangat miring dengan puncak tinggi di 2-3, menunjukkan sebagian besar data memiliki konsumsi makanan utama yang serupa.
- **NCP**: Distribusi miring dengan puncak di 3, menunjukkan mayoritas memiliki 3 kali makan utama per hari.
- **CH2O**: Distribusi miring dengan puncak di 2-2.5 liter, menunjukkan pola konsumsi air yang cukup konsisten.
- **FAF**: Distribusi miring dengan puncak di 0-1, menunjukkan aktivitas fisik rendah di sebagian besar data.
- **TUE**: Distribusi miring dengan puncak di 0-0.5 jam, menunjukkan penggunaan teknologi yang umumnya rendah.

### Multivariate Analysis
**Gambar 1: Sebaran Kategori 'NObeyesdad' Berdasarkan 'Gender'**
menunjukkan distribusi kategori **NObeyesdad** berdasarkan **Gender**. Beberapa poin penting yang dapat disimpulkan:
- **Female**:
  - Didominasi oleh kategori **Obesity_Type_III** dengan jumlah tertinggi, menunjukkan bahwa obesitas parah lebih banyak terjadi pada perempuan dalam dataset ini.
  - Kategori **Insufficient_Weight** juga cukup tinggi pada perempuan dibandingkan laki-laki.
  - Sebaran kategori lainnya relatif merata, tetapi **Normal_Weight** juga termasuk yang cukup tinggi.
- **Male**:
  - Paling banyak berada dalam kategori **Obesity_Type_II**, menunjukkan bahwa obesitas tingkat menengah lebih umum pada laki-laki dalam data ini.
  - Terdapat jumlah signifikan pada kategori **Obesity_Type_I** dan **Overweight_Level_II**.
  - Kategori **Insufficient_Weight** memiliki jumlah yang jauh lebih rendah dibandingkan pada perempuan.

- **Perbandingan Gender**:
  - **Obesity_Type_III** sangat dominan pada perempuan, sedangkan **Obesity_Type_II** paling dominan pada laki-laki.
  - **Normal_Weight** hampir seimbang antara laki-laki dan perempuan, tetapi sedikit lebih tinggi pada laki-laki.
  - Beberapa kategori seperti **Overweight_Level_I** dan **Overweight_Level_II** memiliki distribusi yang tidak terlalu mencolok perbedaannya antar gender.

    ![image](https://github.com/user-attachments/assets/9205e287-4138-429d-9d5c-21740f03aeab)

**Gambar 2: Sebaran Kategori 'NObeyesdad' Berdasarkan 'family_history_with_overweight'**
menunjukkan distribusi status berat badan berdasarkan apakah seseorang memiliki **riwayat keluarga yang mengalami kelebihan berat badan** atau tidak.

**Jika memiliki riwayat keluarga (Yes):**
- Distribusi sangat didominasi oleh kategori **Obesity_Type_III**, menunjukkan bahwa faktor genetik atau lingkungan keluarga dapat berkontribusi besar terhadap tingkat obesitas ekstrem.
- Kategori obesitas lainnya (**Obesity_Type_I** dan **Obesity_Type_II**) juga cukup tinggi.
- Terdapat sebaran yang relatif merata untuk kategori **Normal_Weight**, **Overweight_Level_I**, dan **Overweight_Level_II**, namun jauh lebih kecil dibanding kategori obesitas.
- Kategori **Insufficient_Weight** cukup rendah, menunjukkan bahwa kekurangan berat badan tidak umum pada kelompok ini.

**Jika tidak memiliki riwayat keluarga (No):**
- **Kategori Normal_Weight dan Insufficient_Weight** mendominasi, menunjukkan bahwa orang tanpa riwayat keluarga cenderung memiliki berat badan normal atau malah kurang.
- Kategori **Obesity_Type_I, II, III** sangat minim atau hampir tidak ada.
- Jumlah individu pada kelompok ini juga secara keseluruhan lebih sedikit dibandingkan kelompok dengan riwayat keluarga.

  ![image](https://github.com/user-attachments/assets/0baa82bf-d656-4425-a39b-6fccab3dd193)

**Gambar 3: Sebaran Kategori 'NObeyesdad' Berdasarkan 'FAVC'**
- **Kategori 'No' (Tidak Sering Mengkonsumsi Makanan Tinggi Kalori)**:
  - `Normal_Weight` memiliki jumlah tertinggi (50), diikuti oleh `Overweight_Level_I` (40) dan `Obesity_Type_III` (30).
  - Kategori `Insufficient_Weight`, `Obesity_Type_I`, dan `Obesity_Type_II` memiliki jumlah yang relatif rendah (<20).

- **Kategori 'Yes' (Sering Mengkonsumsi Makanan Tinggi Kalori)**:
  - `Obesity_Type_III` mendominasi dengan jumlah tertinggi (~300), menunjukkan korelasi kuat antara konsumsi makanan tinggi kalori dan obesitas tingkat tinggi.
  - `Insufficient_Weight` memiliki jumlah terendah (0), menunjukkan bahwa konsumsi makanan tinggi kalori jarang terkait dengan berat badan kurang.
  - `Normal_Weight` (150), `Overweight_Level_I` (200), `Obesity_Type_I` (200), dan `Obesity_Type_II` (100) juga signifikan, dengan `Overweight_Level_I` dan `Obesity_Type_I` menunjukkan distribusi yang seimbang.

    ![image](https://github.com/user-attachments/assets/2661fbd8-96f3-43b6-9aee-345f01376e2d)

**Gambar 4: Sebaran Kategori 'NObeyesdad' Berdasarkan 'CAEC'**
- **Kategori 'Sometimes'**:
  - `Obesity_Type_III` memiliki jumlah tertinggi (300), menunjukkan korelasi kuat antara konsumsi makanan di antara waktu makan secara sesekali dengan obesitas tingkat tinggi.
  - `Overweight_Level_II` (200), `Obesity_Type_I` (200), dan `Obesity_Type_II` (150) juga signifikan.
  - `Normal_Weight` (~100) dan `Insufficient_Weight` (50) memiliki jumlah yang lebih rendah.
- **Kategori 'Frequently'**:
  - `Normal_Weight` mendominasi (50), diikuti oleh `Insufficient_Weight` (30).
  - Kategori obesitas seperti `Obesity_Type_III` dan `Overweight_Level_II` memiliki jumlah sangat rendah (<10).
- **Kategori 'Always'**:
  - `Normal_Weight` memiliki jumlah tertinggi (20), diikuti oleh `Insufficient_Weight` (10).
  - Kategori obesitas hampir tidak ada, menunjukkan bahwa konsumsi makanan di antara waktu makan secara terus-menerus jarang terkait dengan obesitas.
- **Kategori 'No'**:
  - `Normal_Weight` dan `Insufficient_Weight` masing-masing memiliki jumlah sangat kecil (5), dengan kategori obesitas hampir tidak ada.
  
    ![image](https://github.com/user-attachments/assets/cae894fa-1bbc-421a-b02d-b11bf79447a2)

**Gambar 5: Sebaran Kategori 'NObeyesdad' Berdasarkan 'SMOKE'**
- **Kategori 'No' (Tidak Merokok)**:
  - `Obesity_Type_III` memiliki jumlah tertinggi (300), menunjukkan korelasi kuat antara tidak merokok dengan obesitas tingkat tinggi.
  - `Normal_Weight` (200), `Obesity_Type_I` (200), `Overweight_Level_II` (180), dan `Obesity_Type_II` (150) juga signifikan.
  - `Insufficient_Weight` (120) memiliki jumlah yang lebih rendah dibandingkan kategori obesitas.
- **Kategori 'Yes' (Merokok)**:
  - `Normal_Weight` memiliki jumlah tertinggi (20), diikuti oleh `Insufficient_Weight` (10).
  - Kategori obesitas seperti `Obesity_Type_III`, `Obesity_Type_I`, dan `Overweight_Level_II` memiliki jumlah sangat rendah (<5), menunjukkan bahwa merokok jarang terkait dengan obesitas.
  
    ![image](https://github.com/user-attachments/assets/f7721d31-f1c9-4e16-a393-d633c5b89268)

**Gambar 6: Sebaran Kategori 'NObeyesdad' Berdasarkan 'SCC'**
- **Kategori 'No' (Tidak Ada Konsumsi Kalori Tinggi di Akhir Pekan)**:
  - `Obesity_Type_III` mendominasi (300), menunjukkan korelasi kuat dengan obesitas tingkat tinggi.
  - `Normal_Weight` (200), `Obesity_Type_I` (200), dan `Overweight_Level_II` (180) juga signifikan.
- **Kategori 'Yes' (Ada Konsumsi Kalori Tinggi di Akhir Pekan)**:
  - `Normal_Weight` (20) dan `Insufficient_Weight` (10) paling umum, dengan obesitas sangat minim.
  
    ![image](https://github.com/user-attachments/assets/5187b089-14e3-4307-a7f1-a6ec443205b7)

**Gambar 7: Sebaran Kategori 'NObeyesdad' Berdasarkan 'CALC' (Konsumsi Alkohol)**
- **Kategori 'no' (Tidak Pernah Minum Alkohol):**
  - Distribusi paling merata antar kategori berat badan.
  `Obesity_Type_I` mendominasi kategori ini, diikuti oleh `Overweight_Level_I`, `Overweight_Level_II`, dan `Normal_Weight`.
  `Obesity_Type_III` sangat sedikit, menunjukkan bahwa tidak minum alkohol tidak serta-merta mencegah obesitas berat, tetapi lebih umum ditemukan pada tingkat obesitas ringan hingga sedang
  `Insufficient_Weight` juga memiliki porsi yang signifikan, menunjukkan bahwa tidak mengonsumsi alkohol umum pada individu dengan berat badan di bawah normal.

- **Kategori 'Sometimes' (Kadang Minum Alkohol):**
  - Merupakan kategori dengan jumlah individu terbanyak di antara seluruh kategori `CALC`
  `Obesity_Type_III` sangat dominan, menunjukkan korelasi antara konsumsi alkohol sesekali dengan obesitas tingkat tinggi.
  `Obesity_Type_II`, `Obesity_Type_I`, dan `Overweight_Level_I` juga tinggi, mengindikasikan tren peningkatan berat badan seiring konsumsi alkohol.
  `Normal_Weight` dan `Overweight_Level_II` tetap signifikan, mencerminkan variasi kondisi tubuh dalam kelompok ini.

- **Kategori 'Frequently' (Sering Minum Alkohol):**
  - Jumlah individu jauh lebih sedikit dibandingkan kategori sebelumnya.
  Distribusi kecil dan merata pada `Normal_Weight`, `Overweight_Level_I`, `Obesity_Type_I`, dan `Overweight_Level_II`.
  `Obesity_Type_II` dan `Obesity_Type_III` menurun drastis, menunjukkan sedikit hubungan dalam kelompok ini.

- **Kategori 'Always' (Selalu Minum Alkohol):**
  - Hampir tidak ada representasi data, sangat sedikit individu dalam kategori ini.
  Tidak terlihat pola dominan karena datanya sangat terbatas.
    ![image](https://github.com/user-attachments/assets/4c874e25-516c-4ba3-85d6-999e1710b437)

**Gambar 8: Sebaran Kategori 'NObeyesdad' Berdasarkan 'MTRANS'**
- **Kategori 'Public_Transportation'**:
  - `Obesity_Type_III` mendominasi (300), diikuti oleh `Obesity_Type_I` (200) dan `Overweight_Level_II` (150).
  - `Normal_Weight` (100) dan `Insufficient_Weight` (50) lebih rendah.
- **Kategori 'Automobile'**:
  - `Obesity_Type_I` (50) dan `Normal_Weight` (40) paling umum, dengan obesitas lainnya rendah.
- **Kategori 'Walking', 'Motorbike', dan 'Bike'**:
  - Distribusi rendah (<20), didominasi oleh `Normal_Weight` dan `Insufficient_Weight`.
**Insight Awal dari EDA**
- Terdapat hubungan antara kebiasaan makan (frekuensi makan, konsumsi kalori, minum air) dengan tingkat obesitas.
- Aktivitas fisik yang rendah berkorelasi dengan level obesitas yang lebih tinggi.
- Perokok cenderung lebih banyak berada di kelas Obesity_Type_I dan Type_II.
- Data yang tidak seimbang perlu ditangani agar model tidak bias terhadap kelas mayoritas.

  ![image](https://github.com/user-attachments/assets/b7001393-4716-4d6d-8c2c-cf2f83fbb78e)

### Visualisasi Hubungan Antar Fitur Numerik
![image](https://github.com/user-attachments/assets/e31e8cdf-3560-4f73-962d-6f66eddc0ae6)
**Korelasi Positif**
- **Height vs Weight**: Terlihat ada kecenderungan korelasi **positif** antara tinggi dan berat badan, meskipun tidak terlalu kuat. Artinya, individu yang lebih tinggi cenderung memiliki berat badan lebih besar.
- **Age vs Weight**: Terlihat korelasi **positif lemah**, di mana individu yang lebih tua cenderung memiliki berat badan lebih tinggi.

**Pola Multimodal**
- Fitur **Weight**, **Age**, dan **CH2O** menunjukkan distribusi **multimodal** pada diagonal plot (kde), yang mengindikasikan adanya **cluster atau sub-kelompok** dalam populasi, kemungkinan berdasarkan kategori obesitas atau pola hidup.

**Tidak Ada Korelasi Jelas**

Sebagian besar fitur lainnya seperti:
- **FCVC** (Frekuensi konsumsi sayur),
- **NCP** (Jumlah makan utama),
- **CH2O** (Asupan air harian),
- **FAF** (Frekuensi aktivitas fisik), dan
- **TUE** (Penggunaan perangkat elektronik)

tidak menunjukkan korelasi linier yang jelas satu sama lain. Pola sebaran titik yang acak (scattered) ini kemungkinan disebabkan oleh:
- Skala kategori numerik yang **terbatas** (contoh: FCVC hanya bernilai 1–3),
- Adanya efek dari variabel kategorikal lain yang belum divisualisasikan (misalnya: jenis kelamin, transportasi, dll).

**Outlier & Konsentrasi**
- Terlihat beberapa **outlier** pada fitur seperti `Weight`, `FAF`, dan `TUE`.
- Terdapat **konsentrasi titik** pada nilai tertentu, menunjukkan bahwa fitur-fitur seperti `FCVC`, `NCP`, dan `CH2O` kemungkinan berasal dari **skala ordinal atau kategorikal yang dikonversi ke numerik**.

### Memvisualisasikan Matriks Korelasi untuk Fitur Numerik
![image](https://github.com/user-attachments/assets/3906918e-41a6-4cf9-9f0a-c3af2a1655f8)
- **Korelasi Tinggi (Positif)**:
  - `Weight` memiliki korelasi kuat (0.44) dengan `Height`, menunjukkan hubungan positif antara berat dan tinggi badan.
  - `FCVC` memiliki korelasi kuat (0.28) dengan `Weight`, menunjukkan hubungan positif antara frekuensi konsumsi sayuran dalam setiap makan dan berat badan.
  - `NCP` memiliki korelasi kuat (0.06) dengan `CH2O`, menunjukkan hubungan positif yang lemah antara jumlah makan utama per hari dan jumlah konsumsi air putih (CH2O).
  - `FAF` memiliki korelasi kuat (0.12) dengan `CH2O`, menunjukkan hubungan positif yang lemah antara aktivitas fisik dan konsumsi air putih.
  - `TUE` memiliki korelasi kuat (0.08) dengan `FAF`, menunjukkan hubungan positif yang lemah antara penggunaan waktu teknologi dan aktivitas fisik.

- **Korelasi Negatif**:
  - `Age` memiliki korelasi negatif (-0.19) dengan `TUE`, menunjukkan bahwa semakin tua usia, semakin sedikit waktu yang dihabiskan untuk teknologi.
  - `Height` memiliki korelasi negatif (-0.09) dengan `FCVC`, menunjukkan hubungan negatif yang lemah antara tinggi badan dan frekuensi konsumsi sayuran dalam setiap makan.
  - `Weight` memiliki korelasi negatif (-0.13) dengan `TUE`, menunjukkan bahwa semakin berat seseorang, semakin sedikit waktu yang dihabiskan untuk teknologi.
  - `FCVC` memiliki korelasi negatif (-0.12) dengan `TUE`, menunjukkan hubungan negatif yang lemah antara frekuensi konsumsi sayuran dalam setiap makan dan penggunaan teknologi.
  - `NCP` memiliki korelasi negatif (-0.04) dengan `TUE`, menunjukkan hubungan negatif yang sangat lemah antara konsumsi makanan utama dan penggunaan teknologi.
  - `CH2O` memiliki korelasi negatif (-0.02) dengan `TUE`, menunjukkan hubungan negatif yang sangat lemah antara konsumsi air dan penggunaan teknologi.

- **Observasi Umum**:
  - Matriks menunjukkan bahwa korelasi antar fitur secara keseluruhan cukup rendah, dengan beberapa pasangan menunjukkan hubungan yang signifikan (baik positif maupun negatif).
  - Fitur seperti `Age`, `Weight`, dan `FVC` memiliki pengaruh lebih jelas terhadap fitur lain dibandingkan `NCP`, `CH2O`, `FAF`, dan `TUE`.

### Memvisualisasikan Outliers
![image](https://github.com/user-attachments/assets/833449c9-2cda-4813-ad7e-c47f451c6d5c)
![image](https://github.com/user-attachments/assets/b01ea32a-a39f-49a4-8acc-1565de16a9bd)
![image](https://github.com/user-attachments/assets/dfc8ee0b-bd28-4c57-b6f4-370bde184803)
![image](https://github.com/user-attachments/assets/6549260c-ccf7-4ca9-becc-4cdc1f219a61)
![image](https://github.com/user-attachments/assets/521fdc0f-3254-4a1a-93ab-6e4dfd407e93)
![image](https://github.com/user-attachments/assets/efabe508-1aea-457d-bcea-b9a12d6be51e)
![image](https://github.com/user-attachments/assets/81520981-fd28-49e4-9af4-e4a4c0a618cd)
![image](https://github.com/user-attachments/assets/d4a60d84-058c-4460-a5ee-0dd030a62751)

## Data Preparation

Pada tahap ini, dilakukan berbagai langkah persiapan data sebelum diterapkan pada model machine learning. Tujuan utama dari tahapan ini adalah memastikan kualitas data, menghilangkan gangguan seperti outlier, serta menyederhanakan dimensi data agar model dapat bekerja secara optimal. Berikut adalah tahapan-tahapannya secara berurutan:

1. Penghapusan Outlier

Pada tahap awal data preparation, dilakukan **penghapusan outlier** pada fitur numerikal menggunakan metode **IQR (Interquartile Range)**. Outlier adalah nilai-nilai ekstrem yang jauh dari sebaran umum data dan dapat memengaruhi performa serta akurasi model jika tidak ditangani.

**Langkah-langkah:**

1). **Seleksi kolom numerik**: hanya kolom bertipe numerik yang dipertimbangkan.

2). **Hitung Q1, Q3, dan IQR**:
   - Q1: Kuartil pertama (25%)
   - Q3: Kuartil ketiga (75%)
   - IQR = Q3 - Q1
     
3). **Tentukan batas bawah dan atas untuk mendeteksi outlier**:
   - Batas bawah = Q1 - 1.5 × IQR
   - Batas atas = Q3 + 1.5 × IQR
     
4). **Filter baris-baris yang mengandung outlier** di **kolom numerik mana pun**, dan buang baris tersebut dari dataset.

**Kode:**

```python
# Ambil hanya kolom numerikal
numeric_cols = obesity_df.select_dtypes(include='number').columns

# Hitung Q1, Q3, dan IQR hanya untuk kolom numerikal
Q1 = obesity_df[numeric_cols].quantile(0.25)
Q3 = obesity_df[numeric_cols].quantile(0.75)
IQR = Q3 - Q1

# Buat filter untuk menghapus baris yang mengandung outlier di kolom numerikal
filter_outliers = ~((obesity_df[numeric_cols] < (Q1 - 1.5 * IQR)) |
                    (obesity_df[numeric_cols] > (Q3 + 1.5 * IQR))).any(axis=1)

# Terapkan filter ke dataset asli (termasuk kolom non-numerikal)
obesity_df = obesity_df[filter_outliers]

# Cek ukuran dataset setelah outlier dihapus
obesity_df.shape
```

2. Encoding Variabel Kategorikal

Setelah proses pembersihan data (seperti penghapusan outlier), langkah selanjutnya dalam tahap data preparation adalah mengubah fitur kategorikal menjadi format numerik agar dapat diproses oleh algoritma machine learning. Untuk ini digunakan teknik **One-Hot Encoding**.

**Langkah-langkah:**

1). Beberapa kolom dalam dataset memiliki tipe data kategorikal (non-numerik), seperti:
- `Gender`
- `family_history_with_overweight`
- `FAVC` (Frequent consumption of high-caloric food)
- `CAEC` (Eating between meals)
- `SMOKE`
- `SCC` (Monitoring of calorie consumption)
- `CALC` (Frequency of alcohol consumption)
- `MTRANS` (Transportation used)
  
2). Semua kolom tersebut diubah ke dalam format **One-Hot Encoding** dengan menggunakan `pd.get_dummies()`, yaitu setiap kategori akan diubah menjadi kolom biner (0 atau 1).

3). Setelah encoding selesai, kolom asli yang bersifat kategorikal dihapus menggunakan `drop()` karena telah direpresentasikan oleh kolom hasil encoding.

**Kode:**

```python
obesity_df = pd.concat([obesity_df, pd.get_dummies(obesity_df['Gender'], prefix='Gender')], axis=1)
obesity_df = pd.concat([obesity_df, pd.get_dummies(obesity_df['family_history_with_overweight'], prefix='family_history_with_overweight')], axis=1)
obesity_df = pd.concat([obesity_df, pd.get_dummies(obesity_df['FAVC'], prefix='FAVC')], axis=1)
obesity_df = pd.concat([obesity_df, pd.get_dummies(obesity_df['CAEC'], prefix='CAEC')], axis=1)
obesity_df = pd.concat([obesity_df, pd.get_dummies(obesity_df['SMOKE'], prefix='SMOKE')], axis=1)
obesity_df = pd.concat([obesity_df, pd.get_dummies(obesity_df['SCC'], prefix='SCC')], axis=1)
obesity_df = pd.concat([obesity_df, pd.get_dummies(obesity_df['CALC'], prefix='CALC')], axis=1)
obesity_df = pd.concat([obesity_df, pd.get_dummies(obesity_df['MTRANS'], prefix='MTRANS')], axis=1)
```

4). Hapus kolom asli karena sudah diencoding
obesity_df.drop(['Gender', 'family_history_with_overweight', 'FAVC', 'CAEC', 'SMOKE', 'SCC', 'CALC', 'MTRANS'], axis=1, inplace=True)

5). Tampilkan hasil encoding
obesity_df.head()

3. Standarisasi dan Reduksi Dimensi (PCA)

Standarisasi dilakukan agar setiap fitur memiliki rata-rata 0 dan standar deviasi 1. Ini penting karena PCA sangat sensitif terhadap skala data. Jika fitur memiliki rentang nilai yang berbeda jauh, maka fitur dengan skala besar akan mendominasi hasil PCA. Standarisasi dilakukan menggunakan `StandardScaler` dari pustaka `sklearn`.

```python
scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)
```

Setelah itu, PCA dikonfigurasi untuk menghasilkan 3 komponen utama (principal components):
```python
pca = PCA(n_components=3, random_state=123)
X_pca = pca.fit_transform(X_scaled)
```

Kemudian, dilakukan visualisasi untuk membantu melihat distribusi kelas obesitas berdasarkan hasil reduksi dimensi:
```python
plt.figure(figsize=(10, 6))
sns.scatterplot(data=pca_df, x='PC1', y='PC2', hue='Obesity_Level', palette='Set2', s=60)
plt.title('PCA Projection (3 components - visualized in 2D)')
plt.xlabel('Principal Component 1')
plt.ylabel('Principal Component 2')
plt.legend(loc='best', bbox_to_anchor=(1, 1))
plt.tight_layout()
plt.show()
```

![image](https://github.com/user-attachments/assets/07a381b9-1305-4a5e-9e74-64d94fd3283c)

PCA juga menghasilkan informasi tentang berapa persen variansi dari data asli yang berhasil dijelaskan oleh masing-masing komponen. Semakin besar variansi yang dijelaskan, semakin baik representasi data oleh PCA.
```python
explained_var = pca.explained_variance_ratio_
print(f"Explained Variance per Component: {explained_var}")
print(f"Total Explained Variance (3 components): {explained_var.sum():.2f}")

# Output
Explained Variance per Component: [0.14850576 0.1028321  0.07563161]
Total Explained Variance (3 components): 0.3
```

## Modeling
Pada tahap ini, performa dari tiga model klasifikasi dibangun dan dibandingkan dalam menyelesaikan permasalahan klasifikasi tingkat obesitas. Model-model tersebut adalah:

1. **K-Nearest Neighbors (KNN)**
2. **Random Forest Classifier**
3. **AdaBoost Classifier (Boosting)**

Setiap model dilatih menggunakan dataset training dan diuji pada dataset test. Untuk mengukur kinerjanya, digunakan **akurasi** sebagai metrik utama, serta menampilkan hasil evaluasi tambahan seperti precision, recall, dan F1-score pada tahap evaluasi.

### Model yang Digunakan

#### 1. K-Nearest Neighbors (KNN)

- **Parameter**: `n_neighbors = 10`
- **Kelebihan**:
  - Mudah diimplementasikan.
  - Tidak memerlukan proses pelatihan kompleks.
- **Kekurangan**:
  - Sensitif terhadap noise dan skala fitur.
  - Lambat untuk data besar karena sifat lazy learning.
- **Hasil Akurasi**:
  - **Train Accuracy**: `0.79`
  - **Test Accuracy**: `0.74`

#### 2. Random Forest Classifier

- **Parameter**: `n_estimators = 50`, `max_depth = 16`, `random_state = 55`
- **Kelebihan**:
  - Tidak mudah overfitting karena menggunakan banyak pohon.
  - Dapat menangani data yang tidak seimbang dan fitur yang banyak.
- **Kekurangan**:
  - Model menjadi besar dan sulit diinterpretasikan.
- **Hasil Akurasi**:
  - **Train Accuracy**: `1.00`
  - **Test Accuracy**: `0.87`

#### 3. AdaBoost Classifier

- **Parameter**: `learning_rate = 0.05`, `random_state = 55`
- **Kelebihan**:
  - Meningkatkan kinerja model sederhana dengan boosting.
  - Baik untuk menangani outlier moderat.
- **Kekurangan**:
  - Sensitif terhadap data noise dan outlier.
  - Kurang efektif jika data tidak seimbang atau jumlah kelas banyak.
- **Hasil Akurasi**:
  - **Train Accuracy**: `0.50`
  - **Test Accuracy**: `0.51`

### Ringkasan Akurasi Model

| Model         | Train Accuracy | Test Accuracy |
|---------------|----------------|---------------|
| KNN           | 0.79           | 0.74          |
| Random Forest | 1.00           | 0.87          |
| Boosting      | 0.50           | 0.51          |


### Rekomendasi Model

#### Top Recommendation:
- **Random Forest Classifier** dipilih sebagai model terbaik berdasarkan akurasi tinggi dan generalisasi yang cukup baik pada data uji.
- Model ini mengatasi ketidakseimbangan kelas lebih baik dibandingkan dua model lainnya.

#### Alternatif Recommendation:
- **KNN** dapat digunakan sebagai baseline atau model cepat jika sumber daya komputasi terbatas.
- **Boosting** kurang direkomendasikan untuk dataset ini karena performanya jauh lebih rendah.


## Evaluation
Pada tahap ini, performa model dievaluasi pada klasifikasi obesitas menggunakan beberapa metrik evaluasi yang umum digunakan dalam permasalahan klasifikasi multiclass, yaitu:
### Metrik Evaluasi
#### 1. Accuracy
Mengukur proporsi prediksi yang benar terhadap total jumlah prediksi

Namun, pada kasus klasifikasi dengan data tidak seimbang antar kelas, **accuracy saja tidak cukup** mewakili performa model. Oleh karena itu, digunakan pula metrik lain seperti:

#### 2. Precision
Mengukur seberapa banyak prediksi positif yang benar dari seluruh prediksi positif.

#### 3. Recall
Mengukur seberapa banyak prediksi positif yang benar dari seluruh data aktual positif.

#### 4. F1-Score
Rata-rata harmonis dari precision dan recall. Cocok untuk kondisi kelas tidak seimbang.

### Hasil Evaluasi Model

#### Random Forest Classifier

| Dataset | Accuracy | Macro Avg F1 | Weighted Avg F1 |
|--------|----------|--------------|-----------------|
| Train  | 1.00     | 1.00         | 1.00            |
| Test   | 0.87     | 0.85         | 0.87            |

- **Kelebihan**: Performa sangat tinggi, mampu menangani semua kelas dengan baik.
- **Kekurangan**: Overfitting terlihat dari akurasi training yang sempurna.

#### AdaBoost Classifier

| Dataset | Accuracy | Macro Avg F1 | Weighted Avg F1 |
|--------|----------|--------------|-----------------|
| Train  | 0.50     | 0.30         | 0.39            |
| Test   | 0.51     | 0.31         | 0.40            |

- **Kelebihan**: Sederhana dan cepat.
- **Kekurangan**: Performa buruk pada kelas minoritas, sangat rendah secara umum.

#### K-Nearest Neighbor (KNN)

| Dataset | Accuracy | Macro Avg F1 | Weighted Avg F1 |
|--------|----------|--------------|-----------------|
| Train  | 0.79     | 0.75         | 0.78            |
| Test   | 0.74     | 0.69         | 0.73            |

- **Kelebihan**: Mudah diimplementasikan dan cukup baik untuk baseline model.
- **Kekurangan**: Kurang optimal untuk dataset dengan dimensi tinggi dan tidak performatif untuk kelas yang tidak seimbang.

### Kesimpulan Evaluasi

- Model terbaik berdasarkan hasil evaluasi adalah **Random Forest**, dengan akurasi tinggi dan distribusi metrik F1-score yang merata di semua kelas pada data uji.
- **AdaBoost** tidak cocok digunakan untuk dataset ini karena sangat rendah dalam mengenali kelas minoritas.
- **KNN** cukup baik untuk _baseline_, namun kalah performa dibanding Random Forest.

### Catatan
- Model-model yang digunakan telah dievaluasi berdasarkan F1-score, yang merupakan metrik utama dalam kasus ini karena:
  - Data tidak seimbang.
  - Klasifikasi yang akurat untuk semua kelas sangat penting.
- F1-score memberikan pandangan menyeluruh tentang keseimbangan antara kemampuan mendeteksi kelas yang benar (recall) dan ketepatan prediksi kelas (precision).
