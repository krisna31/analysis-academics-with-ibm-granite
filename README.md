# Dampak Penggunaan Jumlah Aplikasi Harian terhadap Kinerja Akademik Siswa Kelas 12

## Project Overview

Proyek ini bertujuan untuk menganalisis hubungan liniar antara jumlah aplikasi yang digunakan setiap hari (Apps_Used_Daily), dengan kinerja akademik (Academic_Performance) di kalangan siswa kelas 12. proyek ini mengadopsi pendekatan dua tahap antara lain:

Klasifikasi Berbasis Kode: Siswa dikelompokkan ke dalam empat profil pengguna yang berbeda (Minimal, Moderate, Heavy, Power User) berdasarkan distribusi kuartil dari data penggunaan aplikasi harian mereka. Pendekatan ini memastikan klasifikasi yang objektif, cepat, dan hemat biaya.

Prediksi Berbasis AI: Hasil analisis dari pengelompokan tersebut kemudian disajikan sebagai konteks kepada Large Language Model (LLM) IBM Granite. AI digunakan untuk melakukan prediksi dua arah (memprediksi skor dari profil, dan sebaliknya) lengkap dengan penalaran logis berdasarkan data yang disajikan.

Tujuan akhirnya adalah untuk mengungkap hubungan linear sebesar apa, serta mendemonstrasikan penggunaan AI ibm dalam analisis data.

## Raw dataset link

Analisis ini menggunakan dataset yang tersedia untuk umum yang relevan dengan topik penelitian.
Dataset: Teen Phone Addiction
Sumber: Kaggle
Owner: Sumedh1507
URL: <https://www.kaggle.com/datasets/sumedh1507/teen-phone-addiction>

## Insight & findings

Adanya korelasi negatif lemah antara jumlah aplikasi yang digunakan vs performa akademik kurang lebih sebesar -0.026136 atau sekitar 2,6%, yang artinya jumlah aplikasi tidak terlalu berpengaruh terhadap nilai akademik yang dicapai. Namun hal yang dapat kita pelajari disini adalah karena korelasinya negatif maka semakin sedikit aplikasi yang kita gunakan setiap harinya akan memiliki hubungan terbalik terhadap nilai akademik yang didapatkan yaitu lebih besar dan sebaliknya.

## AI support explanation

Dalam proyek ini, model ibm-granite/granite-3.0-8b-instruct dari IBM dimanfaatkan untuk penalaran prediktif berbasis dataset.

AI berperan sebagai seorang analis data ahli. Setelah analisis dan pengelompokan awal dilakukan dengan kode, sebuah ringkasan temuan (tabel kinerja akademik per profil pengguna) diberikan kepada model sebagai "base knowledge". Berdasarkan konteks ini, AI ditugaskan untuk:

Memprediksi rentang kinerja akademik seorang siswa jika profil penggunaannya diketahui.
Memprediksi profil pengguna yang paling mungkin jika skor akademiknya diketahui.
Memberikan alasan (reasoning) yang logis untuk setiap prediksi, yang didasarkan sepenuhnya pada data ringkasan yang diberikan.
Mengapa Pendekatan Ini Dipilih: Karena pendekatan ini memanfaatkan kekuatan dari LLM untuk memahami, menalar, dan mengartikulasikan hubungan dalam bahasa alami, yang menunjukkan AI dapat berfungsi sebagai mitra prediksi untuk memprediksi hasil dan menjelaskan alasannya.
