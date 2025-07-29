# Flood Prediction Project

## Overview
Proyek ini bertujuan untuk mengembangkan model machine learning untuk prediksi banjir menggunakan teknik regresi. Proyek ini mengeksplorasi penggunaan pendekatan berbasis data untuk meningkatkan sistem peringatan dini dengan memprediksi probabilitas banjir secara terus-menerus daripada menggunakan klasifikasi biner.

## Tujuan Proyek
1. Mengembangkan model prediksi probabilitas banjir (berbasis regresi) untuk mendukung perencanaan mitigasi berbasis risiko.
2. Mengidentifikasi fitur-fitur yang paling berpengaruh, seperti intensitas curah hujan dan kepadatan penduduk.

## Metodologi
- Dataset: [Flood Prediction Dataset dari Kaggle](https://www.kaggle.com/datasets/naiyakhalid/flood-prediction-dataset) (50,000 sampel, 20 fitur).
- Membandingkan tiga model yang digunakan: Linear Regression, Gradient Boosting Regression, dan Artificial Neural Network (ANN).

## Evaluasi Model
| Model               | MSE       | RMSE   | R² |
|---------------------|----------|--------|----------|
| Linear Regression              | 1.12 × 10⁻⁵   | 0.00334  | 0.9955 |
| Gradient Boosting Regressor (GBR) | 2.41 × 10⁻⁴ | 0.0155   | 0.9028 |
| ANN (ReLU/Tanh/LeakyReLU) | 3.68 × 10⁻⁴   | 0.0192   | 0.8515 |

### Insight Utama
- Linear Regression unggul dibandingkan model lain dengan MSE terendah (`1.12e-5`) dan R² tertinggi (`0.9955`).
- Feature engineering meningkatkan relevansi fitur baru yang dibuat.
- Tidak ada overfitting. Model-model tersebut diterapkan dengan baik pada data uji.

## Tools & Teknologi
- Bahasa Pemrograman: Python
- **Libraries**:  
  - Scikit-learn (Linear Regression, GBR)  
  - TensorFlow/Keras (ANN)  
  - Pandas, NumPy (data processing)  
  - Matplotlib, Seaborn (visualization)
- **Data Normalization**: `RobustScaler`
- **Hyperparameter Tuning**: Manual tuning untuk ANN (epochs=10, learning_rate=0.01).

## Cara Menjalankan
Clone repo:
```
git clone https://github.com/nafakhairunnisa/flood-prediction-regression.git
```

Install requirements:
```
pip install pandas numpy scikit-learn tensorflow matplotlib seaborn
```

Jalankan notebook:
```
jupyter notebook Submission_Predictive_Analytics.ipynb
```

## Future Work
- Integrasi data lokal Indonesia
- Deployment sebagai web service
