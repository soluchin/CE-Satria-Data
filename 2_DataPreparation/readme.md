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

