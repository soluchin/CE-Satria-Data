Kuliah Online 2: Sabtu, 4 September 2021
# Data Preparation
_Oleh: Usman Bustaman, S.Si., MSE, M.Sc._  

<details>
  <summary>Course video</summary>
  
**Click for Full Online Course Video:**  
[![Click for full online course](https://img.youtube.com/vi/dggfr_sE7U4/0.jpg)](https://www.youtube.com/watch?v=dggfr_sE7U4)
</details>

**Outline:**
1. Introduction
2. Data Cleaning
3. Data Transformation
4. Data Integration

## I. Introduction
### Apa itu data preparation?
&nbsp;&nbsp;&nbsp;Saat ini data tersedia dengan sangat banyak sehingga menjadi tantangan bagaimana caranya kita dapat memanfaatkan data yang banyak itu. Namun, sebelum data dapat
menghasilkan suatu informasi yang berharga, data perlu melalui proses **data preparation**. Proses ini adalah proses persiapan dan penghilangan data mentah (raw data) sebelum
dianalisis dengan tujuan untuk menghasilkan data yang valid, berkualitas dan sesuai dengan format kebutuhan bisnis atau pengguna data.
> Hampir 80% proses data mining digunakan untuk persiapan data (data preparation)

<img width="600" src="https://devopedia.org/images/article/194/2438.1584952442.svg">

### Mengapa perlu dilakukannya data preparation?
&nbsp;&nbsp;&nbsp;Data yang ditemukan biasanya bersifat mentah (raw data). Jika dalam analisisnya menggunakan secara mentah-mentah data tersebut dikhawatirkan nantinya akan menghasilkan
analisis atau informasi yang tidak akurat bahkan tidak valid. Secara umum dibagi menjadi 3 jenis:
- Tidak lengkap (incomplete): Sebagian data tidak terisi, valuenya tidak tersedia, hanya tersedia agregatnya saja.
- Mengandung error dan outlier: Value dari sebuah variabel tidak sesuai.
- Tidak konsisten: Sebagian value memiliki format atau tipe data yang berbeda untuk 1 variabel.

> Pre-processing data dapat mencegah **Garbage In, Garbage Out** sehingga mendapatkan informasi yang berkualitas

### Apa manfaatnya?
Proses ini memastikan bahwa data siap untuk dianalisis dan terpercaya (Veracity & Integrity)
**Outcome:**
- Proses analisis menjadi efisien
- Mengidentifikasi dan memperbaiki masalah pada data yang yang mungkin belum ditemukan
- Menjadikan data lebih informatif untuk para pengambil keputusan
- Meningkatkan nilai tambah data

> Avoid duplication of efforts in preparing data that can be used in multiple application

### Posisi data preparation dalam satu rangkaian proses data mining
<img width="600" src="https://4.bp.blogspot.com/-6MFgXybnJJw/WsRDXvQWHtI/AAAAAAAAAXc/1Yq1-1dMIIsYknOSqaQXflWbdwXBDxQIwCEwYBhgL/s1600/kdd.jpg">

**Data preparation** terjadi dari proses pertama hingga proses transformasi data sehingga menjadikan 3 dari 5 proses tersebut merupakan preparasi data.


### CRISP-DM
<img align="left" width="300" src="https://www.datascience-pm.com/wp-content/uploads/2021/02/CRISP-DM.png">
<br>

**CRoss Industry Standard Process for Data Mining (CRISP-DM)** is a process model with six phases that naturally describes the data science life cycle:
1. Business understanding – What does the business need?
2. Data understanding – What data do we have / need? Is it clean?
3. Data preparation – How do we organize the data for modeling?
4. Modeling – What modeling techniques should we apply?
5. Evaluation – Which model best meets the business objectives?
Deployment – How do stakeholders access the results?

### 3 Aktifitas utama data preparation
<img width="600" src="3 aktifitas utama.png">

## II. Data Cleaning
- Proses penting setelah seleksi fitur/atribut
- Terdiri dari 2 aktivitas: **quality checking** & **data reduction**
- **Quality checking:** memeriksa data untuk menjamin standar kualitas data
- **Data reduction:** meringkas data tanpa mengurangi informasi yang ada pada data aslinya

### Quality Checking
Terdapat beberapa aspek yang perlu diperhatikan untuk menilai apakah suatu data berkualitas atau tidak. Biasa disebut sebagai **Quality Assurance Framework** (QAF).
berikut adalah dimensi kualitas data yang diperhatihan:
- Completeness
- Accuracy
- Consistency
- Timeliness
- Believability
- Value added
- Interpretablity
- Accessibility

### Handling missing value
Menggunakan teknik imputasi, namun teknik ini memiliki resiko yaitu data sudah tidak lagi real atau asli.
- Cek secara manual
- Berikan nilai 0 (sangat beresiko)
- Berikan kode: "None", "999" dsb
- Diisi dengan rata-rata variabel dengan memperhatikan grup/kelas dimana data itu berada
- Estimasi menggunakan regresi, clustering, dsb

### Noisy data
<img width="600" src="https://www.researchgate.net/profile/Jianwen-Luo-2/publication/220227041/figure/fig4/AS:729402707034117@1550914565642/The-ideal-data-the-noisy-data-A-A-A-and-the-smoothed-data-using-the.jpg">

Noisy data dimana data memuat error atau memuat outliers (data yang secara nyata berbeda dengan data-data yang lain).  
**Penyebab:**
- Kesalahan input data oleh faktor manusia maupun kesalahan alat ukur
- Terdapat masalah pada saat proses transmisi data
- Terdapat output data yang duplikat, tidak lengkap & tidak konsisten

**Dapat diatasi dengan data transformation** (_Clustering_, _Smoothing_)  
- Smoothing  
Melakukan pengelompokkan data ke dalam kelompok/ kategori tertentu. Contoh median smoothing, moving average dan binning
- Clustering  
Mengelompokkan suatu set objek sedemikian rupa sehingga setiap objek yang berada dalam satu cluster memiliki kemiripin yang lebih tinggi dibandingkan dengan objek yang ada di cluster lain

### Outlier
&nbsp;&nbsp;&nbsp;Sejenis noise tapi melenceng terlalu jauh, namun tidak selamanya outlier ini adalah data yang salah. Bisa jadi karena memang valuenya benar namun berbeda jauh dengan nilai yang lainnya. Sebagai contoh, bila seseorang melakukan survei di perusahaan dan menanyakan gaji dari setiap staff dan bossnya, bisa jadi gaji bosnya berada jauh dengan nilai rata-ratanya namun data tersebut valid. Outlier lebih mudah dideteksi menggunakan grafik.
- Univariate: Grafik kurva normal, boxplot
- Multivariate: Clustering, curve fitting

### Inkonsistensi data
&nbsp;&nbsp;&nbsp;Masalah inkonsistensi data muncul karena adanya hubungan antara satu variabel dengan variabel lainnya pada suatu set data namun dari kedua set tersebut dihasilkan suatu informasi yang berbeda. Contoh:
- Hubungan antara data **umur** dan **tanggal lahir**, jika **tahun lahir=2000** namun tertulis **umur=31**.
- Antara **kumulatif penjualan mingguan** dengan **penjualan harian**. Penjualan harian = 4,2,1,3,4,2; kumulatif mingguan= 34.
- Data **total mahasiswa= 30** namun tersedia 32 data mahasiswa

**Solusi:** Buat rumusan validasi data berisi kumpulan peraturan konsistensi antara nilai atribut baik dalam sebuah record maupun antar record

### Dimension reduction
Perlu melakukan reduksi data untuk mengatasi data yang sangat banyak dan alat komputasi tidak mampu untuk mengolahnya, sehingga data menjadi lebih ringkas namun tidak menghilangkan informasi yang dibutuhkan untuk proses analisis. Proses ini dilakukan dengan cara mengurangi ukuran dimensi data baik itu data kolom (atribut/variabel/features) maupun baris (record, cases).  
**teknik yang dapat dilakukan:**
- Feature selection: hanya memilih variabel yang akan diteliti
- Clustering: pengelompokkan data berdasarkan record dan variabel, bisa dengan smoothing untuk record dan PCA untuk variabel
- Rasio missing values: menghilangkan data yang memiliki missing value tinggi
- Variasi: menghilangkan variabel dengan tingkat keragaman kecil karena tidak memiliki banyak informasi yang dapat diolah

## III. Data Transformation
