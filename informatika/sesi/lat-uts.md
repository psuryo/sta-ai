# UNIVERSITAS KATOLIK WIDYA MANDALA SURABAYA
## FAKULTAS TEKNOLOGI INFORMASI
## SOAL LATIHAN PERSIAPAN UTS
### Kecerdasan Buatan — S1 Teknik Informatika

| | |
|---|---|
| **Mata Kuliah** : Kecerdasan Buatan | **Semester** : Genap 2024/2025 |
| **CPMK** : CPMK 1 & CPMK 2 | **Waktu** : 90 menit |
| **Sifat** : Closed book, closed notes | **Cakupan** : Pertemuan 1 – 7 |

---

### PETUNJUK PENGERJAAN

- Soal terdiri dari Bagian A (Teori, 60 poin) dan Bagian B (Studi Kasus, 40 poin).
- Tuliskan jawaban di lembar jawab yang telah disediakan. Penggunaan komputer dan telepon tidak diperbolehkan.
- Jawab dengan terstruktur. Untuk soal hitungan, tunjukkan langkah-langkah penyelesaian.
- Gambar atau diagram sederhana diperbolehkan dan dianjurkan jika memperjelas jawaban.
- Soal ini setara tingkat kesulitannya dengan UTS. Gunakan sebagai tolok ukur kesiapanmu.

---

## BAGIAN A — TEORI (60 Poin)

*Jawab dengan jelas dan terstruktur. Gunakan poin-poin jika diperlukan.*

### Soal 1 — Sejarah, Taksonomi & Cabang AI (20 poin)

**(a) (6 poin)**

Alan Turing mengusulkan sebuah tes pada tahun 1950 sebagai standar kecerdasan mesin. Jelaskan apa itu **Turing Test** dan bagaimana prosedurnya. Kemudian berikan satu argumen **mendukung** dan satu argumen **menolak** Turing Test sebagai ukuran kecerdasan yang valid.

**(b) (6 poin)**

Perhatikan tiga pernyataan berikut dan tentukan masing-masing termasuk **ANI, AGI, atau ASI**. Jelaskan alasanmu:

- "ChatGPT bisa menulis puisi, menjawab pertanyaan sains, dan membantu debugging kode — tapi tidak bisa mengendarai mobil."
- "Sistem AI hipotetis yang dalam satu hari mempelajari semua buku yang pernah ditulis manusia dan mengembangkan teori fisika baru yang belum pernah terpikirkan oleh siapapun."
- "AlphaGo mengalahkan juara dunia Go, tapi tidak bisa bermain catur tanpa dilatih ulang dari awal."

**(c) (8 poin)**

**Neurosymbolic AI** disebut sebagai frontier terkini yang menjanjikan. Jelaskan:

- Apa yang dimaksud dengan Symbolic AI dan mengapa ia memiliki keterbatasan dalam menangani data tak terstruktur?
- Apa yang dimaksud dengan Sub-symbolic AI dan mengapa ia memiliki keterbatasan dalam hal interpretabilitas dan penalaran logis?
- Bagaimana Neurosymbolic AI mencoba menggabungkan keunggulan keduanya? Gunakan AlphaGeometry (Google DeepMind, 2024) sebagai contoh konkret.

### Soal 2 — Algoritma Machine Learning (20 poin)

**(a) (5 poin)**

**Support Vector Machine (SVM)** menggunakan konsep "margin" dalam membangun keputusan klasifikasi.

- Jelaskan apa yang dimaksud dengan margin dalam SVM dan mengapa memaksimalkan margin menghasilkan model yang lebih general.
- Jelaskan fungsi kernel dalam SVM dan berikan contoh kasus di mana kernel RBF (Gaussian) lebih tepat digunakan daripada kernel linear.
- SVM dikenal tidak cocok untuk dataset sangat besar. Jelaskan alasan teknisnya.

**(b) (7 poin)**

Jelaskan perbedaan antara **Gini Impurity** dan **Information Gain (Entropy)** sebagai kriteria pemilihan split pada Decision Tree.

Kemudian perhatikan node berikut yang sedang dipertimbangkan untuk dipecah:

| Node | Kelas A | Kelas B | Total |
|---|---|---|---|
| Parent | 40 | 60 | 100 |
| Child Kiri | 35 | 15 | 50 |
| Child Kanan | 5 | 45 | 50 |

Hitung **Gini Impurity** untuk node Parent, Child Kiri, dan Child Kanan. Kemudian hitung **Weighted Gini** setelah split ini, dan tentukan apakah split ini layak dilakukan.

**(c) (8 poin)**

Jelaskan konsep **Bagging (Bootstrap Aggregating)** yang menjadi fondasi Random Forest. Dalam penjelasanmu, sertakan:

- Apa itu bootstrap sample dan berapa persentase data yang rata-rata masuk ke setiap tree?
- Mengapa menggunakan subset fitur acak di setiap split menghasilkan tree yang lebih beragam (diverse)?
- Apa itu Out-of-Bag (OOB) score dan apa manfaatnya dibanding menggunakan validation set terpisah?
- Jelaskan dalam satu kalimat mengapa Random Forest memiliki varians lebih rendah dari Decision Tree tunggal, menggunakan prinsip statistik yang mendasarinya.

### Soal 3 — Evaluasi & Pemahaman Konseptual (20 poin)

**(a) (8 poin)**

Sebuah model klasifikasi untuk mendeteksi email phishing menghasilkan confusion matrix berikut:

| | Prediksi: Phishing | Prediksi: Normal |
|---|---|---|
| **Aktual: Phishing** | 156 | 44 |
| **Aktual: Normal** | 38 | 1762 |

Hitung: (1) Akurasi, (2) Presisi untuk kelas "Phishing", (3) Recall untuk kelas "Phishing", (4) F1-Score.

Kemudian tentukan: dalam konteks sistem keamanan email perusahaan, mana yang lebih berbahaya — **false positive** (email normal dianggap phishing) atau **false negative** (email phishing dianggap normal)? Jelaskan implikasi bisnisnya dan metrik mana yang harus diprioritaskan.

**(b) (6 poin)**

Jelaskan konsep **bias-variance tradeoff** dalam Machine Learning:

- Apa yang dimaksud dengan high bias (underfitting) dan bagaimana gejalanya terlihat dari data training vs testing?
- Apa yang dimaksud dengan high variance (overfitting) dan bagaimana gejalanya terlihat?
- Gambarkan kurva sederhana (sketsa tangan) yang menunjukkan hubungan antara kompleksitas model dengan training error dan test error.
- Di manakah posisi "sweet spot" model yang ideal pada kurva tersebut?

**(c) (6 poin)**

Kamu dihadapkan pada dua dataset untuk dua masalah yang berbeda. Tentukan **paradigma ML yang tepat** (supervised/unsupervised) dan **tugas spesifiknya** (klasifikasi/regresi/klasterisasi/anomaly detection), serta **satu algoritma yang paling sesuai** untuk masing-masing:

- Dataset A: Rekaman 500.000 transaksi ATM per hari, tidak ada label "fraud" atau "normal". Tim keamanan bank ingin menemukan transaksi yang mencurigakan secara otomatis.
- Dataset B: Data historis 5 tahun produksi pabrik baja — suhu tungku, tekanan, kecepatan pendinginan, dan kualitas output (skor 0–100). Manajer ingin memprediksi skor kualitas sebelum produk selesai.

---

## BAGIAN B — STUDI KASUS (40 Poin)

*Baca setiap kasus dengan seksama. Jawablah dengan analisis terstruktur dan berikan justifikasi untuk setiap keputusan.*

### Soal 4 — Studi Kasus: Sistem Prediksi Harga Tiket Pesawat (20 poin)

**KONTEKS**

Startup TerbangCerdas sedang membangun aplikasi yang membantu pengguna menentukan **kapan waktu terbaik membeli tiket pesawat** agar mendapatkan harga termurah. Mereka mengumpulkan data dari 3 maskapai domestik selama 2 tahun: rute penerbangan, tanggal keberangkatan, jumlah hari pembelian sebelum keberangkatan (H-berapa), waktu pembelian (pagi/siang/malam), musim (liburan/biasa), kapasitas kursi tersisa (%), dan harga tiket aktual (Rp). Total dataset: 2,4 juta baris.

Selain prediksi harga, tim juga ingin memahami **pola pengguna aplikasi** mereka: apakah ada kelompok pengguna yang selalu beli di menit-menit terakhir, yang selalu plan jauh-jauh hari, dll. — untuk keperluan personalisasi fitur aplikasi.

**(a) (4 poin)**

Untuk masalah **prediksi harga tiket**, tentukan:

- Paradigma ML dan tugas spesifiknya (disertai alasan)
- Variabel target (label) yang tepat
- Minimal empat fitur dari dataset yang paling prediktif dan jelaskan mengapa setiap fitur itu relevan
- Satu fitur yang mungkin terlihat relevan tapi sebaiknya tidak dimasukkan langsung — dan jelaskan alasannya

**(b) (4 poin)**

Untuk masalah **segmentasi pengguna**, tentukan:

- Paradigma ML yang tepat dan mengapa tidak bisa menggunakan supervised learning untuk masalah ini
- Antara K-Means dan DBSCAN, mana yang lebih tepat untuk dataset 2,4 juta baris ini? Berikan minimal dua alasan.
- Bagaimana tim akan menentukan jumlah segmen yang optimal? Jelaskan metode yang digunakan.

**(c) (6 poin)**

Tim melakukan data preparation dan menemukan kondisi berikut. Untuk **setiap kondisi**, jelaskan langkah yang harus diambil dan alasannya:

- Kolom "kapasitas kursi tersisa (%)" memiliki 8,3% nilai kosong (missing values)
- Kolom "rute penerbangan" berisi teks seperti "CGK-SUB", "SUB-DPS", dll. (kategorikal)
- Kolom "jumlah hari sebelum keberangkatan" memiliki rentang 1–365, sedangkan "kapasitas tersisa (%)" rentangnya 0–100
- Tim menemukan 2.100 baris di mana harga tiket tercatat Rp 0 — kemungkinan error sistem

**(d) (6 poin)**

Tim mengevaluasi dua model untuk prediksi harga dan mendapatkan hasil berikut pada **test set**:

| Model | RMSE (Rp) | MAE (Rp) |
|---|---|---|
| Random Forest | 87.500 | 51.200 |
| Gradient Boosting | 74.200 | 55.800 |

Menariknya, Gradient Boosting memiliki RMSE lebih rendah tapi MAE lebih tinggi dibanding Random Forest. **Jelaskan mengapa hal ini bisa terjadi** (kaitkan dengan karakteristik matematika RMSE vs MAE). Kemudian tentukan model mana yang sebaiknya dipilih untuk aplikasi konsumen, dan berikan justifikasinya.

### Soal 5 — Studi Kasus: Klasifikasi Ulasan Produk E-commerce (20 poin)

**KONTEKS**

**Platform TokoBesar** memiliki 18 juta ulasan produk dari 5 juta pengguna. Tim data science ingin membangun sistem yang secara otomatis mengklasifikasikan setiap ulasan ke dalam tiga kategori: **Positif, Netral,** atau **Negatif** — sehingga laporan sentimen bisa dikirim ke setiap seller setiap hari tanpa harus dibaca manual. Dataset yang tersedia: 18 juta ulasan teks, dan sebuah tim anotator telah memberi label pada 500.000 ulasan secara manual.

Distribusi label pada 500.000 ulasan berlabel: **Positif: 71%, Netral: 11%, Negatif: 18%**.

**(a) (4 poin)**

Klasifikasikan masalah ini secara lengkap: paradigma ML, tugas, jumlah kelas, dan jenis model yang paling tepat digunakan. Kemudian jawab: apakah 500.000 sampel berlabel dari 18 juta total ulasan sudah cukup untuk melatih model yang andal? Berikan argumenmu.

**(b) (6 poin)**

Tim mengusulkan dua pendekatan berbeda untuk menangani 17,5 juta ulasan yang **belum berlabel**:

- Pendekatan 1: Latih model hanya pada 500.000 ulasan berlabel, lalu gunakan untuk memprediksi 17,5 juta sisanya.
- Pendekatan 2: Gunakan 17,5 juta ulasan tanpa label untuk tahap pre-training, kemudian fine-tune dengan 500.000 ulasan berlabel.

Jelaskan **perbedaan konseptual** kedua pendekatan ini. Pendekatan mana yang kemungkinan menghasilkan model lebih baik, dan mengapa? Kaitkan jawabanmu dengan konsep **supervised** vs **semi-supervised learning**.

**(c) (4 poin)**

Distribusi label **71% Positif : 11% Netral : 18% Negatif** menimbulkan potensi masalah. Jelaskan:

- Apa masalah yang bisa timbul dari distribusi ini jika model dilatih tanpa penanganan khusus?
- Berikan dua strategi konkret untuk mengatasinya
- Metrik evaluasi mana yang paling tepat untuk kasus multi-kelas tidak seimbang ini — dan mengapa Accuracy saja tidak memadai?

**(d) (6 poin)**

Setelah model selesai dilatih dan di-deploy, tim menemukan bahwa model bekerja sangat baik untuk ulasan dalam Bahasa Indonesia formal, tetapi performanya buruk untuk ulasan yang menggunakan **bahasa gaul, singkatan, dan campur kode (code-switching)** seperti: *"Produknya oke bgt sih, tp pengiriman lemot parah :(" atau "Barang ori, fast respon, highly recommended dah pokonya."*

- Apa penyebab mendasar masalah ini? Kaitkan dengan konsep distribusi data training vs data dunia nyata.
- Apakah ini termasuk model drift? Jelaskan perbedaan antara data drift dan concept drift, lalu tentukan ini termasuk yang mana.
- Sebutkan satu solusi jangka pendek (bisa segera dilakukan) dan satu solusi jangka panjang (memerlukan resources lebih besar) untuk mengatasi masalah ini.

---

## TABEL PENILAIAN

| No | Soal | CPMK | Poin | Nilai |
|---|---|---|---|---|
| 1a | Turing Test — argumen pro & kontra | CPMK 1 | 6 | |
| 1b | Klasifikasi ANI, AGI, ASI dari pernyataan | CPMK 1 | 6 | |
| 1c | Neurosymbolic AI & keterbatasan dua aliran | CPMK 1 | 8 | |
| 2a | SVM — margin, kernel, skalabilitas | CPMK 2 | 5 | |
| 2b | Gini Impurity — perhitungan & interpretasi | CPMK 2 | 7 | |
| 2c | Bagging & fondasi Random Forest | CPMK 2 | 8 | |
| 3a | Hitung & interpretasi metrik klasifikasi | CPMK 2 | 8 | |
| 3b | Bias-variance tradeoff & kurva error | CPMK 2 | 6 | |
| 3c | Identifikasi paradigma ML dari dataset | CPMK 1+2 | 6 | |
| 4a | Identifikasi masalah & fitur prediksi harga | CPMK 1+2 | 4 | |
| 4b | Pemilihan algoritma clustering + penentuan K | CPMK 2 | 4 | |
| 4c | Data preparation — 4 skenario | CPMK 2 | 6 | |
| 4d | RMSE vs MAE — analisis & pemilihan model | CPMK 2 | 6 | |
| 5a | Klasifikasi masalah & kecukupan data | CPMK 1+2 | 4 | |
| 5b | Supervised vs semi-supervised learning | CPMK 1+2 | 6 | |
| 5c | Imbalanced multi-class & metrik evaluasi | CPMK 2 | 4 | |
| 5d | Data drift vs concept drift & solusi | CPMK 2 | 6 | |
| **TOTAL** | | | **100** | |

*Soal latihan ini setara tingkat kesulitannya dengan UTS. Jika kamu bisa menyelesaikan seluruh soal dalam 90 menit, kamu siap menghadapi UTS.*

**Selamat belajar!**
