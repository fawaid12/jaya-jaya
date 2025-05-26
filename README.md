# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Jaya Jaya Maju

## Business Understanding

Jaya Jaya Maju adalah sebuah perusahaan multinasional yang telah beroperasi sejak tahun 2000 dengan jumlah karyawan lebih dari 1000 orang yang tersebar di berbagai wilayah di Indonesia. Seiring pertumbuhan bisnis yang semakin besar, perusahaan menghadapi tantangan baru dalam mengelola sumber daya manusianya secara efektif. Salah satu isu utama yang menjadi perhatian adalah tingkat attrition karyawan yang terus meningkat, di mana lebih dari 10% karyawan meninggalkan perusahaan dalam periode tertentu. Kondisi ini tentu menjadi ancaman bagi keberlangsungan operasional dan kestabilan organisasi, khususnya di departemen yang memiliki peran strategis. Untuk menjawab tantangan tersebut, tim Human Resources (HR) ingin mengetahui lebih dalam mengenai faktor-faktor apa saja yang paling mempengaruhi keputusan karyawan untuk mengundurkan diri. Selain itu, mereka juga membutuhkan dashboard bisnis yang dapat membantu dalam memantau tren dan indikator yang berkaitan dengan attrition secara real time. Melalui proyek ini, dilakukan analisis data secara menyeluruh serta pengembangan model prediktif untuk mendukung pengambilan keputusan berbasis data oleh manajemen HR.

### Permasalahan Bisnis
Tahap ini bertujuan untuk merinci tantangan yang dihadapi perusahaan dan menyusunnya dalam bentuk pertanyaan analitis yang dapat dijawab melalui pendekatan data science.
- Tingginya tingkat pengunduran diri (attrition) karyawan di beberapa departemen penting.
- Sulitnya memprediksi karyawan yang berisiko resign sehingga manajemen kesulitan membuat rencana suksesi dan retensi.
- Kebutuhan untuk memahami faktor-faktor utama yang mempengaruhi keputusan karyawan untuk keluar dari perusahaan.

### Cakupan Proyek
Agar solusi lebih terarah dan terukur, maka cakupan proyek perlu didefinisikan secara jelas. Berikut adalah batasan dan ruang lingkup pekerjaan:
- Melakukan eksplorasi data dan pembersihan (data cleaning) pada data karyawan.
- Melakukan analisis data eksploratif (EDA) untuk mencari pola attrition.
- Mengidentifikasi fitur yang paling berpengaruh terhadap attrition menggunakan korelasi.
- Membangun model klasifikasi menggunakan Random Forest, Gradient Boosting, dan XGBoost untuk memprediksi attrition.
- Membuat business dashboard menggunakan Looker Studio untuk visualisasi data penting bagi manajemen.

### Persiapan

Sumber data: Dataset karyawan dari [Dicoding Dataset - Employee Attrition](https://github.com/dicodingacademy/dicoding_dataset/tree/main/employee)

Setup environment: Apabila menginstal Python melalui Anaconda ataupun miniconda, Anda dapat menggunakan conda sebagai package manager dan environment management system. Langkah bisa menggunakan anaconda navigator dengan cara sebagai berikut :
1. Buka anacoda navigator
2. Buka Enviroments
3. Pilih Create
4. Masukan nama enviroment
5. Pilih versi Python 3.9.21
6. klik create
7. pilih anaconda prompt untuk instal file reqruiements.txt
8. Jalankan perintah
   ```
   pip install -r requirements.txt
   ```

Cara lain membuat enviroment menggunakan terminal
1. Buka terminal bisa menggunakan anaconda prompt
2. Jalankan Perintah
   ```
   conda create --name Attrition python=3.9.21
   ```
3. Jalankan Perintah conda activate
   ```
   conda activate Attrition
   ```
4. Jalankan perintah install library
   ```
   pip install -r requirements.txt
   ```

## Business Dashboard
Setelah mendapatkan insight dari proses analisis dan pemodelan, langkah selanjutnya adalah menyajikan informasi tersebut dalam bentuk visual agar mudah dipahami oleh pihak non-teknis, seperti manajemen HR. Pada bagian ini, dashboard berperan penting sebagai alat bantu monitoring dan pengambilan keputusan. Dashboard dibuat dengan looker studio yang dapat diakses [[Attrition Dashboard]](https://lookerstudio.google.com/reporting/1dc46e1e-86c0-4eeb-ac71-3d23f7748bd1). Dalam pembuatan dashboard menggunakan fitur filtering Department, Jobrole, Joblevel, dan age. Kemudian visualisasi Overtime, job satisfaction, total working years, dan stock option level. Fitur dashboard ini diambil dari pendekatan korelasi fitur attrition dengan fitur yang lain dengan menghitung 5 nilai yang paling besar kemudian ditambahkan domain knowledge.


## Conclusion
- Berdasarkan hasil analisis korelasi dan uji model, fitur-fitur yang paling berpengaruh terhadap attrition karyawan meliputi
  ```
  ['TotalWorkingYears', 'Age', 'JobLevel', 'StockOptionLevel', 'MonthlyIncome', 'JobSatisfaction', 'OverTime', 'EnvironmentSatisfaction', 'YearsAtCompany']
  ```
- Kombinasi antara fitur numerik dan kategorikal tersebut membantu model machine learning dalam mengenali pola yang berkaitan dengan keputusan resign karyawan
- Model Random Forest memberikan performa cukup baik secara default
- Dashboard looker studio menyajikan insight visual yang bermanfaat untuk pengambilan keputusan oleh tim HR.

### Rekomendasi Action Items (Optional)
Berdasarkan hasil analisis, beberapa tindakan yang dapat direkomendasikan untuk perusahaan antara lain:
- Memberikan peningkatan kompensasi atau pengembangan karier bagi karyawan dengan tingkat jabatan rendah.
- Mengembangkan program retensi khusus untuk karyawan dengan masa kerja pendek.
- Menggunakan model prediksi attrition sebagai sistem peringatan dini untuk intervensi manajemen.
- Melakukan survei mendalam terhadap kelompok karyawan yang berisiko tinggi untuk mendapatkan insight kualitatif tambahan.
