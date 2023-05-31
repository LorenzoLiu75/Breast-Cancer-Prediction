# **Breast Cancer Classification**

Anggota :

211401015 - Pieter Tanoto

211401024 - Rizky Maulana Sembiring

211401042 - Annisa Khairina

211401061 - Lorenzo Liunardo

211401076 - Andhika Mandalanta Saragih

211401119 - Tiur Asria Tampubolon



|     | Deskripsi |
| --- | --------- |
| Dataset | [Breast Cancer Prediction](<https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data>) |
| Latar Belakang |Menurut data World Health Organization (WHO) pada tahun 2020, terdapat 2,3 juta wanita terdiagnosis kanker payudara dan 685.000 kematian secara global. Hingga akhir tahun 2020, terdapat 7,8 juta wanita hidup yang didiagnosis menderita kanker payudara dalam 5 tahun terakhir, menjadikannya kanker paling umum di dunia. Ada lebih banyak tahun hidup yang disesuaikan dengan kecacatan (DALYs) yang hilang oleh wanita akibat kanker payudara secara global daripada jenis kanker lainnya. Kanker payudara terjadi di setiap negara di dunia pada wanita pada usia berapa pun setelah pubertas tetapi dengan tingkat yang meningkat di kemudian hari.  |
| Masalah | <p>Berdasarkan latar belakang di atas, terdapat beberapa masalah yang terkait dengan kanker payudara. Angka kejadian dan kematian yang tinggi menunjukkan bahwa kanker payudara tetap menjadi masalah serius di tingkat global. Meskipun telah ada peningkatan kesadaran dan upaya pencegahan, masih banyak wanita yang terkena dampak penyakit ini, dan jumlahnya terus meningkat dari waktu ke waktu.</p><p>Selain itu, stigma dan ketidaktahuan tentang kanker payudara juga menjadi masalah yang perlu diatasi. Beberapa masyarakat masih memiliki keyakinan yang salah atau mitos tentang penyakit ini, yang dapat menghalangi upaya pencegahan, deteksi dini, dan pengobatan. Pendidikan dan peningkatan kesadaran akan pentingnya deteksi dini dan akses ke perawatan yang tepat diperlukan untuk mengatasi masalah ini.</p>|
| Solusi Machine Learning | Oleh karena itu, akan lebih baik apabila dilakukan pengecekan secara berkala sebagai tindakan preventif lebih dini terhadap penyakit kanker payudara dengan menggunakan sistem machine learning untuk mengetahui kemungkinan risiko terkena penyakit kanker payudara yang ganas.|
| Metode Pengolahan Data | <p>Metode pengolahan data yang digunakan pada proyek ini dimulai dengan melakukan tahap Data Ingestion, yaitu dengan membaca dataset menggunakan library pandas dan memilih kolom yang diperlukan untuk proses pengujian. Selanjutnya, dilakukan tahap Data Validation untuk memeriksa kualitas data dengan melihat statistik data, melihat tipe data dan frekuensi tiap kolom, serta mengidentifikasi adanya data duplikat dan outliers menggunakan boxplot dan metode IQR. Setelah itu, dilakukan tahap Data Cleansing dengan menghapus data yang termasuk outliers.</p><p>Setelah tahap Data Cleansing, dilakukan tahap Data Preprocessing dengan melakukan transformasi pada data. Fitur-fitur numerik pada dataset diubah menggunakan metode Min-Max Scaling untuk mengubah rentang fitur menjadi antara 0 hingga 1 agar lebih mudah diproses oleh model. Selanjutnya, dataset dibagi menjadi training set dan test set dengan rasio 70:30 menggunakan library scikit-learn.</p><p>Selanjutnya, dilakukan tahap Model Creation dengan membangun model neural network untuk binary classification. Model tersebut menggunakan arsitektur sequential dengan beberapa layer dense. Model di-compile menggunakan optimizer Adam, loss function binary cross entropy, dan menggunakan metrik evaluasi binary accuracy untuk mengukur persentase prediksi yang benar terhadap total data.</p><p>Setelah itu, dilakukan tahap Data Training dengan melatih model menggunakan data training. Jumlah epoch yang digunakan adalah 30, dan hasil pelatihan model dievaluasi menggunakan data test set. Hasil evaluasi model menunjukkan akurasi sebesar 95,36% dan nilai loss sebesar 0.1797.</p><p>Terakhir, dilakukan pengujian model dengan menggunakan beberapa data pengujian baru dan melakukan prediksi kelas kanker (Malignant/Ganas atau Benign/Jinak) berdasarkan output model.</p> |
| Arsitektur Model | <p>Arsitektur model yang digunakan adalah sebuah model neural network untuk binary classification menggunakan dataset "Breast Cancer Wisconsin". Model ini memiliki input layer dengan 10 neuron yang menerima fitur-fitur numerik dari dataset. Kemudian, terdapat dua hidden layer dengan masing-masing 1024 neuron yang menggunakan fungsi aktivasi ReLU. Output layer menggunakan satu neuron dengan fungsi aktivasi sigmoid untuk melakukan prediksi kelas biner.</p><p>Kemudian, kita melakukan kompilasi model dengan optimizer 'adam' dan loss function 'binary\_crossentropy'. Metrics yang digunakan adalah binary\_accuracy untuk mengukur persentase jumlah prediksi benar terhadap total data. Setelah itu, kita melatih model pada data training dengan jumlah epochs sebesar 30 menggunakan metode fit() pada objek model.</p><p>Setelah melatih model, dilakukan evaluasi pada dataset uji (test set) untuk mengukur kinerja model. Selain itu, dilakukan visualisasi akurasi dan loss model selama proses pelatihan menggunakan plot. Terakhir, dilakukan pengujian dengan menggunakan beberapa data pengujian baru dan menampilkan hasil prediksi kelas kanker (Malignant/Ganas atau Benign/Jinak) berdasarkan output model.</p> |
| Metrik Evaluasi | Metrik yang digunakan untuk mengevaluasi performa model *machine learning* adalah *binary accuracy*. *Binary accuracy* dihitung dengan membagi jumlah prediksi yang benar dengan jumlah total data. Metrik ini memberikan gambaran tentang seberapa baik model dapat mengklasifikasikan data secara keseluruhan. Namun, perlu diingat bahwa *binary accuracy* dapat memberikan hasil yang bias jika terdapat ketidakseimbangan dalam jumlah data pada kelas positif dan negatif. |
| Performa Model | Performa model yang telah dibuat termasuk ke dalam kategori yang cukup baik dan ideal dengan tingkat `binary_accuracy` sebesar 94 - 96% dan `loss` sebesar 9 -18%. |
| Kesimpulan | Model yang telah berhasil dibangun telah diuji coba dapat bekerja dan dapat melakukan klasifikasi kanker payudara dengan tepat, apakah kanker payudara tersebut termasuk ke dalam kanker payudara yang ganas atau jinak. |

## Referensi

[1] World Health Organization, "Kanker payudara",*World Health Organization (WHO)*, 2021, Diambil dari: https://www.who.int/news-room/fact-sheets/detail/breast-cancer
