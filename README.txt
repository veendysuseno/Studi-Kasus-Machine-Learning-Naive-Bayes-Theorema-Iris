Penerapan Machine Learning dengan Pendekatan Supervised dengan Metode Algoritma Naive Bayes Classifier

Naive Bayes adalah algoritma machine learning berbasis probabilitas yang digunakan untuk klasifikasi. Algoritma ini didasarkan pada Teorema Bayes dengan asumsi bahwa fitur-fitur yang digunakan dalam klasifikasi adalah independen satu sama lain (inilah mengapa disebut "naive").
Teorema Bayes

Teorema Bayes menyatakan bahwa:
P(H∣E)=P(E∣H)×P(H)P(E)
P(H∣E)=P(E)P(E∣H)×P(H)​

Di mana:

    P(H∣E)P(H∣E) adalah probabilitas hipotesis HH diberikan evidence EE.
    P(E∣H)P(E∣H) adalah probabilitas evidence EE diberikan hipotesis HH.
    P(H)P(H) adalah probabilitas awal hipotesis HH.
    P(E)P(E) adalah probabilitas evidence EE.

Asumsi Kemandirian

Algoritma Naive Bayes mengasumsikan bahwa setiap fitur xixi​ dari sebuah instance data adalah independen dari fitur lainnya, yang artinya:
P(x1,x2,...,xn∣C)=P(x1∣C)×P(x2∣C)×...×P(xn∣C)
P(x1​,x2​,...,xn​∣C)=P(x1​∣C)×P(x2​∣C)×...×P(xn​∣C)

Di mana:

    P(x1,x2,...,xn∣C)P(x1​,x2​,...,xn​∣C) adalah probabilitas munculnya fitur-fitur x1,x2,...,xnx1​,x2​,...,xn​ diberikan kelas CC.
    P(xi∣C)P(xi​∣C) adalah probabilitas munculnya fitur xixi​ diberikan kelas CC.

Langkah-langkah dalam Naive Bayes Classifier

    Persiapan Data: Hitung probabilitas awal dari setiap kelas (prior).
    Menghitung Likelihood: Untuk setiap fitur pada instance yang baru, hitung probabilitas fitur tersebut diberikan kelas tertentu.
    Menghitung Posterior: Kalikan semua probabilitas likelihood dengan prior dari kelas tersebut.
    Memilih Kelas: Pilih kelas dengan probabilitas tertinggi sebagai prediksi.

Implementasi Naive Bayes di TensorFlow 2.x

TensorFlow 2.x tidak memiliki implementasi langsung dari Naive Bayes, tetapi kita bisa menggunakan scikit-learn, atau mengimplementasikannya sendiri dengan TensorFlow jika diperlukan.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Studi Kasus Metode Algoritma Naive Bayes Classifier dengan Dataset Iris:
Disediakan sebuah gambar bunga agar kita tentukan bunga tersebut kedalam spesies atau jenis bunga apa.
1. Disediakan library sklearn pada Python dengan dataset Iris tersedia di library sklearni, bisa diunduh di http://archive.ics.icu.edu
2. Dataset Iris dikumpulkan oleh ahli botani Anderson dan berisi sampel acak bunga milik 3 spesied bunga iris, yaitu setosa, versicolor, dan virginica. Untuk masing-masing spesies, 50 pengamatan untuk panjang sepal, lebar sepal, panjang petal, dan lebar petal dicatat.

Keterangan:
Sepal = daun kelopak, merupakan daun perhiasan bunga paling pangkal, berkelompok membentuk kelopak bunga (calyx).
Petal = aun mahkota yang mengelompok membentuk mahkota bunga (corolla).

Tugas!
Kita akan membuat program machine learning dengan databaset Iris dengan Metode Algoritma Naive Bayes Classifier dengan bahasa Python.



@Copyright Veendy 2024