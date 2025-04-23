# 🌸 Iris Flower Classification

## 💡 Deskripsi
Proyek ini bertujuan mengeksplorasi **Iris Dataset** serta membangun dan membandingkan enam model klasifikasi untuk memprediksi spesies bunga Iris (setosa, versicolor, virginica) berdasarkan empat fitur morfologi (panjang & lebar sepal, panjang & lebar petal).

### Algoritma yang Diuji
1. **Logistic Regression**  
2. **Support Vector Machine** (kernel RBF)  
3. **Decision Tree** (CART)  
4. **K-Nearest Neighbors** (KNN)  
5. **Gaussian Naïve Bayes** (NB)  
6. **AdaBoost** (10 decision stump)

---

## 🔧 Detail Pelatihan
| Langkah | Rincian |
|---------|---------|
| **Pembagian Data** | 70 % pelatihan &nbsp;/&nbsp; 30 % pengujian (stratified) |
| **Validasi Silang** | Stratified K-Fold 10 fold pada set pelatihan |
| **Metrik Evaluasi** | Akurasi (utama), precision, recall, dan F1-score per kelas |
| **Pra-setel Utama** | <ul><li>LR: *liblinear*, regulasi L2</li><li>SVM: kernel RBF, γ = auto</li><li>DT: parameter baku CART</li><li>KNN: *k* = 5 (baku)</li><li>NB: Gaussian prior baku</li><li>AdaBoost: 10 decision stump</li></ul> |

---

## 📊 Ringkasan Hasil

| Model | CV Accuracy (mean ± std) | Test Accuracy | Catatan Confusion Matrix |
|-------|--------------------------|---------------|--------------------------|
| **Logistic Regression** | **95.2 % ± 4.8 %** | **97.8 %** | 1 *versicolor* salah → *virginica* |
| **SVM (RBF)** | **94.4 % ± 4.6 %** | **100 %** | Prediksi tepat untuk semua kelas |
| **Decision Tree** | **92.4 % ± 5.6 %** | **100 %** | Tidak ada kesalahan klasifikasi |
| **K-Nearest Neighbors** | **93.4 % ± 6.0 %** | **100 %** | Tidak ada kesalahan klasifikasi |
| **Gaussian Naïve Bayes** | **92.3 % ± 8.7 %** | **97.8 %** | Pola kesalahan identik dengan LR |
| **AdaBoost (10 stump)** | **≈ 95–96 %** | **100 %** | Ensemble boosting; klasifikasi sempurna |

> **Kesimpulan:**  
> SVM, Decision Tree, KNN, dan AdaBoost mencapai akurasi 100 % pada data uji, menandakan bahwa metode margin-based, pohon keputusan sederhana, model *instance-based*, maupun ensemble boosting sama-sama cukup kuat pada dataset Iris yang relatif mudah. Logistic Regression dan Gaussian NB tetap kompetitif, meski mengalami sedikit kesalahan pada kelas *versicolor*.

---
