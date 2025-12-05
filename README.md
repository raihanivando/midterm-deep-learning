# **Midterm Deep Learning – UTS**

**Nama:** Raihan Ivando Diaz
**Kelas:** TK-46-02
**NIM:** 110233093

Repositori ini berisi pengerjaan **Midterm Deep Learning** dengan fokus pada penerapan *classical deep learning* untuk tiga permasalahan berbeda:

* **Fraud Detection** (Binary Classification)
* **Song Year Prediction** (Regression)
* **Customer Segmentation** (Clustering)

Seluruh proses dikerjakan secara end-to-end menggunakan *Google Colab*, mulai dari pemuatan data, pembersihan, preprocessing, pembuatan model ANN, evaluasi, hingga interpretasi hasil.

---

## ** 1. Google Colab Notebooks**

### **1. Fraud Detection – Binary Classification**

🔗 Notebook:
[https://colab.research.google.com/drive/1oy3oSqRwylEHJQU3sOE5CFnUKfMLPGvB?usp=sharing](https://colab.research.google.com/drive/1oy3oSqRwylEHJQU3sOE5CFnUKfMLPGvB?usp=sharing)

**Ringkasan:**

* Mengolah dataset transaksi online dengan label `isFraud`.
* Melakukan preprocessing: handling missing values, scaling, dan split data.
* Membangun model *Artificial Neural Network* untuk klasifikasi fraud.
* Evaluasi mencakup accuracy, precision, recall, F1-Score, serta confusion matrix.
* Model digunakan untuk memprediksi probabilitas fraud pada data `test_transaction.csv`.

---

### **2. Song Year Prediction – Regression**

🔗 Notebook:
[https://colab.research.google.com/drive/1SJDw8bEMYYy_d0JS6M0FO5SM0B5js3_o?usp=sharing](https://colab.research.google.com/drive/1SJDw8bEMYYy_d0JS6M0FO5SM0B5js3_o?usp=sharing)

**Ringkasan:**

* Dataset berisi fitur numerik anonim dengan target berupa tahun rilis lagu.
* Melakukan normalisasi, pengecekan outlier, dan pemisahan label fitur.
* Menggunakan model ANN regresi untuk memprediksi tahun.
* Evaluasi menggunakan MAE, MSE, dan RMSE.
* Memberikan gambaran performa model dalam memperkirakan tahun berdasarkan pola audio.

---

### **3. Customer Clustering – Unsupervised Learning**

🔗 Notebook:
[https://colab.research.google.com/drive/1-wYI-6R09II2HKXgqRf1HtMRLobyavJZ?usp=sharing](https://colab.research.google.com/drive/1-wYI-6R09II2HKXgqRf1HtMRLobyavJZ?usp=sharing)

**Ringkasan:**

* Dataset mencakup perilaku finansial pengguna kartu kredit (balance, purchases, payments, limit, dll.).
* Preprocessing: cleaning, scaling, dan reduksi dimensi (opsional).
* Pendekatan deep clustering untuk menghasilkan representasi fitur sebelum klasterisasi.
* Hasil berupa kelompok nasabah dengan karakteristik berbeda, seperti:

  * *High Spenders*
  * *Installment Users*
  * *Low Activity Customers*
  * *Cash Advance Heavy Users*

---

## ** 2. Project Overview**

### **2.1 Objectives**

Membangun pipeline deep learning yang komprehensif untuk:

1. **Memprediksi transaksi fraud.**
2. **Mengestimasi tahun rilis lagu.**
3. **Mengelompokkan pelanggan berdasarkan perilaku penggunaan kartu kredit.**

Hal yang dipraktekkan:

* Data cleaning & preprocessing
* Feature scaling
* Handling missing values dan outliers
* Pembangunan model ANN
* Evaluasi sesuai task
* Visualisasi dan interpretasi hasil

---

### **2.2 Implemented Tasks**

#### **Fraud Detection – Binary Classification**

* Target: `isFraud`
* Fitur: nilai transaksi, waktu, info kartu, kode produk, dll.
* Output: probabilitas transaksi merupakan fraud.

#### **Song Year Prediction – Regression**

* Target: tahun rilis lagu.
* Fitur: representasi numerik berbasis karakteristik audio.
* Model: ANN regresi dengan beberapa dense layers.

#### **Customer Clustering – Unsupervised**

* Fitur: balance, purchases, payments, credit limit, cash advance, frekuensi transaksi, dll.
* Output: cluster perilaku pengguna.

---

## ** 3. Dataset Descriptions**

### **3.1 Fraud Detection**

* **train_transaction.csv** → data berlabel
* **test_transaction.csv** → data untuk prediksi
* Label:

  * `1` = Fraud
  * `0` = Non-Fraud

### **3.2 Song Year Prediction**

* **midterm-regresi-dataset.csv**
* Kolom pertama: tahun rilis
* Kolom lainnya: fitur numerik anonim

### **3.3 Customer Clustering**

* **clusteringmidterm.csv**
* Kolom utama mencakup:

  * `BALANCE`, `PURCHASES`, `PAYMENTS`, `CASH_ADVANCE`, `CREDIT_LIMIT`, `TENURE`, dll.

---

##  4. Project Structure**

```
midterm-deep-learning/
├── data/
│   ├── train_transaction.csv
│   ├── test_transaction.csv
│   ├── midterm-regresi-dataset.csv
│   └── clusteringmidterm.csv
├── notebooks/
│   ├── fraud_detection_dl.ipynb
│   ├── regression_song_year_dl.ipynb
│   └── clustering_credit_card_dl.ipynb
├── src/
│   ├── preprocessing.py
│   ├── fraud_model.py
│   ├── regression_model.py
│   └── clustering_model.py
├── requirements.txt
└── README.md
```

