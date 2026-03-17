# 📊 Early Warning System for At-Risk Customers (SaaS)

## 🚀 Executive Summary
Project ini bertujuan membangun sistem **early warning** untuk mendeteksi pelanggan yang berpotensi churn menggunakan pendekatan **recency (aktivitas terakhir pelanggan)**.

### Key Insights:
- 📉 **6.38% customer teridentifikasi sebagai at-risk**
- 🧩 Seluruh risiko terkonsentrasi pada **segmen SMB**
- 🌍 Risiko tertinggi berada di **region EMEA**
- 💰 Customer at-risk masih memiliki kontribusi revenue → **perlu intervensi cepat**

### Business Impact:
Tanpa tindakan proaktif, customer at-risk berpotensi berhenti bertransaksi dan menyebabkan penurunan revenue. Oleh karena itu, diperlukan sistem monitoring dan strategi retensi berbasis risiko.

---

## 🧠 Background
Dalam bisnis SaaS (Software as a Service), mempertahankan pelanggan (retention) merupakan faktor kunci keberhasilan. Namun, tidak semua pelanggan yang akan churn dapat terdeteksi secara langsung.

Pada dataset ini, tidak terdapat churn eksplisit, sehingga digunakan pendekatan **early warning berbasis perilaku transaksi**, khususnya melalui analisis **recency (jarak waktu sejak transaksi terakhir)**.

---

## 🎯 Problem Statement
Perusahaan belum memiliki indikator yang jelas untuk:
- Mengidentifikasi pelanggan yang mulai tidak aktif
- Menentukan segmen dan wilayah dengan risiko tertinggi
- Mengetahui faktor yang berkaitan dengan penurunan aktivitas pelanggan

---

## ❓ Business Questions
1. Bagaimana distribusi customer berdasarkan tingkat risiko (recency)?
2. Siapa saja customer yang paling berisiko dan berapa nilai bisnisnya?
3. Segmen pelanggan mana yang memiliki risiko tertinggi?
4. Wilayah mana yang memiliki konsentrasi risiko tertinggi?
5. Apakah terdapat perbedaan perilaku antara customer aktif dan customer berisiko?

---

## 📂 Dataset
Dataset berisi data transaksi customer SaaS yang mencakup:
- Customer ID
- Order Date
- Sales, Profit, Discount
- Segment, Region, Industry
- Product dan informasi geografis lainnya

---

## 🧹 Data Cleaning
Proses data cleaning dilakukan untuk memastikan kualitas data sebelum analisis:

- ✔️ Tidak ditemukan missing values  
- ✔️ Tidak ditemukan duplicate data  
- ✔️ Validasi kategori menunjukkan data konsisten  
- ✔️ Tidak ditemukan whitespace (leading/trailing spaces)  
- ✔️ Nilai numerik berada dalam rentang yang wajar  
- ✔️ Profit negatif dipertahankan karena relevan dalam konteks bisnis  

---

## ⚙️ Feature Engineering
Untuk mendeteksi potensi churn, dibuat beberapa fitur utama:

- **Last Purchase Date**
- **Recency (days)** → selisih hari sejak transaksi terakhir
- **Risk Bucket**:
  - Active (0–30 hari)
  - Warm (31–90 hari)
  - At-risk (91–180 hari)
  - High Risk (181–365 hari)

---

## 📊 Key Metrics
- Risk Rate: **6.38%**
- Total At-Risk Customers: **3**
- Segmen Risiko Tertinggi: **SMB**
- Region Risiko Tertinggi: **EMEA**

---

## 📊 Key Findings

### 1. Distribusi Risiko
Mayoritas customer masih berada pada kategori **Active dan Warm**, menunjukkan kondisi pelanggan relatif sehat. Namun, terdapat customer dalam kategori **At-risk dan High Risk** yang menjadi early warning terhadap potensi churn.

---

### 2. Customer Prioritas (Business Impact)
Customer dalam kategori At-risk masih memiliki kontribusi revenue yang signifikan, sehingga menjadi **prioritas utama untuk dipertahankan**.

Sebaliknya, customer High risk dengan nilai bisnis rendah lebih cocok ditangani melalui strategi reaktivasi cepat.

---

### 3. Segmen Paling Rentan
Seluruh customer berisiko berasal dari segmen **SMB**, menjadikannya fokus utama dalam strategi retensi.

---

### 4. Wilayah Paling Rentan
Risiko terkonsentrasi pada region **EMEA**, menunjukkan perlunya pendekatan retensi berbasis wilayah.

---

### 5. Faktor yang Berkaitan dengan Risiko
- **Discount** memiliki hubungan signifikan dengan risiko penurunan aktivitas  
- **Profit margin** tidak menunjukkan perbedaan signifikan  

---

## 💡 Business Recommendations

### 1. Implement Early Warning System (Watchlist)
Membangun monitoring mingguan untuk customer at-risk agar tidak terlewat tanpa tindakan.

---

### 2. Risk-Based Follow-Up Strategy
- Warm → engagement ringan  
- At-risk → proactive outreach  
- High risk → reactivation / decision  

---

### 3. Fokus Retensi pada SMB (EMEA)
Mengalokasikan resource pada area dengan risiko tertinggi untuk dampak maksimal.

---

### 4. Optimasi Kebijakan Diskon
Mengurangi ketergantungan pada diskon dan beralih ke pendekatan value-based.

---

## 📈 KPI yang Disarankan
- Penurunan jumlah customer At-risk & High risk  
- Peningkatan retention rate (terutama SMB)  
- Penurunan churn di region EMEA  
- Stabilitas atau peningkatan profit margin  

---

## 📸 Project Preview
*(Tambahkan screenshot dashboard / visualisasi di sini jika ada)*

---

## 🛠️ Tools & Technologies
- Python (Pandas, NumPy, Seaborn, Matplotlib)
- Jupyter Notebook
- Tableau

---

## 🔗 Links
- Notebook: *(tambahkan link jika ada)*  
- Dashboard: *(tambahkan link jika ada)*  

---

## 📌 Conclusion
Meskipun tingkat risiko saat ini masih relatif rendah, keberadaan customer at-risk merupakan **early warning signal** yang penting. Risiko yang terkonsentrasi pada segmen SMB dan region EMEA menunjukkan perlunya strategi retensi yang lebih terarah dan proaktif untuk menjaga keberlanjutan bisnis.

---

## 👤 Author
**Ika Christine Purba**
