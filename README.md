# Unsupervised Learning
## Airline Customer Value Analysis Case
 Pada pekerjaan ini dilakukan pembuatan machine learning clustering dari sebuah dataset. Dataset ini berisi data customer sebuah perusahaan penerbangan dan beberapa fitur yang dapat menggambarkan value tersebut. Gambar dibawah menunjukkan deskripsi dataset dan hasil clustering.
 
 ![dataset_un](https://user-images.githubusercontent.com/116563315/205465472-2c2be932-1612-40c3-b61e-83e459a7f33e.jpg)

![clustering](https://user-images.githubusercontent.com/116563315/205465584-815cef6a-5477-419b-b709-228113859a4f.jpg)

## Project Organization
1. requirements.txt : package yang digunakan pada model
2. eda_preprocessing_model.ipynb : proses tahap eda hingga menjadi model
3. flight.csv : dataset yang digunakan
4. README.md : report tahapan

## Prerequisites
1. Download data [here](https://drive.google.com/drive/folders/1v7BjYPybGlhQ9oNiPwgA-1l1uh3Vi3yW)
2. Instalasi dengan `pip install requirements.txt`

## Getting Started
1. *Exploratory Data Analysis*, dilakukan proses cek duplikat, cek nilai null, mengecek deskripsi data apakah ada yang aneh atau tidak, cek data outlier, cek korelasi, distribusi dan redundan.
2. *Preprocessing*, hasil dari pengamatan EDA selanjutnya diselesaikan di tahapan ini. Tahapan yang dilakukan pada proses ini yaitu *data cleansing, feature selection, scaling*
3. *Model*, pada proses ini dilakukan pembuatan model untuk unsupervised learning - K-means Clustering. Kemudian, hasil dari K-means Clustering dievaluasi menggunakan Elbow Method dan Silhouette hasilnya jumlah clustering yang optimal adalah 4 cluster.

![4_cluster](https://user-images.githubusercontent.com/116563315/205470405-979899b9-007e-42db-ba18-0c3d47143da4.jpg)

Dari hasil clustering tersebut, kami lakukan interpretasi perbedaan dari masing-masing cluster.

![cobaindeh](https://user-images.githubusercontent.com/116563315/205470514-ca31b9ca-2d56-4252-89a3-3b57a785751a.jpg)

Kami lakukan pengelompokan sebagai berikut
1. Cluster 0 : menunjukkan customer yang sudah bergabung sekitar hampir 7 tahun, jarang melakukan penerbangan dan jarak penerbangan yang dilakukan tidak jauh (retained customer)
2. Cluster 1 : menunjukkan customer yang sudah bergabung sekitar hampir 5 tahun, aktif dalam menggunakan jasa penerbangan dan sering berpergian dengan jarak yang cukup jauh (High-value customer)
3. Cluster 2 : menunjukkan customer yang sudah bergabung sekitar 2 tahun (tergolong baru), sering melakukan penerbangan dan jaraknya cukup jauh. (potential customer)
4. Cluster 3 : menunjukkan customer yang sudah bergabung sekitar 3 tahun (tergolong baru) namun sangat jarang menggunakan jasa penerbangan dan sekali menggunakan juga tidak terlalu jauh (low-value customer)

## Strategi Bisnis
Stratei bisnis yang dapat disusun sebagai berikut.
1. Membuat sebuah skema reward untuk pelanggan loyal yang sering menggunakan jasa penerbangan dan skema tersebut dapat meningkat seiring meningkatnya pengeluaran yang dilakukan oleh customer, sehingga customer yang loyal ini merasa memiliki target untuk mengejar skema reward yang lebih tinggi yang menurutnya menguntungkan dan juga menguntungkan bagi perusahaan.
2. Membuat sebuah sistem promo secara general (untuk keseluruhan customer) dalam bentuk voucher yang memiliki kode unik yang semakin cepat diklaim maka nilai potongannya cukup besar (untuk memancing customer menggunakan jasa penerbangan lebih sering agar frekuensi penggunaan jasanya meningkat) dan berlaku juga sebaliknya (semakin lama diklaim semakin kecil nilai potongannya)