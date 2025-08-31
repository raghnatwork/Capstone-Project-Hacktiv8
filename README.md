# Capstone-Project-Hacktiv8

Link Google Collab : https://colab.research.google.com/drive/1mo4ufOuOih_8Xb5DJkIPe0hAoFcD6chm?usp=sharing
Klasifikasi Data Hepatitis

**Latar Belakang**
Hepatitis merupakan salah satu penyakit peradangan hati yang menjadi masalah kesehatan global dan dapat berujung pada kematian. Kemampuan untuk memprediksi prognosis atau hasil akhir kondisi pasien—apakah akan bertahan hidup (LIVE) atau meninggal (DIE)—sangatlah krusial untuk membantu tenaga medis dalam mengambil keputusan klinis yang tepat dan mengalokasikan sumber daya secara lebih efektif.
Penelitian ini bertujuan untuk membangun model klasifikasi Random Forest guna memprediksi prognosis pasien (LIVE atau DIE) menggunakan dataset Hepatitis dari UCI. Tantangan utama dalam dataset berisi 155 rekam medis ini adalah adanya ketidakseimbangan kelas yang signifikan, di mana jumlah data 'LIVE' jauh lebih banyak daripada 'DIE', sehingga berisiko menghasilkan model yang bias dan tidak andal dalam mendeteksi kelas 'DIE' yang kritis.

**Evaluasi Awal**
Evaluasi model awal menunjukkan akurasi sebesar 81%, namun angka ini menutupi masalah performa yang serius. Analisis lebih lanjut mengungkap kinerja yang sangat tidak seimbang, di mana model sangat lemah dalam mendeteksi kelas minoritas 'DIE'. Kelemahan fatal ini terlihat pada nilai Recall untuk kelas 'DIE' yang hanya 50%, artinya model gagal mengidentifikasi setengah dari total pasien yang berisiko. Hal ini membuktikan bahwa ketidakseimbangan data telah menghasilkan model awal yang bias dan tidak dapat diandalkan.

**Solusi**
Untuk mengatasi masalah model yang tidak seimbang, diterapkanlah sebuah teknik oversampling bernama SMOTE (Synthetic Minority Over-sampling Technique). Solusi ini bekerja dengan cara menciptakan sampel 'sintetis' atau 'buatan' baru untuk kelas minoritas ('DIE') secara cerdas, berdasarkan karakteristik dari sampel yang sudah ada. Proses ini diaplikasikan hanya pada data latih untuk menyeimbangkan distribusi kelas, sehingga jumlah sampel 'DIE' menjadi sama banyaknya dengan sampel 'LIVE'. 

**Evaluasi Akhir**
Setelah dilatih ulang dengan data SMOTE, model baru menunjukkan peningkatan signifikan. Kemampuan model dalam mendeteksi kasus kritis membaik, di mana Recall untuk kelas 'DIE' berhasil naik dari 50% menjadi 60%. Peningkatan ini juga turut menaikkan akurasi keseluruhan model menjadi 85%, membuktikan bahwa SMOTE berhasil menciptakan model akhir yang lebih andal dan seimbang.

**Kesimpulan**
Evaluasi model Random Forest awal mengungkap kinerja yang bias akibat data tidak seimbang, dengan kelemahan fatal pada nilai Recall kelas 'DIE' yang hanya 50%. Untuk mengatasi masalah ini, teknik SMOTE diterapkan pada data latih untuk menyeimbangkan distribusi kelas dengan cara menciptakan sampel sintetis. Hasilnya, evaluasi akhir pada model yang telah dilatih ulang menunjukkan peningkatan signifikan, di mana Recall untuk kelas 'DIE' naik menjadi 60% dan akurasi keseluruhan meningkat menjadi 85%. Hal ini membuktikan bahwa SMOTE merupakan langkah krusial untuk mengubah model yang tidak andal menjadi solusi prediksi yang jauh lebih seimbang dan efektif.
