# Rekomendasi-Negara

# Clustering the Countries using K-Means for HELP International

### Author: Bagas Eko Tjahyono Putro

---

## Table of Contents
1. [Background](#background)
2. [Dataset Description](#dataset-description)
3. [Feature Selection](#feature-selection)
4. [Data Handling](#data-handling)
   - [Missing Values](#missing-values)
   - [Outliers](#outliers)
5. [Data Analysis](#data-analysis)
   - [Univariate Analysis](#univariate-analysis)
   - [Bivariate Analysis](#bivariate-analysis)
6. [Clustering](#clustering)
   - [Determining Number of Clusters](#determining-number-of-clusters)
   - [K-Means Clustering](#k-means-clustering)
7. [Recommendations](#recommendations)
8. [Visualizations](#visualizations)

---

## Background

HELP International adalah LSM kemanusiaan internasional yang berkomitmen untuk memerangi kemiskinan dan menyediakan fasilitas serta bantuan dasar bagi masyarakat di negara-negara terbelakang saat terjadi bencana. Proyek ini bertujuan untuk membantu CEO HELP International dalam memutuskan alokasi dana sebesar $10 juta secara strategis dan efektif, berdasarkan analisis mendalam terhadap faktor-faktor sosial ekonomi dan kesehatan yang mempengaruhi perkembangan negara-negara.

## Dataset Description

Dataset terdiri dari 167 baris dan 10 kolom yang berisi informasi berikut:
- **Negara**: Nama negara
- **Kematian_anak**: Kematian anak di bawah usia 5 tahun per 1000 kelahiran
- **Ekspor**: Ekspor barang dan jasa per kapita
- **Kesehatan**: Total pengeluaran kesehatan per kapita
- **Impor**: Impor barang dan jasa per kapita
- **Pendapatan**: Penghasilan bersih per orang
- **Inflasi**: Tingkat pertumbuhan tahunan dari Total GDP
- **Harapan_hidup**: Jumlah tahun rata-rata seorang anak yang baru lahir akan hidup jika pola kematian saat ini tetap sama
- **Jumlah_fertiliti**: Jumlah anak yang akan lahir dari setiap wanita jika tingkat kesuburan usia saat ini tetap sama
- **GDPperkapita**: GDP per kapita, dihitung sebagai Total GDP dibagi dengan total populasi

## Feature Selection

Fitur yang dipilih untuk analisis dan clustering adalah:
- **Pendapatan**
- **Kesehatan**

Alasan pemilihan kedua fitur ini adalah karena tingkat pendapatan dan kesehatan merupakan indikator utama dalam pembangunan di suatu negara, sehingga dapat menjadi dasar yang kuat untuk menentukan prioritas bantuan.

## Data Handling

### Missing Values
Setelah dilakukan pengecekan, tidak terdapat missing values pada dataset.

### Outliers
Pengecekan outliers dilakukan menggunakan boxplot. Metode winsorize digunakan untuk menghandle outliers, menggantikan nilai outliers dengan nilai-nilai pada batas tertentu dari distribusi data.

## Data Analysis

### Univariate Analysis
Analisis univariate dilakukan untuk memahami distribusi masing-masing variabel.

### Bivariate Analysis
Uji korelasi pearson antara variabel pendapatan dan kesehatan menunjukkan nilai sebesar 0.252, yang menunjukkan korelasi cukup rendah antara kedua variabel.

## Clustering

### Determining Number of Clusters
Jumlah cluster yang optimal ditentukan menggunakan metode Elbow. Grafik Elbow menunjukkan bahwa jumlah cluster yang efektif adalah 4.

### K-Means Clustering
Negara-negara dikelompokkan menjadi 4 cluster berdasarkan pendapatan dan harapan hidup:
- **Cluster 1 (biru)**: Negara dengan indeks pembangunan rendah
- **Cluster 2 (hijau)**: Negara dengan indeks pembangunan sedang
- **Cluster 3 (merah)**: Negara dengan indeks pembangunan sedang
- **Cluster 4 (kuning)**: Negara dengan indeks pembangunan tinggi

## Recommendations

Negara-negara yang direkomendasikan untuk mendapatkan bantuan:
- **Niger**: Negara di Afrika Barat dengan ibu kota Niamey
- **Central African Republic**: Negara di jantung Afrika
- **Mozambique**: Negara di bagian tenggara Afrika dengan ibu kota Maputo

## Visualizations

Visualisasi data dilakukan menggunakan heatmap untuk menunjukkan korelasi antar variabel.

---
