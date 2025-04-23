# Iris Flower Classification

## 💡 Deskripsi
Proyek ini melakukan eksplorasi data (EDA) dan pembangunan model klasifikasi pada **Iris Dataset** menggunakan tiga algoritma:  
1. Logistic Regression  
2. Support Vector Machine (SVM)  
3. AdaBoost  

Tujuan utama adalah membandingkan kinerja ketiga model tersebut dalam memprediksi spesies bunga Iris berdasarkan empat fitur morfologi.

# Ringkasan Hasil

| Model               | CV Accuracy | Test Accuracy | Keterangan                             |
|---------------------|-------------|---------------|----------------------------------------|
| Logistic Regression | 95.2%       | 97.8%         | 1 kesalahan pada kelas Versicolor      |
| SVM                 | 94.4%       | 100%          | Margin-based, stabil                   |
| AdaBoost            | 95–96%      | 100%          | Ensemble boosting, stabil dan cepat    |

