#Midterm Deep Learning – UTS

Nama: Raihan Ivando Diaz
Kelas: TK-46-02
NIM: 110233093

Repositori ini berisi pengerjaan Midterm Deep Learning yang berfokus pada penerapan deep learning klasik / tradisional untuk tiga studi kasus berbeda:

Fraud Detection (binary classification)

Song Year Prediction (regression)

Customer Segmentation (clustering)

Seluruh eksperimen dikerjakan menggunakan Google Colab dan disusun sebagai pipeline yang lengkap mulai dari data loading, preprocessing, modeling, evaluasi, hingga interpretasi hasil.

1. Colab Notebooks

Berikut notebook yang digunakan dalam pengerjaan tugas ini:

1. Fraud Detection (Binary Classification)

Notebook:
https://colab.research.google.com/drive/1oy3oSqRwylEHJQU3sOE5CFnUKfMLPGvB?usp=sharing

Ringkasan:

Menggunakan data transaksi online dengan label isFraud.

Preprocessing meliputi handling missing values, scaling, dan train-test split.

Menggunakan model Deep Learning (ANN) sebagai classifier.

Evaluasi menggunakan accuracy, precision, recall, dan confusion matrix.

Model digunakan untuk memprediksi probabilitas fraud pada test_transaction.csv.

2. Song Year Prediction (Regression)

Notebook:
https://colab.research.google.com/drive/1SJDw8bEMYYy_d0JS6M0FO5SM0B5js3_o?usp=sharing

Ringkasan:

Dataset berisi fitur numerik anonim dengan target berupa tahun rilis lagu.

Preprocessing: normalization, pengecekan outlier, dan pemisahan target.

Model menggunakan ANN regresi.

Evaluasi menggunakan MAE, MSE, dan RMSE.

Hasil model menunjukkan kemampuan memprediksi tahun dengan tingkat error tertentu berdasarkan pola fitur audio.

3. Customer Clustering (Unsupervised Learning)

Notebook:
https://colab.research.google.com/drive/1-wYI-6R09II2HKXgqRf1HtMRLobyavJZ?usp=sharing

Ringkasan:

Data berisi perilaku transaksi pengguna kartu kredit (balance, payments, purchases, limit, dll.).

Melakukan cleaning, scaling, dan reduksi dimensi (PCA jika dibutuhkan).

Menggunakan algoritma deep clustering / ANN-based embedding sebelum klasterisasi.

Evaluasi menggunakan visualisasi cluster (2D) dan interpretasi karakteristik tiap cluster, seperti:

High spender

Minimal spender

Frequent installment users

Risky customers

2. Overview Project
2.1 Tujuan

Proyek ini bertujuan membangun pipeline Deep Learning untuk tiga problem yang berbeda:

Klasifikasi – Memprediksi kemungkinan sebuah transaksi merupakan fraud.

Regresi – Memprediksi tahun rilis sebuah lagu berdasarkan fitur numerik audio.

Clustering – Mengelompokkan pengguna kartu kredit berdasarkan pola perilaku finansialnya.

Setiap notebook mempraktikkan:

Data preprocessing & cleaning

Feature scaling

Handling missing values

Model ANN (Artificial Neural Network)

Evaluasi model sesuai jenis tugas

Interpretasi dan visualisasi hasil

2.2 Ringkasan Implementasi
Fraud Detection – Binary Classification

Target: isFraud

Fitur mencakup nilai transaksi, informasi kartu, alamat, waktu, dan kode produk.

Model ANN dengan beberapa hidden layers.

Output: prob. fraud untuk setiap transaksi.

Song Year Prediction – Regression

Target berupa tahun rilis (angka).

Input berupa fitur numerik anonim dari karakteristik audio.

Model ANN regresi.

Evaluasi menggunakan error metrics (MAE/MSE/RMSE).

Customer Segmentation – Clustering

Dataset kredit kartu: pembelian, frekuensi transaksi, cash advance, payments, credit limit, dan lainnya.

Preprocessing + feature scaling.

Pendekatan deep clustering untuk mendapatkan representasi fitur yang lebih baik.

Hasil akhir berupa cluster & analisis interpretatif perilaku tiap kelompok.

3. Dataset Descriptions
3.1 Fraud Detection

train_transaction.csv: data berlabel untuk pelatihan.

test_transaction.csv: data tanpa label untuk prediksi final.

Target:

1 = fraud

0 = tidak fraud

3.2 Song Year Prediction

midterm-regresi-dataset.csv

Kolom pertama = target (tahun), sisanya = fitur numerik audio.

3.3 Customer Clustering

clusteringmidterm.csv

Kolom penting:

BALANCE, PURCHASES, PAYMENTS, MINIMUM_PAYMENTS

CREDIT_LIMIT

frekuensi transaksi & cash advance

TENURE

Setiap baris = satu nasabah kartu kredit.

4. Struktur Project

Struktur repositori dapat mengikuti format berikut:
