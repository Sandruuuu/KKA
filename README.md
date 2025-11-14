# Praktikum Analisis Data Lanjutan - Analisis Penjualan Produk Elektronik

Repositori ini berisi *notebook* Jupyter (`Praktikum_Lanjutan_Analisis_Data.ipynb`) untuk praktikum KKA Analisis Data Lanjutan. Analisis ini berfokus pada data penjualan produk elektronik untuk mengidentifikasi tren pendapatan dan menganalisis performa masing-masing produk.

## 📖 Deskripsi

Analisis ini bertujuan untuk menjawab beberapa pertanyaan bisnis utama:
* Bagaimana tren pendapatan penjualan mingguan sepanjang tahun 2024?
* Produk mana yang paling banyak terjual secara kuantitas?
* Produk mana yang menghasilkan pendapatan bersih (net income) paling tinggi?
* Bagaimana perbandingan antara kuantitas penjualan dan pendapatan bersih untuk setiap produk?

## 💾 Dataset

Dataset yang digunakan adalah data transaksi penjualan (diasumsikan dari file `data.csv` yang ada di repositori) yang mencakup beberapa kolom utama:
* `Tanggal` (Tanggal transaksi)
* `Produk` (Kategori produk, misal: Laptop, Mouse, Keyboard, Monitor, Headset)
* `Jumlah` (Jumlah unit yang terjual)
* `Pendapatan` (Total pendapatan dari transaksi)
* (Kemungkinan) `Pendapatan Bersih` (Pendapatan setelah dikurangi biaya/modal)

## 🛠️ Library yang Digunakan

Analisis ini menggunakan *library* standar Python untuk analisis data:
* **Pandas:** Untuk manipulasi dan agregasi data.
* **Matplotlib:** Untuk membuat visualisasi data.
* **Seaborn:** Untuk membuat visualisasi data yang lebih menarik dan informatif (seperti bar plot dengan *error bar*).
* **NumPy:** (Kemungkinan digunakan) untuk operasi numerik.

## 📈 Hasil Analisis & Visualisasi

Berikut adalah beberapa temuan kunci dari analisis yang dilakukan, berdasarkan output visualisasi:

### 1. Tren Pendapatan Mingguan

![Tren Pendapatan Mingguan](https://github.com/Sandruuuu/KKA/blob/f87c6089fd4c582e7cf623ce2c0e8f1a88b43cb4/Screenshot%202025-11-14%20at%2009-33-16%20KKA_Praktikum_Lanjutan_Analisis_Data.ipynb%20at%20main%20%C2%B7%20Sandruuuu_KKA.png)

Grafik *line plot* ini menunjukkan fluktuasi total pendapatan per minggu selama tahun 2024 (dari Januari hingga Juli).

* **Deskripsi Output:** Tren pendapatan terlihat sangat fluktuatif. Terdapat dua puncak (lonjakan) pendapatan yang sangat signifikan:
    1.  Satu puncak tertinggi terjadi sekitar akhir Maret 2024 (sekitar 2024-03-24).
    2.  Puncak signifikan kedua terjadi sekitar akhir April 2024 (sekitar 2024-04-21).
* **Wawasan (Insight):** Perlu investigasi lebih lanjut untuk memahami apa yang menyebabkan lonjakan besar pada dua periode tersebut (misal: program promosi, liburan, atau penjualan proyek besar).

### 2. Analisis Kuantitas Produk Terjual

![Jumlah Produk Terjual](https://github.com/Sandruuuu/KKA/blob/f87c6089fd4c582e7cf623ce2c0e8f1a88b43cb4/Screenshot%202025-11-14%20at%2009-33-10%20KKA_Praktikum_Lanjutan_Analisis_Data.ipynb%20at%20main%20%C2%B7%20Sandruuuu_KKA.png)

Grafik *bar plot* ini membandingkan rata-rata jumlah (kuantitas) unit yang terjual untuk setiap kategori produk.

* **Deskripsi Output:**
    * **Monitor** adalah produk yang paling banyak terjual secara kuantitas (rata-rata tertinggi).
    * **Keyboard** dan **Mouse** berada di posisi kedua dan ketiga dalam hal kuantitas penjualan.
    * **Headset** memiliki jumlah penjualan menengah ke bawah.
    * **Laptop** adalah produk dengan kuantitas penjualan rata-rata terendah.
* **Wawasan (Insight):** Produk aksesoris (Monitor, Keyboard, Mouse) terjual dalam volume yang tinggi, sementara produk utama (Laptop) terjual dalam volume yang lebih rendah.

### 3. Analisis Pendapatan Bersih per Produk

![Pendapatan Bersih per Produk](https://github.com/Sandruuuu/KKA/blob/f87c6089fd4c582e7cf623ce2c0e8f1a88b43cb4/Screenshot%202025-11-14%20at%2009-33-27%20KKA_Praktikum_Lanjutan_Analisis_Data.ipynb%20at%20main%20%C2%B7%20Sandruuuu_KKA.png)

Grafik *bar plot* ini membandingkan rata-rata pendapatan bersih (profit) yang dihasilkan oleh setiap kategori produk.

* **Deskripsi Output:**
    * **Laptop** menghasilkan rata-rata pendapatan bersih tertinggi secara signifikan, jauh di atas produk lainnya.
    * **Monitor** berada di posisi kedua, menghasilkan pendapatan bersih yang cukup baik.
    * **Mouse**, **Keyboard**, dan **Headset** menghasilkan pendapatan bersih yang relatif sangat kecil per unitnya.
* **Wawasan (Insight):** Terdapat kontras yang jelas dengan analisis kuantitas. Meskipun Laptop terjual dalam jumlah sedikit (Grafik 2), produk ini adalah penghasil profit utama (Grafik 3).

## 💡 Kesimpulan Utama

Analisis ini menunjukkan strategi produk yang berbeda:

1.  **Produk "High-Margin" (Margin Tinggi):** **Laptop** adalah produk *high-margin, low-volume*. Meskipun penjualannya tidak sering, setiap penjualan memberikan kontribusi profit yang sangat besar.
2.  **Produk "High-Volume" (Volume Tinggi):** **Monitor**, **Keyboard**, dan **Mouse** adalah produk *low-margin, high-volume*. Produk ini terjual banyak namun kontribusi profit per unitnya kecil.

Strategi bisnis dapat disesuaikan berdasarkan temuan ini, misalnya dengan melakukan *bundling* produk *high-volume* (Mouse, Keyboard) dengan produk *high-margin* (Laptop) untuk meningkatkan nilai total penjualan.

## 🚀 Cara Menjalankan Notebook

Untuk menjalankan notebook ini di lingkungan lokal Anda:

1.  **Clone repositori ini:**
    ```bash
    git clone [https://github.com/Sandruuuu/KKA.git](https://github.com/Sandruuuu/KKA.git)
    cd KKA
    ```

2.  **Install dependensi yang diperlukan:**
    ```bash
    pip install pandas matplotlib seaborn jupyter
    ```

3.  **Buka Jupyter Notebook:**
    ```bash
    jupyter notebook Praktikum_Lanjutan_Analisis_Data.ipynb
    ```
