# Machine Learning Final Project - Dicoding

## Deskripsi Proyek

Proyek ini merupakan tugas akhir dari kelas Machine Learning di Dicoding. Dalam proyek ini, saya melakukan analisis data dengan metode *clustering* serta membangun model *classification* berdasarkan hasil klasterisasi yang telah dilakukan. Dataset yang digunakan adalah dataset mengenai rating coklat batangan yang didapat dari Kaggle : https://www.kaggle.com/datasets/evangower/chocolate-bar-ratings



Proses utama dalam proyek ini meliputi:

1. **Pencarian Dataset** - Pemilihan dataset yang sesuai untuk diterapkan metode *clustering* dan *classification*.
3. **Clustering** - Pengelompokan data menggunakan metode *unsupervised learning* dan membangun model clustering.
4. **Classification** - Membangun model *supervised learning* untuk mengklasifikasikan hasil klasterisasi.
5. **Evaluasi Model** - Melakukan evaluasi terhadap performa model untuk memastikan hasil yang optimal.

Proyek ini mendapatkan skor **5/5** dalam penilaian.

## Struktur Repository

- `Chocolate.ipynb` : Notebook yang berisi proses *clustering* pada dataset.
- `Chocolate_DT.ipynb` : Notebook yang berisi proses *classification* menggunakan *Decision Tree* berdasarkan hasil klasterisasi.

## Hasil dan Evaluasi

![image](https://github.com/user-attachments/assets/09a354ea-dade-4561-b127-42a2689a9291)


### Model Clustering
Model akhir didapat menggunakan metode KMeans dengan **silhouette score** = 0.7607.

### Analisis Clustering

#### Cluster 0:
- **Persentase cocoa**: range 60-100%, rata-rata 73%
- **Jumlah bahan**: range 1-3, rata-rata 2 bahan
- **Rata-rata rating**: 3.19

#### Cluster 1:
- **Persentase cocoa**: range 42-91%, rata-rata 69%
- **Jumlah bahan**: range 3-6, rata-rata 4 bahan
- **Rata-rata rating**: 3.12

#### Cluster 2:
- **Persentase cocoa**: range 58-99%, rata-rata 71%
- **Jumlah bahan**: range 3-4, rata-rata 3 bahan
- **Rata-rata rating**: 3.24

### Insight dari hasil clustering:
Beberapa pola menarik ditemukan dari hasil clustering:

- Cluster 0 dan Cluster 2 memiliki persentase cocoa dan rating yang mirip. Namun, Cluster 2 memiliki lebih banyak bahan dibandingkan Cluster 0.
- Cluster 1 memiliki persentase cocoa yang lebih rendah, lebih banyak bahan, dan rating yang lebih rendah dibandingkan cluster lainnya.

Selain itu, hampir semua coklat dalam dataset menggunakan bahan dasar B, S, dan S* (Biji Kakao, Gula, dan Pemanis). Namun, Cluster 1 memiliki karakteristik yang berbeda:

- 74% coklat batangan di Cluster 1 menggunakan **L (Lechitin)**
- 52% coklat batangan di Cluster 1 menggunakan **V (Vanilla)**

Sedangkan Cluster 0 dan Cluster 2 hampir tidak menggunakan Lechitin ataupun Vanilla.
- Cluster 0 : 0.0  persen coklat batangan memakai **V (Vanilla)** dan 0.127 persen coklat batangan memakai **L (Lechitin)**
- Cluster 2 : 2.228 persen coklat batangan memakai **V (Vanilla)** dan 2.495 persen coklat batangan memakai **L (Lechitin)**


### Kesimpulan:
Dari hasil ini dapat disimpulkan bahwa rating coklat dipengaruhi oleh persentase cocoa dan bahan tambahan dalam produk. Pada dataset ini, penggunaan Lechitin dan Vanilla mungkin menyebabkan rating menurun, meskipun dampaknya tidak terlalu signifikan.


