# Tool-Wear-Failure-Model

# Prediksi Kegagalan Keausan Alat (Tool Wear Failure) Menggunakan Logistic Regression

Proyek ini bertujuan untuk memprediksi kegagalan keausan alat (Tool Wear Failure, TWF) pada mesin penggilingan menggunakan model pembelajaran mesin. Dengan prediksi yang lebih awal, kita dapat mengurangi waktu henti produksi dan biaya perawatan secara signifikan.

## 1. Deskripsi Proyek

**Tujuan:** Mengembangkan model pembelajaran mesin untuk memprediksi kegagalan keausan alat berdasarkan data sensor.  
**Algoritma:** Logistic Regression  
**Data:** Data sensor yang mencakup suhu udara, suhu proses, kecepatan rotasi, torsi, dan keausan alat.

Model Logistic Regression ini memberikan akurasi prediksi pada data pengujian sebesar XX.XX%. Hasil ini menunjukkan bahwa model dapat digunakan untuk memprediksi kegagalan keausan alat dengan cukup akurat.

Penggunaan Logistic Regression dalam prediksi kegagalan keausan alat menunjukkan hasil yang memuaskan. Dengan pengaturan yang lebih optimal dan pengolahan data tambahan, performa model dapat ditingkatkan lebih lanjut.

## 2. Data

Kami menggunakan data sensor dari mesin penggilingan yang mencakup kolom berikut:
- **Air temperature (Suhu Udara):** Suhu udara di sekitar mesin.
- **Process temperature (Suhu Proses):** Suhu proses pada mesin.
- **Rotational speed (Kecepatan Rotasi):** Kecepatan putar mesin dalam RPM.
- **Torque (Torsi):** Torsi yang diterapkan pada mesin.
- **Tool wear (Keausan Alat):** Ukuran keausan alat.

## 3. Pendekatan

### 3.1 Pembagian Data

Data dibagi menjadi data pelatihan dan data pengujian dengan proporsi 80% untuk pelatihan dan 20% untuk pengujian menggunakan `train_test_split` dari scikit-learn.

```python
from sklearn.model_selection import train_test_split

# Membagi data
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
