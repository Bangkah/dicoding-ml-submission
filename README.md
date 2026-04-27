# Proyek Machine Learning: Bank Transaction Fraud Detection

## Deskripsi
Proyek submission kelas **Belajar Machine Learning untuk Pemula** di Dicoding.
Membangun model **K-Means Clustering** dan **Decision Tree Classification** pada dataset Bank Transaction untuk mendeteksi pola transaksi.

## Author
**Muhammad Dhiyaul Atha**

---

## Struktur File

```
├── [Clustering] Submission Akhir BMLP_Muhammad Dhiyaul Atha.ipynb
├── [Klasifikasi] Submission Akhir BMLP_Muhammad Dhiyaul Atha.ipynb
├── bank_transactions_data_edited.csv
├── model_clustering
├── PCA_model_clustering.h5
├── data_clustering.csv
├── data_clustering_inverse.csv
├── decision_tree_model.h5
├── explore_random_forest_classification
├── tuning_classification
└── README.md
```

---

## Dataset

| Info | Detail |
|------|--------|
| **Nama** | Bank Transactions Data (Edited) |
| **Sumber** | Dicoding (modifikasi dari Kaggle) |
| **Jumlah Data** | 2537 baris |
| **Jumlah Kolom** | 16 kolom |

### Kolom Dataset
| Kolom | Tipe | Keterangan |
|-------|------|------------|
| TransactionID | string | ID transaksi (di-drop) |
| AccountID | string | ID akun (di-drop) |
| TransactionAmount | float | Jumlah transaksi |
| TransactionDate | string | Tanggal transaksi (di-drop) |
| TransactionType | string | Jenis transaksi (Debit/Credit) |
| Location | string | Lokasi transaksi |
| DeviceID | string | ID perangkat (di-drop) |
| IP Address | string | Alamat IP (di-drop) |
| MerchantID | string | ID merchant (di-drop) |
| Channel | string | Platform (ATM/Online) |
| CustomerAge | float | Usia pelanggan |
| CustomerOccupation | string | Pekerjaan pelanggan |
| TransactionDuration | float | Durasi transaksi (detik) |
| LoginAttempts | float | Percobaan login |
| AccountBalance | float | Saldo rekening |
| PreviousTransactionDate | string | Tanggal transaksi sebelumnya (di-drop) |

---

## Kriteria Submission

### Kriteria 1: EDA
- [x] `head()`, `info()`, `describe()`
- [x] Matriks korelasi (heatmap)
- [x] Histogram semua kolom (numerik & kategorikal)
- [x] Visualisasi tanpa label overlap

### Kriteria 2: Preprocessing
- [x] `isnull().sum()` dan `duplicated().sum()`
- [x] `dropna()` dan `drop_duplicates()`
- [x] Drop kolom ID, Address, Date
- [x] `LabelEncoder()` untuk fitur kategorikal
- [x] Handling Outlier (metode IQR drop)
- [x] `StandardScaler()` untuk fitur numerik
- [x] Binning data (CustomerAge & TransactionAmount)

### Kriteria 3: Clustering
- [x] Elbow Method (`KElbowVisualizer()`)
- [x] K-Means Clustering (`sklearn.cluster.KMeans()`)
- [x] `joblib.dump()` → `model_clustering`
- [x] Silhouette Score
- [x] Visualisasi cluster (PCA 2D)
- [x] PCA Model → `PCA_model_clustering.h5`

### Kriteria 4: Interpretasi Clustering
- [x] Analisis deskriptif (mean, min, max)
- [x] Karakteristik tiap cluster (agregasi)
- [x] `inverse_transform()` untuk data asli
- [x] Analisis numerik & kategorikal setelah inverse
- [x] Ekspor `data_clustering.csv` + kolom Target
- [x] Ekspor `data_clustering_inverse.csv`

### Kriteria 5: Klasifikasi
- [x] `train_test_split()` (80:20)
- [x] Decision Tree → `decision_tree_model.h5`
- [x] Random Forest → `explore_random_forest_classification`
- [x] Evaluasi: Accuracy, Precision, Recall, F1-Score
- [x] Hyperparameter Tuning (GridSearchCV) → `tuning_classification`

---

## Library

| Library | Kegunaan |
|---------|----------|
| pandas | Manipulasi data |
| numpy | Operasi numerik |
| matplotlib | Visualisasi |
| seaborn | Visualisasi statistik |
| scikit-learn | Machine Learning |
| yellowbrick | Visualisasi ML (Elbow, Silhouette) |
| joblib | Menyimpan model |

---

## Cara Menjalankan

```bash
# 1. Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn yellowbrick joblib

# 2. Jalankan notebook Clustering TERLEBIH DAHULU
jupyter notebook "[Clustering] Submission Akhir BMLP_Muhammad Dhiyaul Atha.ipynb"

# 3. Setelah selesai, jalankan notebook Klasifikasi
jupyter notebook "[Klasifikasi] Submission Akhir BMLP_Muhammad Dhiyaul Atha.ipynb"
```

---

## Hasil Model

### Clustering
- Algoritma: **K-Means**
- Evaluasi: **Silhouette Score**
- Perbandingan: K-Means vs K-Means + PCA

### Klasifikasi
| Model | Keterangan |
|-------|------------|
| **Decision Tree** | Model utama |
| **Random Forest** | Model eksplorasi tambahan |
| **Tuned Decision Tree** | Setelah hyperparameter tuning |

---

## File Output

| File | Keterangan |
|------|------------|
| `model_clustering` | Model K-Means |
| `PCA_model_clustering.h5` | Model K-Means + PCA |
| `data_clustering.csv` | Data + kolom Target |
| `data_clustering_inverse.csv` | Data inverse + Target |
| `decision_tree_model.h5` | Model Decision Tree |
| `explore_random_forest_classification` | Model Random Forest |
| `tuning_classification` | Model setelah tuning |

---

## Lisensi
Proyek ini dibuat untuk submission di [Dicoding Indonesia](https://www.dicoding.com/).