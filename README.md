# Proyek Machine Learning: Fraud Detection

## Deskripsi
Proyek submission kelas **Belajar Machine Learning untuk Pemula** di Dicoding.
Membangun model **K-Means Clustering** dan **Decision Tree Classification** pada dataset transaksi fraud detection.

## Author
**Muhammad Dhiyaul Atha**

## Struktur File
```
├── [Clustering] Submission Akhir BMLP_Muhammad Dhiyaul Atha.ipynb
├── [Klasifikasi] Submission Akhir BMLP_Muhammad Dhiyaul Atha.ipynb
├── fraud_dataset.csv
├── model_clustering.h5
├── decision_tree_model.h5
├── data_clustering.csv
└── README.md
```

## Dataset
| Info | Detail |
|------|--------|
| **Nama** | Fraud Detection Dataset |
| **Jumlah Data** | 2050 baris |
| **Jumlah Kolom** | 15 kolom |

### Kolom Dataset
| Kolom | Tipe | Keterangan |
|-------|------|------------|
| TransactionID | string | ID transaksi (di-drop) |
| AccountID | string | ID akun (di-drop) |
| DeviceID | string | ID perangkat (di-drop) |
| IPAddress | string | Alamat IP (di-drop) |
| MerchantID | string | ID merchant (di-drop) |
| TransactionDate | string | Tanggal transaksi (di-drop) |
| Amount | float | Jumlah transaksi |
| TransactionType | string | Jenis transaksi |
| Channel | string | Platform transaksi |
| CustomerAge | float | Usia pelanggan |
| CustomerGender | string | Gender pelanggan |
| LoginAttempts | int | Percobaan login |
| AccountBalance | float | Saldo rekening |
| TransactionDuration | float | Durasi transaksi (detik) |
| IsFraud | int | Label fraud (0/1) |

## Kriteria Submission

### Kriteria 1: EDA
- [x] `head()`
- [x] `info()`
- [x] `describe()`

### Kriteria 2: Preprocessing
- [x] `isnull().sum()` dan `duplicated().sum()`
- [x] `dropna()`
- [x] `drop_duplicates()`
- [x] Drop kolom ID, Address, Date
- [x] `LabelEncoder()`

### Kriteria 3: Clustering
- [x] Elbow Method
- [x] `sklearn.cluster.KMeans()`
- [x] `joblib.dump()` → `model_clustering.h5`

### Kriteria 4: Interpretasi Clustering
- [x] Analisis deskriptif (mean, min, max)
- [x] Karakteristik tiap cluster (agregasi)
- [x] Ekspor `data_clustering.csv` dengan kolom **Target**

### Kriteria 5: Klasifikasi
- [x] `train_test_split()`
- [x] Decision Tree
- [x] `joblib.dump()` → `decision_tree_model.h5`

## Library
- pandas
- numpy
- matplotlib
- scikit-learn
- joblib

## Cara Menjalankan
1. Jalankan notebook **Clustering** terlebih dahulu
2. Jalankan notebook **Klasifikasi** setelahnya
