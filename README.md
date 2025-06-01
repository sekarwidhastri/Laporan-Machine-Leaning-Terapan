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
Dalam upaya mendukung penanganan masalah obesitas di kawasan Amerika Latin, proyek ini berfokus pada pemanfaatan _machine learning_ untuk memahami, memprediksi, dan memberikan rekomendasi terhadap tingkat obesitas berdasarkan perilaku makan dan kondisi fisik individu. Klarifikasi masalah dilakukan dengan mengidentifikasi tantangan utama yang dihadapi dalam konteks kesehatan masyarakat serta menguraikan tujuan spesifik yang dapat dicapai melalui pendekatan analitik.

### Problem Statements
- **Pernyataan Masalah 1**

Bagaimana memprediksi tingkat obesitas individu berdasarkan atribut kebiasaan makan, aktivitas fisik, dan kondisi fisiologis?
- **Pernyataan Masalah 2**

Bagaimana menghasilkan rekomendasi personalisasi untuk mencegah atau mengelola obesitas berdasarkan hasil prediksi?
- **Pernyataan Masalah 3**

Bagaimana mengelola ketidakseimbangan data pada kategori tingkat obesitas agar model prediksi tidak bias?

### Goals
- **Menjawab Pernyataan Masalah 1**

Mengembangkan model _machine learning_ yang mampu mengklasifikasikan tingkat obesitas secara akurat berdasarkan fitur yang relevan seperti frekuensi makan, konsumsi makanan tinggi kalori, aktivitas fisik, dan IMT.

- **Menjawab Pernyataan Masalah 2**

Menyediakan sistem rekomendasi berbasis prediksi yang dapat menyarankan perubahan gaya hidup (misalnya: olahraga, pola makan, durasi tidur) sesuai dengan profil pengguna.

- **Menjawab Pernyataan Masalah 3**

Mengimplementasikan metode penyeimbangan data seperti SMOTE untuk mengatasi ketidakseimbangan kelas dan memastikan semua kategori obesitas direpresentasikan secara adil dalam pelatihan model.

### Solution Approach
- **Solution Statement 1: Klasifikasi menggunakan Algoritma Random Forest dan XGBoost**

Model Random Forest dan XGBoost digunakan karena kemampuannya menangani fitur kategorikal, menangani _overfitting_ melalui _ensemble learning_, serta performa tinggi dalam data tabular. Keduanya dievaluasi menggunakan Precision, F1-score, dan akurasi keseluruhan.

- **Solution Statement 2: Penyeimbangan Data dengan SMOTE**

Menggunakan teknik Synthetic Minority Oversampling Technique (SMOTE) untuk meningkatkan representasi kelas minoritas. Pendekatan ini penting untuk menghindari bias model terhadap kelas mayoritas dan memastikan hasil prediksi yang adil.

- **Solution Statement 3: Sistem Rekomendasi Sederhana berbasis Aturan**

Berdasarkan output klasifikasi, diberikan rekomendasi tindakan preventif seperti:
- Underweight: Tambahkan kalori dan aktivitas fisik ringan.
- Normal: Pertahankan pola hidup saat ini.
- Overweight/Obese: Kurangi frekuensi konsumsi makanan cepat saji dan tingkatkan aktivitas fisik.

Rekomendasi ini dapat dikembangkan lebih lanjut menjadi sistem berbasis _rule engine_ atau _hybrid recommender_.

## Data Understanding
Dataset yang digunakan dalam proyek ini adalah "Estimation of Obesity Levels Based on Eating Habits and Physical Condition" yang tersedia secara publik di UCI Machine Learning Repository.
- Informasi Dataset

Jumlah data: 2.111 baris data (_individual records_)

- Jumlah fitur: 17 fitur (variabel independen) + 1 label target (Obesity level)

Asal data: 77% data sintetis dihasilkan menggunakan SMOTE di Weka, dan 23% berasal dari survei web aktual.

- Tipe data: Gabungan antara data kategorikal (nominal dan ordinal) serta numerik (kontinu)

Kondisi data: Tidak ada _missing value_, namun terdapat ketidakseimbangan kelas pada variabel target.

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
1. Distribusi Kelas (_Target Variable_)
- Kelas target tidak seimbang, sebagian besar data berada pada kelas Obesity_Type_I dan Normal_Weight.
  
  ![image](https://github.com/user-attachments/assets/8222c2bd-dd01-45ef-91a5-29af498399ce)

- Visualisasi countplot menunjukkan dominasi kelas tertentu, memperkuat keputusan penggunaan SMOTE.
  
  ![image](https://github.com/user-attachments/assets/1938247e-ad46-4e7b-86f9-5b59f696fdb7)

2. Korelasi antara variabel numerik
- Variabel Weight dan BMI (jika dihitung dari Height dan Weight) menunjukkan korelasi tinggi dengan kelas obesitas.
- Visualisasi menggunakan _pairplot_ dan _heatmap_.
  
  ![image](https://github.com/user-attachments/assets/c340b414-3862-4c18-bd40-8dcbadece5e2)

  ![image](https://github.com/user-attachments/assets/a467fdce-df94-47bd-9e96-0b613747af09)

3. Distribusi berdasarkan Gender
- Beberapa perbedaan pola terlihat antara pria dan wanita, terutama dalam aspek aktivitas fisik dan frekuensi makan.
4. Visualisasi Pola Makan dan Aktivitas Fisik
- Plot distribusi untuk NCP, FAF, dan CAEC menunjukkan tren yang berbeda antar level obesitas.
  
  ![image](https://github.com/user-attachments/assets/e32a3b4c-4545-4f45-a143-5ebaf09ae2be)

5. Outlier
- Tidak ditemukan outlier signifikan, namun Height dan Weight divalidasi rentangnya sesuai data normal manusia dewasa.
  
  ![image](https://github.com/user-attachments/assets/cda579e7-f791-4a45-ab0b-aa072b242263)

  ![image](https://github.com/user-attachments/assets/e32b94ea-453f-43d9-a9ba-6b8c4ab770c0)

**Insight Awal dari EDA**
- Terdapat hubungan antara kebiasaan makan (frekuensi makan, konsumsi kalori, minum air) dengan tingkat obesitas.
- Aktivitas fisik yang rendah berkorelasi dengan level obesitas yang lebih tinggi.
- Perokok cenderung lebih banyak berada di kelas Obesity_Type_I dan Type_II.
- Data yang tidak seimbang perlu ditangani agar model tidak bias terhadap kelas mayoritas.

## Data Preparation

Tahapan data preparation merupakan proses penting untuk memastikan bahwa data yang digunakan oleh algoritma machine learning dalam kondisi optimal. Dalam proyek ini, data preparation dilakukan secara sistematis untuk menangani berbagai isu seperti format data, ketidakseimbangan kelas, serta skala nilai antar fitur.

**1. Pemisahan Fitur dan Label**

Langkah awal adalah memisahkan fitur (`X`) dan label target (`y`). Fitur merupakan 16 variabel independen yang mencerminkan gaya hidup dan kondisi fisik, sedangkan label (target) adalah kategori tingkat obesitas.

**Alasan**: Model membutuhkan input (fitur) dan output (label) yang terpisah agar dapat dilatih secara supervised.

**2. Encoding Label (Label Encoding)**

Label target yang berupa string (seperti *Insufficient Weight*, *Normal Weight*, *Obesity Type I*, dst.) diubah ke dalam format numerik menggunakan `LabelEncoder`.

**Alasan**: Sebagian besar algoritma machine learning klasik (seperti K-Nearest Neighbor, Random Forest, AdaBoost) tidak bisa memproses label dalam bentuk string.

**3. One-Hot Encoding pada Fitur Kategorikal**

Fitur kategorikal seperti `Gender`, `family_history_with_overweight`, `FAVC`, `CAEC`, `SMOKE`, dan `SCC` diubah ke dalam format one-hot encoding. Ini menghasilkan beberapa kolom biner baru untuk merepresentasikan kategori tersebut.

**Alasan**: Algoritma machine learning tidak dapat secara langsung memproses data kategorikal, dan one-hot encoding mencegah pemodelan asumsi urutan pada data nominal.

**4. Feature Scaling**

Seluruh fitur numerik dinormalisasi menggunakan `StandardScaler` agar memiliki mean = 0 dan standard deviation = 1.

**Alasan**: Scaling sangat penting untuk algoritma yang sensitif terhadap skala (misalnya KNN, SVM, atau algoritma berbasis jarak), dan membantu konvergensi lebih cepat pada model ensemble seperti XGBoost.

**5. Train-Test Split**

Data dibagi menjadi data latih (80%) dan data uji (20%) menggunakan stratifikasi pada label target agar distribusi kelas tetap seimbang di kedua subset.

**Alasan**: Pembagian ini penting untuk mengevaluasi performa model secara adil terhadap data yang belum pernah dilihat sebelumnya.

**6. Pemeriksaan Distribusi Kelas**

Distribusi label obesitas diperiksa dan divisualisasikan menggunakan seaborn `countplot()`. Visualisasi menunjukkan bahwa data sudah seimbang karena sebelumnya telah dilakukan balancing menggunakan SMOTE.

**Alasan**: Memastikan tidak ada dominasi kelas tertentu yang dapat menyebabkan bias pada model.


| Tahap                      | Teknik                         | Alasan Penggunaan                       |
|----------------------------|--------------------------------|------------------------------------------|
| Pemisahan fitur dan label  | `.drop()` dan indexing         | Memisahkan input dan output              |
| Encoding label target      | `LabelEncoder`                 | Mengubah label string ke numerik         |
| Encoding fitur kategorikal | `pd.get_dummies()`             | Menghindari asumsi urutan                |
| Normalisasi fitur          | `StandardScaler`               | Mengatur skala untuk algoritma ML        |
| Split data                 | `train_test_split`             | Evaluasi adil terhadap model             |
| Visualisasi distribusi     | `seaborn.countplot()`          | Memastikan distribusi seimbang           |

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
