# Proyek Matematika Diskret Closure Relasi dan Minimum Spanning Tree

## Tujuan
Proyek ini bertujuan untuk:
- Mengimplemnetasikan algoritma untuk memperoleh matriks **closure** dari suatu relasi
- Memvisualisasikan proses pembentukan **Minimum Spanning Tree (MST)** menggunakan **Algoritma Prim** dan **Algoritma Kruskal** dengan membuat jaringan konektivitas minimum antar ibu kota provinsi di seluruh Indonesia

## Program
**Program Closure Relasi** akan menunjukkan contoh penggunaan algoritma untuk memperoleh matriks closure relasi, sedangkan **Program MST** akan mengambil data geografis provinsi di Indonesia, menghitung jarak antar ibu kota provinsi menggunakan rumus Haversine, dan kemudian membangun MST. Hasil dari kedua algoritma divisualisasikan sebagai animasi interaktif di atas peta menggunakan `folium`, yang kemudian disimpan sebagai file HTML.

---
## Cara Menjalankan Program
1.  **Clone Repositori**
    Buka terminal atau CMD dan jalankan perintah berikut untuk mengunduh proyek:
    ```bash
    git clone https://github.com/xinuzo/Proyek_Matdis.git
    ```
    Atau, unduh proyek sebagai file ZIP dan ekstrak.

2.  **Instal Dependensi**
    Navigasikan ke dalam folder proyek yang baru saja Anda clone, lalu instal semua pustaka yang diperlukan:
    ```bash
    pip install -r requirements.txt
    ```

3.  **Jalankan Notebook**
    Buka folder `src`, lalu buka file notebook `.ipynb` menggunakan Jupyter Notebook atau VS Code. Jalankan semua sel kode dari atas ke bawah. 
    - Berkas Masalah 1: closure.ipynb 
    - Berkas Masalah 2: MST.ipynb
---

## Hasil Program

Hasil akhir dari visualisasi Minimum Spanning Tree (MST) untuk kedua algoritma dapat dilihat pada file-file berikut:
- `prim_mst_animation_38.html`
- `kruskal_mst_animation_38.html`

Buka file HTML tersebut di peramban web untuk melihat animasi interaktifnya.
