# Visualisasi Algoritma Minimum Spanning Tree (MST) pada 38 Provinsi di Indonesia

Proyek ini bertujuan untuk memvisualisasikan proses pembentukan **Minimum Spanning Tree (MST)** menggunakan **Algoritma Prim** dan **Algoritma Kruskal**. Studi kasus yang digunakan adalah membuat jaringan konektivitas minimum antar ibu kota provinsi di seluruh Indonesia.

Program ini akan mengambil data geografis provinsi di Indonesia, menghitung jarak antar ibu kota provinsi menggunakan rumus Haversine, dan kemudian membangun MST. Hasil dari kedua algoritma divisualisasikan sebagai animasi interaktif di atas peta menggunakan `folium`, yang kemudian disimpan sebagai file HTML.

---

## Fitur

* **Ekstraksi Data Geografis**: Secara otomatis membaca file `shapefile` untuk mendapatkan daftar provinsi dan koordinat ibu kotanya.
* **Pembangunan Graf Lengkap**: Membangun sebuah graf lengkap di mana setiap provinsi adalah simpul dan bobot antar simpul adalah jarak sebenarnya di permukaan bumi (jarak Haversine).
* **Implementasi MST**: Menggunakan dua algoritma klasik untuk mencari MST:
    * **Algoritma Prim**: Membangun pohon dari satu titik awal dan secara bertahap menambahkan sisi terpendek.
    * **Algoritma Kruskal**: Mengurutkan semua sisi dan menambahkannya satu per satu selama tidak membentuk siklus.
* **Visualisasi Animasi**: Menghasilkan peta interaktif (`.html`) yang menampilkan proses pembentukan MST langkah demi langkah untuk setiap algoritma.
* **Perhitungan Jarak Total**: Menampilkan total jarak (dalam km) dari MST yang dihasilkan oleh kedua algoritma.

---

## 🚀 Cara Menjalankan

1.  **Siapkan Dependensi**:
    Pastikan Anda memiliki Python dan `pip` terinstal. Instal semua pustaka yang diperlukan dengan menjalankan:
    ```bash
    pip install -r requirements.txt
    ```
    *Catatan: `geopandas` mungkin memerlukan dependensi tambahan seperti `gdal` atau `fiona`. Silakan merujuk ke [dokumentasi instalasi GeoPandas](https://geopandas.org/en/stable/getting_started/install.html) untuk panduan spesifik sistem operasi Anda.*

2.  **Unduh Data Shapefile**:
    Program ini memerlukan data `shapefile` untuk batas administrasi negara. Anda bisa mengunduh data yang digunakan dalam proyek ini dari [Natural Earth](https://www.naturalearthdata.com/downloads/10m-cultural-vectors/10m-admin-1-states-provinces/).
    - Unduh file "10m Admin 1 – States, Provinces".
    - Ekstrak file ZIP tersebut ke dalam direktori proyek Anda.

3.  **Jalankan Skrip**:
    Buka skrip Python dan pastikan variabel `SHAPEFILE_PATH` menunjuk ke lokasi file `.shp` yang benar.
    ```python
    SHAPEFILE_PATH = '/path/to/your/ne_10m_admin_1_states_provinces.shp'
    ```
    Jalankan skrip dari terminal:
    ```bash
    python nama_file_skrip_anda.py
    ```
    *Jika Anda menggunakan lingkungan seperti Jupyter Notebook atau Google Colab, cukup jalankan sel kode seperti biasa.*

4.  **Lihat Hasil**:
    Setelah eksekusi selesai, dua file HTML akan dibuat di direktori yang sama:
    * `prim_mst_animation.html`
    * `kruskal_mst_animation.html`
    Buka file-file ini di peramban web Anda untuk melihat visualisasi animasi MST yang interaktif. Total jarak MST untuk setiap algoritma juga akan dicetak di konsol.
