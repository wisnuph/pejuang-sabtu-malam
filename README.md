# Loan Prediction Based on Customer Behavior
Final Project Bootcamp Data Science Rakamin Academy - Batch 42 

|   	| **PSM (Pejuang Sabtu Malam)**    	   |
|---	|--------------------------------------|
| 1 	| Wisnu Pri Hartono  (Ketua Kelompok)  |
| 2 	| Muhammad Zulfarhan 	                 |
| 3 	| Arman Lukman   	                     |
| 4 	| Farki Mahbubi 	                     |
| 5 	| Radithya Arif Pambudi   	           |
| 6 	| Surya Praviarti      	               |
| 7 	| Raihan Damar 	                       |

## Dataset
Bersumber dari Kaggle Dataset dengan judul [Loan Prediction Based on Customer Behavior](https://www.kaggle.com/datasets/subhamjain/loan-prediction-based-on-customer-behavior)

Dalam Dataset diperoleh Data Total nasabah yaitu 252.000 nasabah.

Terdiri dari 13 Column : 
  - **Id, Income, Age, Experience, Married/Single, House_Ownership, Car_Ownership, Profession, CITY, STATE, CURRENT_JOB_YRS, CURRENT_HOUSE_YRS, Risk_Flag**

## Insight Summary dari [Exploratory Data Analysis](https://colab.research.google.com/drive/1dkZTO5T_3kKiRdpLPdupE97ANdhv2t2L?usp=sharing)
Berdasarkan data yang diperoleh dapat disimpulkan bahwa tidak adanya nilai outliers dan distribusi data rata-rata cenderung normal kecuali pada kolom CURRENT_JOB_YEARS yang memiliki distribusi skewed ke arah kanan.

Dalam penentuan tingkat resiko gagal bayar (risk flag) yang dilakukan oleh nasabah, dapat diterapkan analisa berdasarkan:
  - **group usia vs group income**
    
    Group usia dan group income sama-sama lebih dominan tidak beresiko risk flag dari pada yang beresiko risk flag.
    Jumlah nasabah yang tidak beresiko risk flag yang terbesar yaitu pada group usia dewasa dan group low income sebesar 25501. Sebaliknya yang terkecil adalah group usia remaja dan group low income sebesar 5969.
    Jumlah nasabah yang beresiko risk flag yang terbesar yaitu pada group usia dewasa dan group low income sebesar 3788. Sebaliknya yang terkecil adalah group usia remaja dan group medium income sebesar 811.

 - **married status vs group income**

    Berdasarkan data diperoleh bahwa nasabah dengan status single dan rentang pendapatan High Income cenderung memiliki tingkat resiko cukup tinggi dalam gagal bayar pinjaman (memiliki risk flag yang terbesar) sebesar 9829.
   Sebaliknya untuk nasabah dengan status married dan rentang pendapatan High Income justru memiliki tingkat risk flag terendah sebesar 799.

  - **group income vs house ownership**
    
    Group income dan group house ownership sama-sama lebih dominan tidak beresiko risk flag dari pada yang beresiko risk flag.
    Berdasarkan data diperoleh bahwa group rented yang memiliki resiko risk flag terbesar sekaligus tidak memiliki resiko risk flag yang terbesar.
    Kemudian pada group norent noown yang memiliki resiko risk flag terkecil sekaligus tidak memiliki resiko risk flag yang terkecil.
    Jumlah nasabah yang tidak beresiko risk flag yang terbesar yaitu pada group high income dan group rented sebesar 67836.
    Sebaliknya yang terkecil adalah group medium income dan group norent noown sebesar 1844.
    Jumlah nasabah yang beresiko risk flag yang terbesar yaitu pada group high income dan group rented sebesar 10062.
    Sebaliknya yang terkecil adalah group medium income dan group norent noown sebesar 193.

Selain itu, dapat juga diterapkan analisis dan visualisasi data berdasarkan:
  - **usia vs status**
    
    Tingkat resiko berdasarkan usia dan status yang tertinggi yaitu pada usia Dewasa dengan status single sebesar 14.99% atau 9.584 customer beresiko.
    Berdasarkan data ini pemberi pinjaman dapat memberikan penambahan jaminan pada customer dengan usia Dewasa dan status Single untuk memperkecil kemungkinan kerugian perusahaan saat customer tersebut berisiko.

  - **state**
    
    Dari 10 state dengan jumlah pelanggan terbanyak, tingkat resiko tertinggi terdapat di state Uttar Pradesh sebanyak 3.343 nasabah beresiko. Top 10 Jumlah nasabah beresiko di state Uttar Prades di dominasi kepemilikan rumah sewa dan tidak mempunyai mobil dengan Income > 2,000,000.
    Berdasarkan data tersebut, dengan melakukan Clusterisasi daerah yang beresiko tinggi  dan mewajibkan DP tinggi agar cicilan customer rendah sehingga customer tidak berat saat membayar pinjaman.
    Dari segi bisnis perusahaan dapat menaikkan  Bunga pinjaman agar modal yang dikeluarkan untuk pemberian pinjaman  dapat kembali diawal.

  - **harta kepemilikan dan income dengan jumlah user**
    
    Berdasarkan Income, Kepemilikan Rumah dan Mobil dapat dibuat sebuah penilaian harta kepemilikan(Net Worth Value) dari User. Berdasarkan Incomenya dapat diberikan nilai 1-3 dari Low, Medium dan High Income berdasarkan pembagian dari Q1 dan Q3 Income. Untuk Kepemilikan rumah diberikan nilai 3 untuk ‘owned’, 2 untuk ‘rented’ dan 1 untuk ‘noown_norent’ dan kemudian dijumlahkan. Untuk kepemilikan mobil digunakan 1 untuk ‘yes’ dan 0 untuk ‘no’. Berdasarkan grafik dari data diperoleh bahwa user dominan memiliki harta kekayaan baik itu dari Income, rumah ataupun mobil. User dengan value score 4 memiliki jumlah terbanyak dan juga memiliki risk yang besar.
    Dari data tersebut, pemberian kredit lebih baik diberikan kepada nasabah yang memiliki networth value yang bernilai 4 kebawah dapat dilakukan penambahan bunga atau peningkatan DP untuk mengurangi kerugian apabila user tersebut gagal bayar. 
