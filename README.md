# 🎓 Student Performance Analytics: Behavioral & Digital Insights
> **End-to-End Machine Learning Project: Predicting Academic Success**

## 📌 Project Overview
Proyek ini mengeksplorasi hubungan antara gaya hidup digital, kesehatan mental, dan performa akademik siswa. Dengan menganalisis 32 fitur yang mencakup aspek perilaku hingga penggunaan teknologi, kami membangun model prediktif untuk membantu institusi pendidikan mengidentifikasi siswa yang membutuhkan dukungan tambahan.

## 📁 Project Structure
- `/data`: Dataset mentah (`student_performance_dataset.csv`).
- `/images`: Galeri visualisasi hasil analisis dan evaluasi model.
- `/notebooks`: Dokumentasi kode lengkap dalam Jupyter Notebook.

---

## 📊 Data Analysis & Insights
Berdasarkan tahap **Exploratory Data Analysis (EDA)**, ditemukan beberapa temuan kunci:

1.  **Digital Distraction vs Focus:** Terdapat korelasi negatif yang signifikan antara durasi *social media* (terutama *doomscrolling*) dengan skor ujian. Sebaliknya, variabel *deep work sessions* menjadi pendorong utama keberhasilan akademik.
2.  **The Stress-Performance Gap:** Analisis boxplot menunjukkan bahwa siswa di kategori "Low Performance" memiliki tingkat stres yang jauh lebih tinggi dan durasi tidur yang lebih tidak teratur dibandingkan kategori lainnya.
3.  **Efficiency over Quantity:** Jam belajar mandiri memberikan dampak positif hanya jika dibarengi dengan efisiensi revisi yang tinggi; kuantitas jam belajar tanpa fokus tidak menjamin hasil yang optimal.

---

## 🤖 Model Benchmarking & Results
Kami menguji empat pendekatan model untuk mendapatkan hasil terbaik dalam prediksi skor (Regresi) dan kategori performa (Klasifikasi).

### 1. Regression Results (Predicting Final Exam Score)
Kami membandingkan **Random Forest (Baseline)** dengan **XGBoost (Optimized)**.
- **Random Forest:** Mencapai R2 Score 0.59 dengan RMSE 11.64.
- **XGBoost:** Berhasil meningkatkan performa secara signifikan dengan **R2 Score 0.73** dan **RMSE 9.42**.
*Insight: XGBoost mampu menangkap pola non-linear dalam data pendidikan 14% lebih baik daripada model standar.*

### 2. Classification Results (Predicting Performance Category)
Tantangan utama adalah mendeteksi kelas minoritas (Siswa kategori "High").
- **Random Forest:** Gagal menangkap pola kelas High dengan Recall hanya 11%.
- **XGBoost:** Melalui optimasi, Recall kelas High meningkat pesat menjadi **37%**.
*Insight: Penggunaan teknik penyeimbangan beban kelas (class weight) dan algoritma boosting sangat krusial untuk deteksi siswa berprestasi.*

---

## 💡 Top Predicstors (Feature Importance)
Berdasarkan hasil pemodelan, tiga fitur yang paling menentukan skor akhir siswa adalah:
1.  **Discipline Score:** Fitur buatan yang menggabungkan kehadiran dan tingkat penyelesaian tugas.
2.  **Focus Intensity:** Efektivitas konsentrasi selama sesi belajar.
3.  **Study vs Social Ratio:** Keseimbangan antara waktu produktif dan distraksi digital.

---

## 🛠️ Tech Stack & Requirements
- **Language:** Python 3.8+
- **Main Libraries:** `pandas`, `scikit-learn`, `xgboost`, `seaborn`, `matplotlib`.
- **Optimization:** Feature Engineering, ColumnTransformer Pipeline, Label Encoding.

## 🚀 How to Use
1. Clone repositori ini.
2. Install dependensi: `pip install -r requirements.txt` (jika tersedia) atau install manual library di atas.
3. Jalankan notebook di folder `/notebooks` untuk melihat alur kerja lengkap dari pembersihan data hingga evaluasi model.

---
⭐ *Project by annisatristant*
