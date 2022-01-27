Kuliah Online 1: Rabu, 1 September 2021
# Pengantar Statistical Machine Learning
_Oleh: Prof. Dr. Ir. Khairil Anwar Notodiputro, MS_  

<details>
  <summary>Course video</summary>
  
**Click for Full Online Course Video:**  
[![Click for full online course](https://img.youtube.com/vi/d-0zu5ZOweY/0.jpg)](https://www.youtube.com/watch?v=d-0zu5ZOweY)
</details>

**Outline:**
1. Introduction
2. Overview of Machine Learning
3. The Role of Statistics
4. Statistical Machine Learning
5. Special Topic: Active Learning

## I. Introduction:
**Apa itu statistical machine learning?**
- Statistical machine learning sangat berkembang di berbagai negara
- Menggabungkan statistika, komputasi, sistem dan optimasi
- Statistika dan sains data sulit untuk dipisahkan
- Menjadikan sains data lebih luas dari statistika itu sendiri

## II. Overview of Machine Learning  
### Apa itu machine learning?
- **Nvidia:** Machine learning adalah praktik penggunaan algoritma untuk mengurai data, belajar darinya, dan kemudian membuat penentuan atau prediksi tentang sesuatu di dunia  
- **McKinsey & Company:** Machine learning didasarkan pada algoritme yang dapat belajar dari data tanpa bergantung pada pemrograman berbasis aturan  
- **Stanford:** Machine learning membuat komputer bertindak tanpa diprogram secara eksplisit

&nbsp;&nbsp;&nbsp;Tujuan dari machine learning (ML) yaitu memanfaatkan data baru untuk membuat keputusan atau rekomendasi berdasarkan perhitungan dan analisis yang intensif 
sehingga komputasi tidak dapat dipisahkan. Dilakukan menggunakan teknik Kecerdasan Buatan atau Artificial Intelligence (AI) untuk aplikasi di berbagai bidang. Model ML dapat 
belajar, mengidentifikasi pola, dan bisa membuat keputusan dengan sedikit interensi manusia sehingga lebih efisien dan mengurangi kesalahan akibat _human error_.

### Kapan machine learning digunakan? 
&nbsp;&nbsp;&nbsp;Tidak semua masalah yang mengandung angka dan data dapat diselesaikan menggunakan teknik machine learning. Ada beberapa kriteria dimana machine learning
dibutuhkan untuk menjadi solusi, berikut adalah ciri-cirinya:
1. Masalah memerlukan data untuk proses pembelajaran
2. Masalah memerlukan prediksi
3. Mencakup masalah otomatisasi _(automation)_ yang perlu diselesaikan
4. Diperlukannya pemahaman pola
5. Ingin membangun sistem rekomendasi
6. Memerlukan pengidentifikasian entitas atau objek

### Pengaplikasian machine learning  
<img width="600" src="https://cdn-gcp.marutitech.com/wp-media/2016/10/77de88c8-top-9-applications-of-machine-learning-min.png">  
_source: https://marutitech.com/problems-solved-machine-learning/_

### 5 Langkah penyelesaian machine learning
<img align="left" height="200" src="5 step ML.png">  
<br>
<br>

1. **Periksa data:** ketahui dan pahami informasi umum data yang akan digunakan
2. **Pra-processing data** seperti memilih kolom yang diperlukan, konversi kategorik numerik dll
3. **Analisis data:** perjelas apa yang menjadi variabel respon (label) dan variabel penjelas (features)
4. **Definisikan model:** supervised/unsupervised, cluster analysis, decision tree dll
5. **Prediksi hasil:** memprediksi data baru kemudian melakukan evaluasi terhadap model

<br>

### Algoritma apa yang digunakan?
&nbsp;&nbsp;&nbsp;Untuk memahaminya, perlu mengetahui terlebih dahulu apa itu label. Secara sederhana label adalah nilai yang ingin diprediksi sebagai Y atau varibel respon. Disebut juga sebagai _dependent variable_. Terbagi menjadi 2, yaitu **Supervised Learning** & **Unsupervised Learning**. Perhatikan sintaks dibawah.
```
if(dependent_variable_exist=True):
  supervisedLearning()
else:
  unsupervisedLearning()
```
- _**Supervised Learning**_ merupakan istilah jika model membutuhkan supervisi atau label ketika membangun model
- _**Unsupervised Learning**_ sebaliknya, data Y atau label tidak tersedia untuk membangun model

**Beberapa algoritma yang dapat digunakan dengan permasalahan yang berbeda-beda:**
1. **Linear regression** - numerik data
2. **Logistic regression** - variabel output berupa binary
3. **Linear descriminant analysis** - multi category classification
4. **Decision tree** - regression & classification
5. **Ensembles** - regression & classification
6. **Naive bayes** - regression & classification
7. **K-nearest neighbour (KNN)** - classification

## III. The Role of Statistics
Peranan statistika dalam pembelajaran mesin

**Towards Statistical Learning:**  
<img align="left" height="200" src="3 step tsml.png">  
1. **Core Statistics Consepts**  
Statistika deskriptif, sebaran peluang, pengujian hipotesis, regresi dan model linear
2. **Bayesian Thinking**  
Peluang bersyarat, sebaran prior & posterior, dan kemungkinan maksimum
3. **Statistical Machine Learning**  
Konsep pembelajaran mesin, supervised & unsupervised, metode resampling, regulasi & seleksi model, model klasifikasi, non-linear, tree-based model, support vector machine

### Core Statistics Concepts
<img width="600" src="step 1 tsml.png">  

### Bayesian Thinking
<img width="600" src="step 2 tsml.png">  

### Statistical Machine Learning
<img width="600" src="step 3 tsml.png">  

## IV. Statistical Machine Learning
Model secara umum didefinisikan sebagai fungsi <img src="https://latex.codecogs.com/gif.latex?Y%3Df%28X%29%20&plus;%20%5Cepsilon">, kemudian kita akan menduga f dengan 2 alasan yaitu **prediksi** dan **inferensi**.  


**prediksi:**
- Jika kita mengetahui besaran x nantinya kita dapat menduga besaran <img src="https://latex.codecogs.com/gif.latex?%5Chat%7BY%7D%3D%5Chat%7Bf%7D%28X%29">
- Apakah dugaan akurat? harus memperhatikan _reducible error_ dan _irreducible error_
- <img src="https://latex.codecogs.com/gif.latex?E%28Y-%5Chat%7BY%7D%29%5E2%3D%5Bf%28X%29-%5Chat%7Bf%7D%28X%29%5D%5E2&plus;Var%28%5Cepsilon%29">
- <img src="https://latex.codecogs.com/gif.latex?%5Bf%28X%29-%5Chat%7Bf%7D%28X%29%5D%5E2%20%5Crightarrow%20reducable"> **reducable** adalah kesalahan yang timbul dari ketidaksesuaian antara f̂ dan f. f adalah hubungan antara X dan Y, tetapi kita hanya dapat memperkirakannya.
- <img src="https://latex.codecogs.com/gif.latex?Var%28%5Cepsilon%29%20%5Crightarrow%20irreducable"> **irreducable** adalah nilai yang muncul dari fakta bahwa X tidak sepenuhnya menentukan Y.
- Semakin minimum nilai reducable error maka penduga <img src="https://latex.codecogs.com/gif.latex?%5Chat%7BY%7D"> juga semakin mendekati nilai Y aktual.

**inferensi:**
- Menarik kesimpulan bagaimana X dapat menjelaskan Y sehingga f(X) tidak lagi dipandang sebagai _black box_
- Inferensi dapat menjawab
  - Peubah penjelas (X) apa yang memengaruhi peubah respon (Y)
  - Apakah hubungan X dan Y positif/negatif?
  - Apakah hubungannya bersifat linear/non-linear?

**prediksi** | **inferensi**
--|--
tidak penting bagaimana bentuk modelnya asalkan dapat memprediksi dengan akurat dan presisi | mementingkan bentuk modelnya dan mempelajari hakikat hubungan antara X dan Y
fokus kepada <img src="https://latex.codecogs.com/gif.latex?%5Chat%7BY%7D%20%5Crightarrow%20Y"> | fokus dengan hubungan X dan Y

**Bagaimana menduga f?**
&nbsp;&nbsp;&nbsp;Dengan digunakannya data penggamatan sebanyak n, dibagi menjadi 2 yaitu data latih dan data uji. Data latih digunakan untuk mengajari model menduga atau memprediksi nilai f, artinya model akan mempelajari dan menemukan rumus sehingga Y = f(X). Data uji digunakan untuk menilai seberapa baik model dapat memprediksi data baru yang belum pernah dilihat sebelumnya oleh model. Pendekatannya bisa bersifat **parametrik** maupun **non-parametrik**.

### Supervised vs Unsupervised
**Supervised**|**Unsupervised**
--|--
setiap prediktor memiliki label respon|prediktor tidak memiliki label respon
memprediksi label secara akurat|hanya dapat membedakan berdasarkan features yang ada
dapat melakukan inferensi|klasterisasi
