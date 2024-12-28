# Digital Image Processing - Final Project
## Group Members
- Syehan Fariz Gustomo - 1301210530
- Naufal Geo Pastrana - 1301213083
- Akmal Sidki Razaka - 1301210547

# Object Detection for Car and Ambulance Identification

This repository contains a Jupyter Notebook (`.ipynb`) that demonstrates a machine learning workflow to classify images of vehicles as either **regular cars** or **ambulances**. The project involves data preprocessing, feature extraction, and classification using state-of-the-art algorithms.

## Overview
This project focuses on object detection to identify whether a given image contains a regular car or an ambulance. The workflow includes:
- Image preprocessing with labeling.
- Feature extraction using ORB (Oriented FAST and Rotated BRIEF) and HOG (Histogram of Oriented Gradients).
- Classification using Support Vector Machines (SVM).

The approach is designed to handle real-world datasets with diverse scenarios, making it suitable for practical applications like traffic monitoring or emergency vehicle detection.

## Dataset
The dataset used in this project is sourced from Kaggle. It includes:
- Images of **sedans** categorized as regular cars.
- Images of **ambulances**.

## Dependencies
The following libraries and tools are required to run this project:
- Python 3.7+
- Jupyter Notebook
- NumPy
- OpenCV
- Scikit-learn
- Matplotlib

## Workflow
### Data Preprocessing
1. **Labeling:**
   - Images are pre-labeled based on their directory structure (e.g., `cars` and `ambulances`).
   - Each image is resized and converted to grayscale for uniformity and reduced computational load.

2. **Augmentation (Optional):**
   - Basic transformations like rotation, flipping, or scaling can be applied to increase dataset diversity.

### Feature Extraction
Two feature extraction techniques are utilized:
1. **ORB (Oriented FAST and Rotated BRIEF):**
   - Detects keypoints and computes descriptors, which are invariant to scaling and rotation.
   - Suitable for identifying unique patterns in vehicle shapes and details.

2. **HOG (Histogram of Oriented Gradients):**
   - Extracts features based on edge direction and intensity distribution.
   - Effective for capturing the overall shape and structure of vehicles.

### Classification
1. **SVM (Support Vector Machine):**
   - Trains a classifier using features extracted from ORB and HOG.
   - Uses a linear or RBF kernel for robust classification.
   - Outputs whether the input image is a regular car or an ambulance.

### Cara Kerja Notebook
1. **Persiapan Data:**
   - Dataset disimpan di Google Drive, terdiri dari gambar sedan dan ambulans. Struktur direktori memisahkan gambar berdasarkan labelnya.
   - Fungsi `plot_sample_images` digunakan untuk menampilkan beberapa contoh gambar dari dataset untuk memverifikasi data input.

2. **Pelabelan Data:**
   - Notebook mencocokkan setiap gambar dengan label dalam file teks terpisah. Fungsi `plot_images_with_labels` menampilkan gambar beserta label yang sesuai untuk memastikan proses pelabelan benar.

3. **Preprocessing dan Visualisasi:**
   - Gambar diubah ke format seragam, seperti ukuran dan warna, untuk memastikan konsistensi data.
   - Dataset yang bersih ditampilkan untuk memberikan gambaran visual dan memastikan kualitas data.

4. **Feature Extraction:**
   - Algoritma ORB dan HOG digunakan untuk mengambil fitur unik dari gambar.

5. **Klasifikasi:**
   - Model SVM membedakan antara sedan (mobil biasa) dan ambulans berdasarkan fitur yang diekstraksi.

6. **Evaluasi Model:**
   - Evaluasi menggunakan metrik seperti akurasi dan laporan klasifikasi.
