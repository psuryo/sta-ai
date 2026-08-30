# Kecerdasan Buatan — S1 Informatika · UKWMS
### Silabus Revisi 2026/2027 · 14 Pertemuan · 3 SKS

**Dosen:** Philipus Suryo Subandoro
**Program Studi:** S1 Informatika
**Evaluasi:** UTS Teori + UAS Proyek
**Tools Utama:** Python · Scikit-learn · TensorFlow/Keras · LangChain · OpenAI/Claude API · Streamlit

---

## 1. Deskripsi & Capaian Mata Kuliah

### Deskripsi

Mata kuliah Kecerdasan Buatan membahas konsep, teknik, dan aplikasi AI mulai dari Machine Learning klasik hingga Large Language Model modern. Fokus ditempatkan pada **aplikasi AI untuk bisnis dan industri**, bukan derivasi matematis mendalam — karena hal tersebut dicakup di mata kuliah Machine Learning di semester atas. Teknik pemrosesan gambar dasar dicakup di mata kuliah Pengolahan Citra Digital tersendiri; mata kuliah ini menempatkan Computer Vision sebagai studi kasus aplikasi bisnis.

Mahasiswa akan belajar menggunakan tools AI siap pakai, membangun pipeline data sederhana, mengintegrasikan LLM via API, mendeploy model ke aplikasi web, dan menyelesaikan proyek akhir berupa solusi AI untuk masalah bisnis nyata.

### Prasyarat
- Pemrograman Python dasar (variabel, fungsi, OOP)
- Statistika dasar (rata-rata, distribusi, probabilitas)
- Struktur Data & Algoritma

### Capaian Pembelajaran Mata Kuliah (CPMK)

| Kode | Capaian |
|---|---|
| C1 | **Memahami konsep & taksonomi AI** — definisi, cabang, sejarah, perbedaan AI/ML/DL |
| C2 | **Menerapkan Machine Learning** — membangun & mengevaluasi model klasifikasi, regresi, klasterisasi |
| C3 | **Menggunakan Deep Learning & LLM** — CNN sederhana, integrasi LLM via API |
| C4 | **Menerapkan AI untuk bisnis** — solusi end-to-end: prediksi, rekomendasi, chatbot, computer vision |
| C5 | **Mengevaluasi dampak & etika AI** — bias, fairness, regulasi AI Indonesia |
| C6 | **Mengomunikasikan solusi AI** — presentasi teknis & non-teknis ke stakeholder bisnis |

---

## 2. Jadwal Pertemuan

### Blok 1 · P1–P7 → UTS Teori

#### P-01 — Pengantar AI & Lanskap Industri *(sudah berjalan)*
- Definisi, sejarah, cabang AI, dampak di dunia bisnis dan industri global
- **Touch-point konseptual:** akar symbolic AI (search, knowledge representation) yang mendasari agent/tool-use modern — disebut singkat, bukan dibahas mendalam
- *Tipe: Teori*

#### P-02 — Machine Learning: Konsep & Algoritma
- Supervised, unsupervised, reinforcement learning
- Overfitting & evaluasi model **pada level intuisi** (detail matematis/cross-validation mendalam dicakup di MK Machine Learning)
- *Tipe: Teori*

#### P-03 — Praktik ML dengan Python & Scikit-learn
- Klasifikasi & regresi pada dataset bisnis: prediksi churn pelanggan, harga rumah
- Feature engineering ringan (±20 menit pengantar praktis, bukan sesi penuh)
- **Ethics touch-point:** bias dataset — studi kasus model churn/kredit yang bias terhadap kelompok tertentu
- *Tipe: Praktik*

#### P-04 — AI untuk Bisnis: Studi Kasus & Deployment
- Studi kasus penerapan AI di industri
- Deploy model sederhana sebagai aplikasi web menggunakan Streamlit
- **Ethics touch-point:** tanggung jawab saat model masuk ke produksi nyata
- *Tipe: Praktik*

#### P-05 — Deep Learning & Neural Network
- Arsitektur ANN, CNN dasar (konseptual, tanpa derivasi backpropagation)
- Use case bisnis untuk Deep Learning
- *Tipe: Teori*

#### P-06 — Praktik Deep Learning: CNN **atau** Analisis Sentimen
- Pilih satu topik untuk didalami penuh (CNN untuk image classification, **atau** sentiment analysis dengan Keras); topik lain didemokan singkat (±15 menit)
- **Ethics touch-point:** bias dalam data teks/gambar (mis. sentiment analysis bias budaya/bahasa)
- *Tipe: Praktik*

#### P-07 — Review & Persiapan UTS
- Rekap konsep P1–P6, latihan soal, tanya jawab, kisi-kisi UTS
- *Tipe: Review*

**📝 UTS — Ujian Teori** *(setelah Pertemuan 7)*
Pilihan ganda + esai: konsep AI, studi kasus industri, interpretasi output model, pemilihan algoritma

---

### Blok 2 · P8–P14 → UAS Proyek

#### P-08 — LLM & Generative AI
- Cara kerja transformer, GPT, Claude; aplikasi chatbot & summarizer untuk bisnis
- **Ethics touch-point:** hallucination, transparansi ke pengguna
- *Tipe: Teori*

#### P-09 — Prompt Engineering & API Integration
- Zero/few-shot, chain-of-thought; integrasi LLM via API ke aplikasi Python
- *Tipe: Praktik*

#### P-10 — RAG Part 1: Embedding & Vector Database
- Konsep embedding, vector database, LangChain dasar
- *Tipe: Praktik*

#### P-11 — RAG Part 2 & AI untuk Prediksi/Rekomendasi Bisnis
- Menyelesaikan chatbot berbasis dokumen perusahaan (lanjutan P10)
- Pengantar ringkas: demand forecasting, recommendation system, customer segmentation
- **Ethics touch-point:** fairness dalam rekomendasi (filter bubble, diskriminasi harga)
- *Tipe: Praktik*
- ⚠️ **Catatan:** sesi ini menggabung dua topik besar — pertimbangkan penyesuaian bobot tergantung mana yang lebih relevan untuk proyek UAS mahasiswa Anda

#### P-12 — Sintesis Etika AI, Regulasi Indonesia & Computer Vision
- Rekap & sintesis isu bias/fairness yang muncul di P3, P6, P8, P11
- Regulasi AI & perlindungan data di Indonesia (UU PDP, draf regulasi AI)
- Computer Vision sebagai studi kasus aplikasi bisnis (object detection, OCR, quality control) — level "cara pakai", teknik dasar pemrosesan citra dicakup di MK Pengolahan Citra Digital
- *Tipe: Teori*

#### P-13 — Workshop Proyek UAS — Sesi 1
- Pembentukan kelompok, penetapan topik, bimbingan arsitektur solusi AI
- *Tipe: Proyek*

#### P-14 — Workshop Proyek UAS — Sesi 2
- Finalisasi implementasi, persiapan demo & laporan, dry-run presentasi
- *Tipe: Proyek*

**🚀 UAS — Proyek Kelompok** *(setelah Pertemuan 14)*
Demo live solusi AI untuk bisnis nyata + laporan teknis + presentasi 30 menit + tanya jawab individual

---

## 3. Penilaian

| Komponen | Bobot | Keterangan |
|---|---|---|
| Tugas & Praktik Harian | 40% | Tugas individu tiap sesi praktik, laporan praktikum, keaktifan diskusi, kuis singkat |
| UTS — Ujian Teori | 25% | Setelah P-07: konsep AI/ML, studi kasus industri, interpretasi output model |
| UAS — Proyek Kelompok | 35% | Relevansi masalah (20%), kualitas solusi (40%), presentasi & demo (30%), dokumentasi (10%) |

**Konversi Nilai:** A = 85–100 · B+ = 75–84 · B = 65–74 · C+ = 55–64 · C = 45–54 · D = 35–44 · E = 0–34

---

## 4. Referensi

### Buku Wajib
- **Artificial Intelligence: A Modern Approach**, 4th Ed. — Stuart Russell & Peter Norvig (Pearson, 2020). Fondasi konseptual P1–P7. Chapter relevan: 1, 3, 5, 12, 18, 19, 21.
- **Hands-On Machine Learning with Scikit-Learn, Keras & TensorFlow**, 3rd Ed. — Aurélien Géron (O'Reilly, 2022). Praktik P3, P5, P6.
- **Designing Machine Learning Systems** — Chip Huyen (O'Reilly, 2022). Perspektif produksi/deployment untuk P4 dan proyek UAS.

### Sumber Online Gratis
- **Stanford CS221** (cs221.stanford.edu) — pelengkap P1–P5
- **AI For Everyone** — Andrew Ng, Coursera (audit gratis) — bacaan tambahan P1, P8
- **MIT 6.S191: Introduction to Deep Learning** (introtodeeplearning.com) — referensi P5, P6
- **Dokumentasi resmi LangChain** (terbaru) — wajib dicek karena buku cetak cepat basi untuk tooling LLM/RAG

### Laporan Industri
- **Stanford AI Index Report** (aiindex.stanford.edu) — tren riset, adopsi, regulasi, tenaga kerja
- **McKinsey: The State of AI** (mckinsey.com) — statistik adopsi AI perusahaan global, digunakan di P1 dan P8

### Regulasi & Etika (Indonesia)
- UU No. 27 Tahun 2022 tentang Pelindungan Data Pribadi (PDP)
- Draf/rancangan regulasi AI Indonesia terkini — digunakan di P12

---

## 5. Ringkasan Perubahan dari Silabus Sebelumnya

1. **Data preparation & feature engineering** — dari sesi penuh (P4 lama) menjadi pengantar ringkas di P3; detail dipindah ke MK Machine Learning.
2. **P4 baru** — slot yang terbuka diisi "AI untuk Bisnis: Studi Kasus & Deployment" (Streamlit), lebih relevan untuk orientasi bisnis mata kuliah ini.
3. **P6** — CNN dan analisis sentimen tidak lagi digabung dalam satu sesi; pilih satu untuk didalami.
4. **RAG** — dipecah dari satu sesi (P10 lama) menjadi dua (P10–P11), karena kompleksitasnya tidak realistis untuk satu sesi.
5. **Etika AI** — dari satu sesi terkonsentrasi (digabung dengan CV) menjadi touch-point terdistribusi di P3, P4, P6, P8, P11, dengan sintesis dan regulasi Indonesia di P12.
6. **Computer Vision** — tidak lagi mendapat sesi teknis mendalam; menjadi studi kasus aplikasi bisnis di P12, karena teknik dasar pemrosesan citra sudah dicakup MK Pengolahan Citra Digital tersendiri.
7. **Symbolic AI** — tetap tidak mendapat sesi dedicated; disebut sebagai touch-point konseptual singkat di P1, mengingat fokus mata kuliah ini pada aplikasi bisnis, bukan fondasi teori AI komprehensif.
