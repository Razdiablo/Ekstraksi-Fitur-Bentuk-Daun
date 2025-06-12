# Ekstraksi-Fitur-Bentuk-Daun

Repositori ini berisi kode Python untuk melakukan **ekstraksi fitur warna, tekstur, dan bentuk** dari citra daun obat menggunakan OpenCV dan `scikit-image`. Ekstraksi dilakukan dari dataset gambar daun yang disimpan di Google Drive dan hasilnya disimpan dalam file CSV.

##  Fitur yang Diekstrak

1. **Warna (Color) - format HSV**:

   * Rata-rata dan standar deviasi dari Hue, Saturation, dan Value.

2. **Tekstur (Texture) - GLCM (Gray-Level Co-occurrence Matrix)**:

   * Contrast
   * Dissimilarity
   * Homogeneity
   * Energy
   * Correlation

3. **Bentuk (Shape)**:

   * Luas (Area)
   * Keliling (Perimeter)
   * Circularity (kebulatan bentuk)

##  Struktur Output

File output adalah `extracted_features_daun_obat.csv` dengan kolom sebagai berikut:

* `filename`
* `mean_H`, `std_H`, `mean_S`, `std_S`, `mean_V`, `std_V`
* `contrast`, `dissimilarity`, `homogeneity`, `energy`, `correlation`
* `area`, `perimeter`, `circularity`

##  Dependensi

Pastikan Anda menginstal pustaka berikut:

```bash
pip install opencv-python-headless scikit-image pandas matplotlib
```

##  Struktur Dataset

Dataset harus berada di Google Drive, misalnya:

```
/MyDrive/Colab Notebooks/Dataset Daun/train/
```

Setiap file gambar di folder ini akan diproses secara otomatis.

##  Cara Menjalankan

1. Jalankan kode ini di Google Colab.
2. Upload gambar daun yang ingin di ekstraksi.
3. Jalankan seluruh sel.

##  Visualisasi sekaligus output

Kode ini juga menyertakan visualisasi yang dijadikan sebagai output:

* Komponen HSV
* Citra grayscale untuk GLCM
* Thresholding dan labeling bentuk objek


##  Author

* Nama: *\[Isikan nama kamu]*
* Project oleh: *\[Tulis institusi/kegiatan jika terkait, misalnya tugas Computer Vision]*

Berikut adalah struktur direktori minimal dan file `requirements.txt` yang kamu butuhkan agar proyek ini rapi dan siap diunggah ke GitHub:

---

##  Struktur Direktori

```
ekstraksi-fitur-daun/
├── README.md
├── requirements.txt
├── ekstraksi_fitur_daun.py
├── extracted_features_daun_obat.csv  # (akan muncul setelah dijalankan)
└── sample_images/                    # opsional, bisa isi contoh gambar daun
````````````````````````````````````````````````````````````````````````````````````````````````

##  requirements.txt

```txt
opencv-python-headless
scikit-image
pandas
matplotlib
numpy
```

> Gunakan `opencv-python-headless` untuk menghindari error pada lingkungan server (seperti Colab atau CI/CD).

---

##  dataset
https://www.kaggle.com/datasets/riteshranjansaroj/segmented-medicinal-leaf-images
