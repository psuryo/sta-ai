# Kunci Jawaban UTS Kecerdasan Buatan (INF201)

**Program Studi:** Informatika  
**Semester:** 3  
**Tahun Akademik:** 2026/2027  
**Jenis dokumen:** Kunci jawaban dan pedoman koreksi  
**Catatan:** Jawaban berikut merupakan acuan. Jawaban alternatif dapat diterima jika benar secara konsep dan didukung alasan yang logis.

---

## Soal 1 — Konsep Dasar dan Taksonomi AI (20 poin)

### 1.1 Symbolic AI dan Sub-symbolic AI

**Symbolic AI** merepresentasikan pengetahuan dengan simbol, aturan eksplisit, logika, atau struktur pengetahuan yang dapat ditelusuri. Sistem mengambil keputusan dengan memanipulasi representasi tersebut.

Contoh:
1. **Sistem pakar berbasis aturan** untuk diagnosis kerusakan: menggunakan aturan seperti *IF gejala A dan gejala B THEN kemungkinan kerusakan C*. Ini termasuk Symbolic AI karena pengetahuan dinyatakan secara eksplisit dalam aturan.
2. **Sistem berbasis logika untuk pembuktian teorema atau perencanaan**: menggunakan fakta, operator logika, dan aturan inferensi untuk memperoleh kesimpulan atau urutan tindakan.

**Sub-symbolic AI** mempelajari pola dari data menggunakan representasi numerik, parameter, atau jaringan yang tidak seluruhnya ditulis sebagai aturan eksplisit oleh manusia.

Contoh:
1. **Jaringan saraf untuk pengenalan wajah**: mempelajari representasi visual dan pola dari contoh gambar.
2. **Model deep learning untuk pengenalan suara**: mempelajari hubungan antara sinyal audio dan transkripsi dari data pelatihan.

Sebuah sistem hibrida dapat menggabungkan kedua pendekatan tersebut, sehingga klasifikasi tidak selalu mutlak untuk seluruh komponen sistem.

### 1.2 ANI, AGI, ASI, dan posisi AI saat ini

- **ANI (*Artificial Narrow Intelligence*)**: AI yang dirancang atau dilatih untuk tugas atau kelompok tugas tertentu, misalnya penerjemahan, rekomendasi produk, deteksi objek, dan chatbot.
- **AGI (*Artificial General Intelligence*)**: konsep AI yang mampu belajar, memahami, dan menerapkan pengetahuan pada beragam tugas intelektual secara umum, dengan fleksibilitas yang mendekati kemampuan manusia. Definisi dan tolok ukur AGI masih diperdebatkan.
- **ASI (*Artificial Superintelligence*)**: konsep hipotetis AI yang melampaui kemampuan manusia secara luas pada sebagian besar atau seluruh ranah kognitif.

**Posisi saat ini:** Sistem AI yang digunakan secara luas saat ini umumnya memiliki kemampuan yang masih terbatas oleh tugas, konteks, data, alat, dan cara evaluasinya. Model generatif dapat menjalankan banyak jenis tugas, tetapi hal tersebut tidak dengan sendirinya membuktikan tercapainya AGI. ASI merupakan konsep hipotetis, bukan kemampuan yang telah dibuktikan tersedia secara umum.

Perbedaan utamanya adalah cakupan dan fleksibilitas kemampuan: ANI berfokus pada tugas tertentu; AGI diharapkan dapat mentransfer kemampuan lintas tugas secara umum; ASI secara hipotetis melampaui manusia pada banyak bidang. Pernyataan tentang kapan AGI atau ASI akan tercapai adalah prediksi, bukan fakta pasti.

### 1.3 Hubungan AI, Machine Learning, Deep Learning, dan Generative AI

Pernyataan “Deep Learning dan Machine Learning adalah dua cabang AI yang berdiri sendiri dan tidak saling berhubungan” **salah**.

Diagram sederhana:

```text
Artificial Intelligence (AI)
└── Machine Learning (ML)
    └── Deep Learning (DL)
        └── Banyak pendekatan Generative AI modern
```

Diagram ini merupakan penyederhanaan konseptual, bukan klasifikasi yang mencakup semua sistem generatif. Generative AI adalah kategori berdasarkan tujuan menghasilkan konten; model generatif dapat menggunakan pendekatan selain deep learning, meskipun banyak model generatif modern menggunakan deep learning.

Contoh:
- **ML tanpa deep learning:** model Decision Tree untuk memprediksi pelanggan berhenti berlangganan.
- **Deep learning:** jaringan saraf untuk klasifikasi gambar.
- **Generative AI:** model bahasa besar yang menghasilkan teks, atau model difusi yang menghasilkan gambar.

Dengan demikian, Deep Learning merupakan bagian dari Machine Learning, dan Machine Learning merupakan bagian dari AI.

---

## Soal 2 — Overfitting, Ensemble Learning, dan K-Means (20 poin)

### 2.1 Analisis overfitting

Akurasi training 99,8% dan testing 71,3% menunjukkan kesenjangan generalisasi yang besar dan merupakan indikasi kuat **overfitting**. Model sangat cocok dengan data training, tetapi performanya turun pada data yang belum pernah dilihat.

Kemungkinan penyebab:
- Pohon terlalu kompleks atau terlalu dalam.
- Model mempelajari noise atau pola khusus pada data training.
- Data training tidak cukup mewakili distribusi data nyata.
- Terdapat kebocoran data atau perbedaan distribusi train dan test; hal ini perlu diperiksa, bukan langsung diasumsikan.

Tiga strategi penanganan yang dapat digunakan:
1. **Batasi kompleksitas pohon:** atur `max_depth`, `min_samples_split`, atau `min_samples_leaf`.
2. **Pruning:** pangkas cabang yang tidak membantu generalisasi.
3. **Validasi dan pemilihan hiperparameter:** gunakan validation set atau cross-validation untuk memilih konfigurasi yang memberikan performa generalisasi lebih baik.

Alternatif lain yang layak: menambah data yang representatif, memperbaiki kualitas fitur, mengurangi fitur yang tidak relevan, atau menggunakan ensemble dengan validasi yang benar.

### 2.2 Random Forest dibandingkan Gradient Boosting

| Aspek | Random Forest | Gradient Boosting |
|---|---|---|
| Cara membangun ensemble | Melatih banyak pohon dengan sampel bootstrap dan/atau subset fitur secara acak | Melatih pohon secara berurutan; pohon baru memperbaiki kesalahan atau residual yang belum ditangani model sebelumnya |
| Arah pembangunan tree | Umumnya independen dan dapat dilatih paralel | Bergantung pada model sebelumnya, sehingga umumnya berurutan |
| Strategi reduksi error | Mengurangi varians melalui penggabungan prediksi banyak pohon | Mengurangi loss secara bertahap dengan mengikuti arah gradien fungsi loss |
| Risiko overfitting | Relatif tahan terhadap overfitting dibanding satu pohon, tetapi tetap dapat bermasalah pada data atau pengaturan tertentu | Dapat overfit jika terlalu banyak pohon, pohon terlalu kompleks, atau learning rate tidak sesuai |
| Kecepatan training | Pohon dapat dilatih paralel; sering efisien untuk banyak pohon | Training umumnya lebih sulit diparalelkan karena ketergantungan antariterasi |

Keduanya adalah metode ensemble, tetapi mekanisme pembentukan pohon dan cara meningkatkan performanya berbeda.

### 2.3 Cara kerja K-Means dengan enam titik dan K = 2

Gunakan enam titik dua dimensi berikut:

- A = (1, 1)
- B = (1, 2)
- C = (2, 1)
- D = (8, 8)
- E = (8, 9)
- F = (9, 8)

Kita pilih centroid awal:
- Centroid 1: \(C_1=(1,1)\)
- Centroid 2: \(C_2=(8,8)\)

**Langkah 1 — Hitung jarak dan tetapkan cluster**

K-Means menghitung jarak setiap titik ke kedua centroid, lalu memasukkan titik ke centroid terdekat. Dengan jarak Euclidean, hasil pengelompokan awal:

- Cluster 1: A, B, C
- Cluster 2: D, E, F

**Langkah 2 — Perbarui centroid**

Centroid baru adalah rata-rata koordinat seluruh titik dalam cluster.

Untuk Cluster 1:

\[
C_1=\left(\frac{1+1+2}{3},\frac{1+2+1}{3}\right)
=\left(\frac{4}{3},\frac{4}{3}\right)
\]

Untuk Cluster 2:

\[
C_2=\left(\frac{8+8+9}{3},\frac{8+9+8}{3}\right)
=\left(\frac{25}{3},\frac{25}{3}\right)
\]

**Langkah 3 — Ulangi penetapan cluster**

Hitung kembali jarak setiap titik ke centroid baru dan tetapkan cluster terdekat. Pada contoh ini, keanggotaan cluster tetap A, B, C dan D, E, F.

**Langkah 4 — Konvergensi**

Karena penetapan anggota cluster tidak berubah pada iterasi berikutnya, algoritma telah konvergen pada contoh ini. Secara umum, konvergensi dapat ditentukan ketika keanggotaan cluster tidak berubah, perubahan centroid sangat kecil, atau batas iterasi tercapai.

**Formula jarak Euclidean:**

\[
d(x,c)=\sqrt{\sum_{j=1}^{n}(x_j-c_j)^2}
\]

**Kelemahan utama:** K-Means sensitif terhadap centroid awal dan umumnya kurang cocok untuk cluster dengan bentuk yang tidak cembung atau dengan banyak noise.

**Alternatif:** DBSCAN dapat digunakan ketika cluster memiliki bentuk tidak beraturan dan terdapat noise. Untuk data dengan cluster yang tumpang tindih atau kepadatan berbeda, pemilihan algoritma harus mempertimbangkan karakteristik data; DBSCAN juga memiliki keterbatasan pada kepadatan yang sangat bervariasi.

---

## Soal 3 — Evaluasi Klasifikasi dan Paradigma Machine Learning (20 poin)

### 3.1 Menghitung metrik dari confusion matrix

Dari tabel soal:

| | Prediksi: Kanker | Prediksi: Normal |
|---|---:|---:|
| Aktual: Kanker | TP = 87 | FN = 13 |
| Aktual: Normal | FP = 22 | TN = 378 |

Jumlah data:

\[
N=87+13+22+378=500
\]

**Accuracy**

$$ \text{Accuracy} = \frac{\text{TP} + \text{TN}}{N} = \frac{87 + 378}{500} = \frac{465}{500} = 0.93 $$
Hasil: **93,00%**.

**Precision kelas Kanker**

\[
Precision=\frac{TP}{TP+FP}
=\frac{87}{87+22}
=\frac{87}{109}\approx0{,}7982
\]

Hasil: **79,82%**.

**Recall kelas Kanker**

\[
Recall=\frac{TP}{TP+FN}
=\frac{87}{87+13}
=\frac{87}{100}=0{,}87
\]

Hasil: **87,00%**.

**F1-Score kelas Kanker**

\[
F1=2\frac{Precision\times Recall}{Precision+Recall}
\]

\[
F1\approx 2\frac{0{,}7982\times0{,}87}{0{,}7982+0{,}87}
\approx0{,}8325
\]

Hasil: **83,25%**.

### 3.2 Metrik yang paling kritis untuk deteksi kanker

Recall sangat penting karena false negative berarti pasien yang sebenarnya memiliki kanker diprediksi normal. Kesalahan ini dapat menunda pemeriksaan dan penanganan.

Namun, false positive juga memiliki konsekuensi, seperti pemeriksaan lanjutan, biaya, kecemasan, dan penggunaan sumber daya. Oleh karena itu, recall perlu diprioritaskan sesuai tujuan klinis, tetapi tidak boleh dipisahkan dari precision, validasi klinis, dan evaluasi konsekuensi kesalahan.

### 3.3 Mengapa akurasi 96% dapat menyesatkan?

Dataset berisi:
- 9.600 sampel negatif.
- 400 sampel positif.
- Total 10.000 sampel.

Proporsi kelas negatif adalah 96%, sedangkan kelas positif hanya 4%. Distribusi ini disebut **class imbalance** atau ketidakseimbangan kelas.

Model yang selalu memprediksi negatif memperoleh:

\[
Accuracy=\frac{9600}{10000}=96\%
\]

Meskipun akurasinya 96%, model tersebut tidak pernah mendeteksi sampel positif. Recall untuk kelas positif adalah 0% sehingga model mungkin tidak berguna untuk tujuan deteksi positif.

Metrik yang lebih relevan:
- **Recall kelas positif:** mengukur proporsi kasus positif yang berhasil ditemukan.
- **Precision kelas positif:** mengukur proporsi prediksi positif yang benar.
- **F1-score:** menyeimbangkan precision dan recall.
- **PR-AUC:** berguna untuk menilai trade-off precision-recall pada kelas positif yang jarang.
- **Confusion matrix:** memperlihatkan jumlah TP, FP, FN, dan TN secara langsung.

Metrik utama harus disesuaikan dengan biaya false positive dan false negative dalam konteks penggunaan.

### 3.4 Supervised learning dan unsupervised learning

| Aspek | Supervised Learning | Unsupervised Learning |
|---|---|---|
| Ketersediaan label | Data training memiliki label atau target yang diketahui | Data tidak memerlukan label target untuk proses pembelajaran utama |
| Tujuan | Belajar memetakan fitur ke target, misalnya klasifikasi atau regresi | Menemukan struktur, kelompok, pola, atau representasi dalam data |
| Contoh | Memprediksi apakah transaksi termasuk penipuan berdasarkan label historis | Mengelompokkan pelanggan berdasarkan pola pembelian menggunakan K-Means |

---

## Soal 4 — Studi Kasus Apotek Sehat Prima (20 poin)

### 4.1 Prediksi stok obat

**Paradigma:** Supervised learning, jika tersedia target historis yang dapat digunakan untuk melatih dan mengevaluasi model.

**Jenis tugas:**
- **Klasifikasi**, jika targetnya adalah apakah suatu obat di cabang tertentu akan kehabisan stok dalam tujuh hari ke depan (`habis` atau `tidak habis`).
- **Regresi**, jika targetnya adalah jumlah permintaan atau jumlah unit obat yang diperkirakan terjual dalam tujuh hari ke depan.

Untuk tujuan operasional, sistem juga dapat menggabungkan prediksi permintaan dengan data persediaan dan waktu pengadaan untuk memperkirakan risiko kehabisan stok.

**Contoh variabel target klasifikasi:** `risiko_habis_7_hari`.

**Fitur yang relevan:**
- Identitas obat dan cabang.
- Riwayat penjualan harian atau mingguan.
- Hari dalam minggu, bulan, hari libur, dan pola musiman.
- Stok saat ini dan riwayat perubahan stok.
- Riwayat penerimaan barang dan pengadaan.
- Waktu tunggu pemasok dan frekuensi pengiriman.
- Pola permintaan berdasarkan cabang.
- Jika relevan dan sesuai kebijakan privasi, agregat karakteristik transaksi atau penggunaan resep.

**Data tambahan yang diperlukan:**
1. Stok saat ini per obat dan cabang.
2. Riwayat stok dan tanggal terjadinya kehabisan stok.
3. Barang masuk, retur, dan penyesuaian stok.
4. Pesanan pengadaan yang belum tiba.
5. Waktu tunggu pemasok dan jadwal pengiriman.
6. Jika tersedia, informasi promosi, hari libur, dan faktor musiman.

Data transaksi penjualan saja belum tentu cukup. Penjualan yang tercatat nol, misalnya, dapat berarti tidak ada permintaan atau obat sedang kosong. Informasi stok diperlukan untuk membedakan kedua kondisi tersebut.

### 4.2 Segmentasi pelanggan

**Paradigma:** Unsupervised learning, karena tujuan utamanya menemukan kelompok pelanggan tanpa target kelas yang telah ditentukan.

**Pilihan awal yang masuk akal: K-Means**, setelah transaksi diubah menjadi fitur pada tingkat pelanggan dan fitur numerik yang relevan dipersiapkan.

Contoh fitur segmentasi:
- Frekuensi transaksi.
- Rata-rata nilai transaksi.
- Total belanja pada periode tertentu.
- Keragaman kategori atau jenis obat yang dibeli.
- Jarak waktu antartransaksi.
- Proporsi pembelian dengan resep, jika relevan dan digunakan secara sah.

**Alasan memilih K-Means:**
- Relatif efisien untuk data berskala besar.
- Mudah dipahami dan hasil cluster dapat diringkas untuk kebutuhan program loyalitas.
- Dapat digunakan sebagai baseline, kemudian jumlah cluster dan kualitas segmentasi dievaluasi.

**Perbandingan alternatif:**
- **DBSCAN:** berguna untuk menemukan cluster berbentuk tidak beraturan dan mendeteksi noise, tetapi dapat menantang pada data besar dan kepadatan cluster yang berbeda-beda.
- **Hierarchical Clustering:** membantu mengeksplorasi struktur bertingkat, tetapi pendekatan klasik dapat mahal dari sisi waktu dan memori untuk data berukuran sangat besar.

**Catatan skala:** 1,2 juta transaksi tidak berarti harus melakukan clustering langsung atas setiap transaksi. Segmentasi pelanggan biasanya dilakukan setelah membuat satu baris fitur per pelanggan. Jumlah pelanggan unik harus diketahui untuk memperkirakan kebutuhan komputasi. Hasil clustering perlu diuji kegunaannya bagi program loyalitas, bukan hanya dinilai dari bentuk cluster.

### 4.3 Data preparation untuk prediksi stok

Berikut contoh langkah preprocessing yang sesuai:

| Langkah | Tujuan | Relevansi terhadap data apotek |
|---|---|---|
| 1. Membersihkan data hilang dan duplikasi | Mengurangi kesalahan pencatatan dan penghitungan transaksi ganda | Transaksi duplikat dapat membuat permintaan obat tampak lebih tinggi |
| 2. Menyeragamkan tipe dan format tanggal | Memastikan urutan waktu dan agregasi konsisten | Data mencakup tiga tahun sehingga pola harian, mingguan, dan musiman perlu dianalisis |
| 3. Menggabungkan data transaksi dan persediaan | Menyediakan konteks stok, penerimaan, dan kondisi kehabisan stok | Penjualan rendah tidak selalu berarti permintaan rendah jika stok kosong |
| 4. Agregasi berdasarkan obat, cabang, dan periode | Membentuk unit observasi yang konsisten | Target prediksi adalah risiko atau kebutuhan stok di tiap cabang dalam tujuh hari |
| 5. Membuat fitur waktu | Mengidentifikasi tren, pola mingguan, dan musim | Permintaan dapat berubah saat akhir pekan, hari libur, atau periode tertentu |
| 6. Encoding fitur kategori | Mengubah kategori seperti cabang dan obat menjadi representasi yang dapat diproses model | Identitas obat dan cabang merupakan fitur kategoris |
| 7. Menangani pencilan dan anomali | Memeriksa lonjakan tidak biasa atau kesalahan pencatatan | Pembelian besar, retur, atau kesalahan input dapat memengaruhi prediksi |
| 8. Membagi data berdasarkan waktu | Menguji model pada periode yang lebih baru daripada data training | Menghindari kebocoran informasi masa depan ke dalam training |

Mahasiswa diminta minimal empat langkah. Nilai penuh layak diberikan jika setidaknya empat langkah dijelaskan dengan benar, tujuan jelas, dan kaitannya dengan karakteristik data diterangkan.

Untuk evaluasi prediksi stok, pembagian data secara kronologis lebih tepat daripada pembagian acak biasa jika tujuan model adalah memprediksi periode mendatang.

---

## Soal 5 — Studi Kasus Deteksi Helm pada CCTV (20 poin)

### 5.1 Paradigma dan tugas Machine Learning

**Paradigma utama:** Supervised learning, karena 8.200 foto memiliki label manual yang dapat digunakan untuk melatih model.

**Tugas yang sesuai:** Object detection apabila sistem harus mendeteksi lokasi pekerja dan helm pada gambar. Jika gambar atau potongan gambar sudah ditentukan dan sistem hanya memutuskan apakah pekerja memakai helm, tugas dapat dimodelkan sebagai klasifikasi gambar.

**Input:** Gambar atau frame video CCTV.

**Output:** Prediksi pekerja memakai helm atau tidak memakai helm; untuk object detection, output juga dapat mencakup bounding box dan confidence score. Sistem kemudian dapat menerapkan aturan untuk mengirim notifikasi kepada supervisor.

Foto yang belum berlabel tidak otomatis menjadikan masalah ini unsupervised learning. Data tanpa label dapat digunakan untuk eksplorasi, pretraining, atau semi-supervised learning, tetapi model deteksi yang diawasi tetap memerlukan target berlabel untuk pelatihan dan evaluasi yang sesuai.

**Apakah 8.200 foto berlabel cukup?**

Tidak dapat dipastikan hanya dari jumlahnya. Kecukupan bergantung pada:
- Jumlah contoh pekerja tanpa helm yang benar-benar berlabel.
- Variasi kamera, sudut pandang, jarak, pencahayaan, dan kondisi cuaca.
- Variasi bentuk dan warna helm serta seragam.
- Kualitas label dan konsistensi anotasi.
- Kemiripan data training dengan kondisi penerapan.
- Kinerja pada data uji yang terpisah dan representatif.

Foto dari frame video yang berdekatan dapat sangat mirip. Karena itu, pembagian training dan testing sebaiknya mempertimbangkan kamera, waktu, atau urutan video agar evaluasi tidak terlalu optimistis.

### 5.2 Ketidakseimbangan kelas

Jumlah data:
- Memakai helm: 11.900 foto.
- Tidak memakai helm: 2.100 foto.
- Total: 14.000 foto.

Proporsi kelas:
- Memakai helm: \(11900/14000=85\%\).
- Tidak memakai helm: \(2100/14000=15\%\).

Data berlabel manual berjumlah 8.200 foto, tetapi distribusi kelas khusus di antara foto berlabel tidak disebutkan. Oleh sebab itu, proporsi keseluruhan tidak boleh langsung dianggap sama dengan proporsi subset berlabel.

Jika ketidakseimbangan juga terjadi pada data training, model dapat cenderung memprediksi kelas mayoritas dan melewatkan pekerja tanpa helm. Akurasi keseluruhan yang tinggi belum menjamin kemampuan mendeteksi pelanggaran K3.

**Dua strategi penanganan:**

1. **Class weighting:** memberikan penalti lebih besar untuk kesalahan pada kelas pekerja tanpa helm.
2. **Oversampling atau augmentasi kelas minoritas:** menambah variasi contoh kelas tanpa helm dalam training, dengan tetap memastikan variasi yang dihasilkan realistis.

Alternatif lain termasuk undersampling kelas mayoritas atau mengumpulkan dan memberi label tambahan pada contoh kelas minoritas. Evaluasi tetap harus menggunakan data uji yang mewakili kondisi lapangan.

### 5.3 Pengaruh threshold 0,3 dan 0,5

Threshold adalah batas confidence untuk memutuskan suatu prediksi sebagai positif, dalam konteks ini misalnya “pekerja tanpa helm”.

Jika threshold diturunkan dari 0,5 menjadi 0,3:
- Lebih banyak prediksi akan ditandai sebagai positif.
- **Recall cenderung meningkat**, karena lebih banyak pekerja tanpa helm terdeteksi.
- **Precision cenderung menurun**, karena notifikasi palsu dapat bertambah.
- **F1-score tidak selalu meningkat**; nilainya bergantung pada perubahan precision dan recall.

Jika threshold dinaikkan, kecenderungan sebaliknya biasanya terjadi: prediksi positif berkurang, precision dapat meningkat, dan recall dapat menurun. Ini merupakan kecenderungan umum, bukan jaminan untuk setiap dataset.

**Rekomendasi:** Uji threshold 0,3 dan 0,5 pada validation set yang representatif. Untuk sistem K3, recall kelas “tanpa helm” perlu menjadi prioritas karena pekerja yang tidak terdeteksi dapat mengalami risiko keselamatan. Namun, jumlah notifikasi palsu juga perlu diukur agar supervisor tidak mengalami *alert fatigue*.

Threshold akhir harus ditentukan berdasarkan hasil validasi, kapasitas tindak lanjut, dan tingkat risiko yang dapat diterima—bukan hanya memilih angka yang lebih rendah.

### 5.4 Penurunan performa setelah tiga bulan

Akurasi turun dari 91% menjadi 74% saat proyek memasuki tahap finishing. Seragam berubah dari oranye menjadi putih dan warna helm makin beragam.

Fenomena yang mungkin terjadi adalah **data drift** atau **distribution shift**, yaitu perubahan distribusi data input dibandingkan data yang digunakan saat model dilatih. Jika perubahan tersebut menyebabkan hubungan antara fitur dan label ikut berubah, kondisi ini dapat berkaitan dengan concept drift. Dari informasi soal saja, data drift merupakan penjelasan langsung yang paling kuat; concept drift belum dapat dipastikan tanpa analisis tambahan.

Penyebab yang mungkin:
- Model terlalu mengandalkan warna seragam atau helm yang dominan pada data training.
- Kondisi visual pada tahap finishing berbeda dari kondisi sebelumnya.
- Data training tidak cukup mewakili variasi warna, pencahayaan, dan lingkungan proyek.

**Solusi jangka pendek:**
- Audit kesalahan pada data terbaru, ukur precision dan recall per kondisi, dan jika diperlukan sesuaikan threshold untuk mengurangi risiko pekerja tanpa helm terlewat sambil mengawasi beban notifikasi.

**Solusi jangka panjang:**
- Kumpulkan dan labeli data dari berbagai tahap proyek, variasi seragam, warna helm, kamera, sudut, dan pencahayaan; kemudian retrain atau fine-tune model serta evaluasi kembali menggunakan data terbaru yang terpisah.

Pemantauan berkala perlu dilakukan terhadap recall kelas tanpa helm dan jenis kesalahan, bukan hanya akurasi keseluruhan.

---

## Ringkasan Kunci Numerik

| Bagian | Hasil acuan |
|---|---|
| Soal 3 — Accuracy | 93,00% |
| Soal 3 — Precision kelas Kanker | 79,82% |
| Soal 3 — Recall kelas Kanker | 87,00% |
| Soal 3 — F1-Score kelas Kanker | 83,25% |
| Dataset 9.600 negatif dan 400 positif | Akurasi model yang selalu memprediksi negatif = 96% |
| Foto CCTV secara keseluruhan | 85% memakai helm dan 15% tanpa helm |

## Catatan untuk Dosen

1. Kunci ini adalah acuan, bukan satu-satunya bentuk jawaban yang benar.
2. Terima jawaban alternatif yang secara teknis valid, terutama untuk pemilihan algoritma dan rancangan solusi.
3. Pada soal hitungan, nilai proses dapat diberikan jika formula dan metode benar tetapi ada kesalahan aritmetika kecil.
4. Pada studi kasus, prioritaskan ketepatan alasan, pemahaman risiko, dan kesesuaian solusi terhadap konteks.
5. Total bobot tiap kelompok soal adalah 20 poin, sehingga nilai keseluruhan adalah 100 poin.
