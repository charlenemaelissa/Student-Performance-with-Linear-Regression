# Student-Performance-with-Linear-Regression
Melakukan prediksi performance index dengan data student performance dengan variabel independen Hours Studied, Previous Scores, Sleep Hours, Sample Quaestion Papers Practiced. Kemuadian, variabel dependennya adalah  Perofrmance Index

tools yanga digunakan dalam pengerjaan tools ini:
- Python
- Pandas
- Prettytable
- Matplotlib / Seaborn
- Scikit-Learn

# Eksplorasi data
Sebelum melakukan prediksi, pertama tama perlu dilakukan pengecekan noise. Namun, karena data ini sudah bersih maka lanjut ke langkah selanjutnya yaitu eksplorasi data, saya menggunakan heatmap korelasi untuk melihat korelasi kuat dan lemah sesama fitur.
![Eksplorasi data](images/heatmap_korelasi.png) 
berdasarkan heatmap, variabel yang paling berpengaruh
terhadap performance index adalah previous scores dengan korelasi sangat
kuat sebesar 0.92, diikuti oleh Hours Studied dengan korelasi sedang
sebesar 0.37. Sementara itu, variabel sleep hours and sample question
papers practiced memiliki korelasi yang sangat lemah terhadap
performance index, masing masing hanya 0.05 dan 0.04, menunjukkan
pengaruhnya hampir tidak signifikan terhadap performa.

# Model Coeficient
![Model Koefisien](images/modelkoef.png)
Hours Studied: 2.8532
Previous Scores: 1.0191
Sleep Hours: 0.4716
Sample Question Papers Practiced: 0.1888
Berdasarkan grafik koefisien regresi linear, variable Hours Studied memiliki pengaruh besar terhadap performance index dengan koefisien sebesar 2.85, diikuti oleh previous scores(1.02), Sleep Hours (0.47) dan yang paling kecil ada sample papers practiced dengan nilai 0.19. Ini
menunjukkan bahwa setiap penambahan 1 jam belajar memberikan peningkatan performa yang paling signifikan dibandingkan predictor lainnya.

# hasil R squared
Train R2: 0.9886087194897399
Test R2: 0.9879991283609477
Nilai R squared untuk dat alatih sebesar 0.9886 dan untuk data uji sebesar 0.9880 menunjukkan bahwa model ini sangat baik memprediksi nilai performance index. Artinya, hampir semua variasi nilai bisa dijelaskan oleh model ini. Karena selisih antara data latih dan data uji sangat kecil, model ini bisa bekerja dengan baik baik di data yang sudah dikenal maupun data baru, jadi bisa dibilang modelnya akurat.

# Hasil MSE
Train MSE: 4.274694411673067
Test MSE: 4.129528706087852
Nilai Train MSE 4.27dan Test MSE 4.13 menunjukkan bahwa rata rata kesalahan prediksi model terhadap nilai asli cukup kecil, baik pada data latih maupun data uji. Karena nilai MSE pada data uji hampir sama dengan data latiih, ini berarti model bekerja dengan konsisten. Semakin kecil nilai MSE, semakin akurat model memprediksi. Jadi, bisa disimpulkan bahwa model kamu cukup akurat dan bisa diandalkan.

# melihat ada berapa banyak kombinasi fitur
15 15 15
Ada 15 kombinasi fitur yang diuji, masing-masing- kombinasi itu sudah dihitung nilai MSE dan R squared nya. Dengan jumlah yang sama semua berarti tidak ada kombinasi fitur yang terlewat atau gagal hitung.

# Evaluasi Model
![evaluasi model](images/Evaluasimodel.png)
Berdasarkan tabel hasil evaluasi model regresi linier pada kombinasi prediktor yang berbeda, terlihat bahwa kombinasi variabel Kours Studied, Previous Scores, Sleep Hours, Sample Questions Papers Practiced menghasilkan performa terbaik dengan nilai MSE terkecil sebesar 4.13 dan nilai R squared tertinggi sebesar 0.988. Ini menunjukkan bahwa kombinasi keempat variabel tersebut mampu menjelaskan sekitar 98.8% variasi data target, menjadikannya model paling akurat dibandingkan kombinasi lainnya.

# Melakukan prediksi
Prediksi siswa belajar selama 7 jam, memiliki nilai sebelumnya 89, tidur 8 jam, dan mengerjakan 4 lembar latihan soal.

# Hasil prediksi
[81.46449569]
Berdasarkan hasil prediksi model, dengan input 7 jam belajar, skor sebelumnya 89, 8 jam tidur, dan 4 lembar latihan soal, diperoleh prediksi nilai akhir sebesar 81.46. Ini menunjukkan bahwa kombinasi kebiasaan belajar tersebut diperkirakan menghasilkan performa akademik yang baik menurut model regresi linear yang digunakan.
