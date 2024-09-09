# Penerapan Algoritma Naive Bayes Classifier

## Studi Kasus

Proyek ini menggunakan dataset Iris yang tersedia di [link ini](http://archive.ics.uci.edu/dataset/53/iris). Tujuan dari proyek ini adalah untuk mengklasifikasikan spesies bunga iris berdasarkan data fitur seperti panjang sepal, lebar sepal, panjang petal, dan lebar petal menggunakan Algoritma Naive Bayes.

## Pengenalan Naive Bayes

Naive Bayes adalah algoritma klasifikasi berbasis probabilitas yang didasarkan pada Teorema Bayes. Algoritma ini disebut "naive" karena mengasumsikan bahwa fitur-fitur yang digunakan dalam klasifikasi adalah independen satu sama lain.

### Teorema Bayes

Teorema Bayes dapat dinyatakan sebagai:

- P(x1, x2, ..., xn∣C) = P(x1∣C) × P(x2∣C) × ... × P(xn∣C)

### Di mana:

- **P(x1, x2, ..., xn∣C)**: Probabilitas munculnya fitur-fitur diberikan kelas C.
- **P(xi∣C)**: Probabilitas munculnya fitur ke-i diberikan kelas C.

## Langkah-langkah Naive Bayes Classifier

1. **Persiapan Data**: Hitung probabilitas awal (prior) dari setiap kelas.
2. **Menghitung Likelihood**: Hitung probabilitas fitur tertentu muncul berdasarkan kelas.
3. **Menghitung Posterior**: Kalikan semua probabilitas likelihood dengan prior dari kelas.
4. **Memilih Kelas**: Kelas dengan probabilitas tertinggi dipilih sebagai prediksi.

## Implementasi Naive Bayes dengan Python

TensorFlow 2.x tidak memiliki implementasi langsung dari Naive Bayes. Oleh karena itu, untuk proyek ini, kita akan menggunakan library `scikit-learn`.

### Studi Kasus Naive Bayes Classifier dengan Dataset : Iris

Dataset Iris berisi 150 sampel acak dari tiga spesies bunga iris: setosa, versicolor, dan virginica. Untuk masing-masing spesies, data yang dikumpulkan mencakup:

- Panjang Sepal (cm)
- Lebar Sepal (cm)
- Panjang Petal (cm)
- Lebar Petal (cm)

#### Keterangan:

- **Sepal**: Daun kelopak, merupakan daun perhiasan bunga yang membentuk kelopak bunga.
- **Petal**: Daun mahkota bunga yang membentuk mahkota bunga.

### Tugas:

Buat program machine learning dengan Naive Bayes Classifier untuk mengklasifikasikan spesies bunga berdasarkan dataset Iris menggunakan Python.

#### Contoh Implementasi Naive Bayes dengan `scikit-learn`

```python
from sklearn import datasets
from sklearn.model_selection import train_test_split
from sklearn.naive_bayes import GaussianNB
from sklearn.metrics import accuracy_score

# Load dataset Iris
iris = datasets.load_iris()
X = iris.data
y = iris.target

# Bagi dataset menjadi data training dan testing
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3, random_state=42)

# Inisialisasi model Naive Bayes
model = GaussianNB()

# Latih model
model.fit(X_train, y_train)

# Prediksi data testing
y_pred = model.predict(X_test)

# Hitung akurasi
accuracy = accuracy_score(y_test, y_pred)
print(f"Akurasi: {accuracy * 100:.2f}%")
```

## Penjelasan Kode:

- datasets.load_iris: Memuat dataset Iris.
- train_test_split: Membagi dataset menjadi data training dan testing.
- GaussianNB: Menginisialisasi model Naive Bayes Gaussian.
- fit: Melatih model dengan data training.
- predict: Memprediksi data testing.
- accuracy_score: Menghitung akurasi dari prediksi.

## Kesimpulan

- Naive Bayes adalah algoritma machine learning yang sederhana dan efektif untuk klasifikasi. Dalam proyek ini, algoritma digunakan untuk mengklasifikasikan spesies bunga iris berdasarkan data fitur. Naive Bayes mengasumsikan kemandirian antar fitur, dan meskipun ini sering kali bukan asumsi yang sepenuhnya benar, algoritma ini tetap memberikan hasil yang baik dalam banyak kasus.

## Catatan:

- Pada repo ini terdapat 3 cara penyelesaian: - codev1; - codev2; - codev3.
  dimana ketiga memiliki cara cara tersendiri dalam menyelesaikan studi kasus dengan algoritma Naive Bayes.

#### @Copyright Veendy 2024
