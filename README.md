# KlikMart Churn Prediction

## 📌 Deskripsi Proyek
KlikMart adalah perusahaan E-commerce di Indonesia yang menyediakan berbagai kebutuhan sehari-hari secara online. Sejak berdiri pada tahun 2016, KlikMart telah menarik jutaan pelanggan berkat layanan pengiriman langsung dari gudang ke rumah dan program loyalitas seperti cashback dan promo.

Namun, dengan semakin ketatnya persaingan industri E-commerce, KlikMart menghadapi tantangan dalam mempertahankan pelanggannya. Data internal menunjukkan tren peningkatan churn (hilangnya pelanggan) dari bulan ke bulan. Padahal, biaya mempertahankan pelanggan rata-rata hanya **$50**, jauh lebih murah dibandingkan biaya memperoleh pelanggan baru yang mencapai **$150**.

Proyek ini bertujuan membangun **model prediksi churn berbasis Machine Learning** untuk mengidentifikasi pelanggan berisiko churn secara optimal. Dengan model ini, intervensi dapat dilakukan secara tepat sasaran melalui penawaran personalisasi atau peningkatan layanan, sehingga strategi retensi lebih efisien dan berdampak.

---

## 🎯 Rumusan Masalah
> Bagaimana membangun model prediksi churn yang mampu secara optimal mengidentifikasi pelanggan yang berisiko churn agar perusahaan dapat melakukan tindakan pencegahan secara tepat sasaran?

---

## 🗂 Dataset
Dataset berisi informasi historis pelanggan, antara lain:
- Tenure: Lama waktu (dalam hari/bulan/tahun) pelanggan telah bergabung atau menggunakan layanan perusahaan.
- WarehouseToHome: Jarak antara gudang penyimpanan barang ke rumah pelanggan.
- NumberOfDeviceRegistered: Jumlah perangkat (device) yang terdaftar oleh pelanggan untuk mengakses layanan.
- PreferedOrderCat: Kategori produk yang paling sering atau terakhir dipesan oleh pelanggan dalam satu bulan terakhir.
- SatisfactionScore: Skor kepuasan pelanggan terhadap layanan yang diberikan, biasanya dalam skala tertentu (misalnya 1–5).
- MaritalStatus: Status pernikahan pelanggan, seperti "Single" atau "Married".
- NumberOfAddress: Jumlah alamat yang telah ditambahkan oleh pelanggan ke akun mereka (misalnya alamat rumah, kantor, dll).
- Complaint: Menunjukkan apakah pelanggan pernah mengajukan keluhan dalam satu bulan terakhir (biasanya 0 = tidak, 1 = ya).
- DaySinceLastOrder: Jumlah hari sejak terakhir kali pelanggan melakukan pemesanan.
- CashbackAmount: Rata-rata nilai cashback yang diterima pelanggan dalam satu bulan terakhir.
- Churn: Label apakah pelanggan berhenti menggunakan layanan (1 = churn, 0 = tidak churn).

---

## 🛠 Metodologi
1. **Preprocessing**: imputasi median, scaling, encoding kategorikal
2. **SMOTE**: menangani imbalance data
3. **Modeling**: berbagai algoritma (LogisticRegression, KNeighborsClassifier, DecisionTreeClassifier, VotingClassifier, StackingClassifier, BaggingClassifier, RandomForestClassifier, AdaBoostClassifier, GradientBoostingClassifier, XGBClassifier)
4. **Evaluasi**: metrik utama F3-score
5. **Threshold Tuning**: optimal pada 0.38

## 📊 Hasil Utama
- **Model Terbaik:** Voting Classifier
- **Skor Awal (tuning):** 0.813226  
- **Skor Setelah Threshold 0.38:** 0.821089  
- **Insight:** Penyesuaian threshold membantu mengoptimalkan keseimbangan recall dan precision sehingga *false negative* menurun.

---

## 💰 Analisis Biaya

**Sebelum ML**
- Skenario 1 (Semua pelanggan diasumsikan churn): **$27,350**  
- Skenario 2 (Semua pelanggan diasumsikan tetap): **$16,050**  
- **Total:** **$43,400**

**Sesudah ML**
- Total biaya turun menjadi **$6,750**  
- **Penghematan:** **$36,650**

---

## 📌 Kesimpulan
Penerapan model machine learning dengan metrik F3-score dan threshold 0.38 terbukti mampu:
- Mengidentifikasi pelanggan berisiko churn lebih akurat
- Menekan *false negative* yang berisiko tinggi secara bisnis
- Menghemat biaya retensi dan mengurangi kerugian akibat churn

---

## 🚀 Rekomendasi
1. Implementasikan model secara penuh pada seluruh segmen pelanggan
2. Integrasikan model dengan sistem CRM untuk intervensi otomatis
3. Lakukan retraining model secara berkala dengan data terbaru
4. Pantau KPI retensi dan ROI program loyalitas secara berkelanjutan

---
