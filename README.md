# Apel vs Tomat – Transfer Learning Image Classification

Tugas ini merupakan bagian dari mata kuliah Deep Learning, di mana saya membangun model klasifikasi gambar untuk dua objek berbeda: Apel dan Tomat menggunakan metode Transfer Learning.

## Deskripsi Proyek

Proyek ini menggunakan pendekatan Transfer Learning dengan pretrained model (kemungkinan VGG16/ResNet50) untuk membedakan gambar Apel dan Tomat berdasarkan dataset yang dikumpulkan dan diunggah ke Kaggle. Dataset ini memuat gambar dengan berbagai variasi warna, bentuk, dan sudut pengambilan untuk masing-masing kelas.

## Tools & Library

- Python
- Google Colab
- TensorFlow & Keras
- NumPy, Pandas, Matplotlib
- Scikit-learn
- Kaggle API

## Model Transfer Learning

- Model: Pretrained CNN (misalnya VGG16 atau ResNet50)
- Strategi:
  - Layer awal dibekukan (frozen)
  - Ditambahkan Dense layer untuk klasifikasi 2 kelas
  - Optimizer: Adam
  - Loss function: Binary Crossentropy
  - Metric: Accuracy

## Dataset

- Jumlah total: 200+ gambar
  - Apel: ±100 gambar
  - Tomat: ±100 gambar
- Sumber: Dataset pribadi di Kaggle
- Format: JPG/PNG
- Ukuran gambar: Diresize ke (224, 224)
- Split data:
  - 80% training
  - 20% validation

## Hasil & Evaluasi

- **Akurasi validasi akhir:** 99.00%
- **Confusion Matrix:**

  |        | Pred Apel | Pred Tomat |
  |--------|-----------|------------|
  | Apel   | 98        | 2          |
  | Tomat  | 0         | 100        |

- **Classification Report:**

  | Class     | Precision | Recall | F1-Score | Support |
  |-----------|-----------|--------|----------|---------|
  | Apple     | 1.00      | 0.98   | 0.99     | 100     |
  | Tomato    | 0.98      | 1.00   | 0.99     | 100     |
  | **Accuracy**  |           |        | **0.99**  | **200**   |
  
- Visualisasi:
  - Grafik akurasi dan loss selama training
    ![akurasi](https://github.com/user-attachments/assets/05884845-6a94-4e0d-b566-5d997a7f439d)
    ![loss](https://github.com/user-attachments/assets/7ec54f01-5e66-413e-bd4a-ff5645eac96a)

## Refleksi Pribadi

Saya mempelajari bagaimana memanfaatkan model pretrained untuk melakukan klasifikasi gambar, serta pentingnya preprocessing dan split data yang baik. Tantangan utama dalam proyek ini adalah menyusun dataset yang seimbang dan menghindari overfitting. Proyek ini meningkatkan pemahaman saya tentang alur kerja deep learning berbasis citra.

## File dalam Repository

| Nama File             | Deskripsi                                    |
|-----------------------|----------------------------------------------|
| apelvstomat.ipynb     | Notebook utama berisi seluruh proses coding  |
| README.md             | Deskripsi proyek ini                         |
| laporan.pdf (opsional)| Laporan lengkap jika diperlukan              |

## Link Tugas

- GitHub Repo: [https://github.com/adykim/apel-vs-tomat](https://github.com/adykim/apel-vs-tomat)
