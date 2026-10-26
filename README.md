# RAG Parameter Exploration

## Informasi Eksperimen

**Nama PDF:**

6639-Article Text-25282-1-10-20230918.pdf

**Jumlah halaman PDF:**

9 page

**Isi / topik PDF secara singkat:**

Penelitian ini membuat model machine learning menggunakan algoritma K-nearest neighbors yang diimplementasikan kepada sebuah website untuk memprediksi customer churn dan customer tidak churn guna untuk mempertahankan pelanggan pada perusahaan telekomunikasi. 

------------------------------------------------------

# Pertanyaan Pengujian

## Pertanyaan 1

Algoritma machine learning apa yang digunakan peneliti untuk memprediksi customer churn pada perusahaan telekomunikasi, dan berapa persentase akurasi yang dihasilkan dari evaluasi model tersebut? (KNN dan akurasi 81%)

## Pertanyaan 2

Metode apa yang diterapkan oleh peneliti untuk mengatasi masalah data yang tidak seimbang (imbalancing data) pada dataset sebelum melakukan pemodelan? (SMOTE-NC)

------------------------------------------------------

# Baseline Configuration

```text
Temperature:     0.2  
TOP_K:           4     
Chunk Size:      100   
Chunk Overlap:   20    
Embedding Model: sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2
LLM Model:       openai/gpt-oss-120b (Groq)
```

Ingest baseline: `pages_read: 9`, `chunks_stored: 88`

------------------------------------------------------

# Experiment 1 - Temperature

Gunakan pertanyaan yang sama pada seluruh percobaan.

## Temperature = 0.0

### Actual Output

**1. Algoritma yang dipakai:** Peneliti menggunakan algoritma **K‑Nearest Neighbors (KNN)** untuk memprediksi churn pelanggan pada perusahaan telekomunikasi 【Source: 6639-Article Text-25282-1-10-20230918.pdf | Page: 1‑2】.  

**Akurasi model:** Persentase akurasi hasil evaluasi model tidak tercantum dalam dokumen yang diunggah, sehingga tidak dapat disampaikan.  

**2. Penanganan data tidak seimbang:** Dokumen tidak menyebutkan metode apa pun yang diterapkan untuk mengatasi masalah data tidak seimbang (imbalancing data) sebelum pemodelan.  

*Jawaban didasarkan pada informasi yang tersedia dalam dokumen; detail yang tidak ada tidak dapat disediakan.

### Observation

Jawaban cukup jelas dan langsung menjawab kedua pertanyaan. Model menyebutkan algoritma KNN, menjelaskan bahwa akurasi tidak tercantum dalam dokumen, dan menyatakan bahwa metode penanganan data tidak seimbang tidak dijelaskan oleh peneliti.

------------------------------------------------------

## Temperature = 0.2

### Actual Output

**1. Algoritma yang dipakai:** Peneliti menggunakan algoritma **K‑nearest neighbors (KNN)** untuk memprediksi churn pelanggan [Source: 6639‑Article Text‑25282‑1‑10‑20230918.pdf, p. 1‑2].

**Akurasi model:** Persentase akurasi hasil evaluasi model tidak tercantum dalam dokumen yang di‑upload.

**2. Penanganan data tidak seimbang:** Dokumen tidak menyebutkan metode apa pun yang diterapkan untuk mengatasi masalah data tidak seimbang (imbalancing data) sebelum pemodelan.

### Observation

Jawaban memiliki isi yang sama dengan temperature 0.0. Perbedaannya hanya pada susunan kalimat dan format sitasi. Tidak ada perubahan informasi yang diberikan, sehingga kedua hasil menunjukkan jawaban yang konsisten pada pengujian ini.

------------------------------------------------------

## Temperature = 0.8

### Actual Output

**1. Algoritma yang dipakai**  
Peneliti menggunakan algoritma **K‑Nearest Neighbors (K‑NN)** untuk memprediksi apakah pelanggan akan churn atau tidak 【Source: 6639-Article Text-25282-1-10-20230918.pdf | Page: 1】【Source: 6639-Article Text-25282-1-10-20230918.pdf | Page: 2】.  

**Persentase akurasi** – Informasi mengenai nilai akurasi yang diperoleh dari evaluasi model tidak terdapat dalam dokumen yang di‑upload.  

**2. Penanganan data tidak seimbang** – Dokumen tidak menyebutkan metode apa yang diterapkan untuk mengatasi masalah data yang tidak seimbang sebelum pemodelan.  

*Jawaban didasarkan pada isi dokumen yang tersedia; bila ada bagian lain yang memuat detail akurasi atau teknik penanganan imbalancing, informasi tersebut tidak tercakup dalam teks yang diberikan.*

### Observation

Jawaban pada temperature 0.8 masih sama dengan temperature 0.0 dan 0.2. Model tetap menyebutkan algoritma KNN, sementara informasi akurasi dan metode penanganan data tidak seimbang tidak ditemukan di dokumen. Perbedaannya ada di cara penjelasan yang sedikit lebih panjang, terutama pada bagian akhir jawaban. Isi jawabannya tetap sama dan tidak ada perubahan fakta yang terlihat.

------------------------------------------------------

## Kesimpulan Experiment Temperature

Apa perubahan yang paling terlihat?

erubahan yang paling terlihat ada pada cara penyampaian jawaban. Pada temperature 0.0, 0.2, dan 0.8, isi jawaban tetap sama. Model selalu menyebutkan algoritma KNN, tetapi tidak memberikan nilai akurasi dan metode penanganan data tidak seimbang karena informasinya tidak ditemukan di dokumen. Perbedaan hanya terlihat pada susunan kalimat dan panjang jawaban.

Menurut kalian nilai mana yang paling cocok untuk aplikasi RAG ini?

temperature 0.0

Kenapa?

Karena jawaban yang dihasilkan lebih konsisten dan langsung ke inti pertanyaan. Aplikasi RAG membutuhkan jawaban yang sesuai dengan isi dokumen, bukan jawaban yang bervariasi atau terlalu kreatif. Temperature 0.0 juga membantu mengurangi variasi jawaban ketika pengguna mengajukan pertanyaan yang sama.

------------------------------------------------------

# Experiment 2 - TOP_K

## TOP_K = 1

### Actual Output

1. Peneliti menggunakan algoritma **K‑Nearest Neighbors (KNN)** untuk memprediksi churn pelanggan pada perusahaan telekomunikasi【Source: 6639‑Article Text‑25282‑1‑10‑20230918.pdf, p. 1】. Persentase akurasi yang dilaporkan tidak terdapat dalam dokumen yang di‑upload.

2. Metode yang diterapkan untuk mengatasi data tidak seimbang (imbalancing data) sebelum pemodelan tidak disebutkan dalam konteks yang diberikan.

### Sources / Similarity Score

- 6639-Article Text-25282-1-10-20230918.pdf p. 1

### Observation

Jawaban sudah menjawab kedua pertanyaan, tetapi sumber yang digunakan hanya halaman 1. Informasi yang diberikan cukup singkat dan model tidak menambahkan penjelasan lain di luar isi dokumen.

------------------------------------------------------

## TOP_K = 4

### Actual Output

**1. Algoritma yang dipakai:** Peneliti menggunakan algoritma **K‑Nearest Neighbors (KNN)** untuk memprediksi churn pelanggan [Source: 6639‑Article Text‑25282‑1‑10‑20230918.pdf, p. 1‑2].

**Akurasi model:** Persentase akurasi hasil evaluasi model tidak tercantum dalam dokumen yang di‑upload, sehingga tidak dapat disampaikan.

**2. Penanganan data tidak seimbang:** Dokumen tidak menyebutkan metode apa pun (misalnya oversampling, SMOTE, atau teknik penyeimbangan lainnya) yang diterapkan untuk mengatasi masalah data tidak seimbang sebelum pemodelan. Oleh karena itu, informasi tersebut tidak ditemukan dalam sumber yang diberikan.

### Sources / Similarity Score

- 6639-Article Text-25282-1-10-20230918.pdf p. 1
- 6639-Article Text-25282-1-10-20230918.pdf p. 2

### Observation

Jawaban masih sama dengan TOP_K = 1, tetapi penjelasan tentang metode penanganan data tidak seimbang lebih detail. Sumber yang digunakan mencakup halaman 1 dan 2, tetapi belum ada informasi baru mengenai akurasi atau metode yang dipakai peneliti.

------------------------------------------------------

## TOP_K = 8

### Actual Output

**1. Algoritma yang dipakai**  
Peneliti menggunakan algoritma **K‑Nearest Neighbors (K‑NN)** untuk memprediksi apakah pelanggan akan churn atau tidak 【Source: 6639-Article Text-25282-1-10-20230918.pdf | Page: 1‑2】.  

**Persentase akurasi** – Dokumen yang diberikan tidak mencantumkan nilai akurasi (atau metrik evaluasi lain) yang diperoleh dari model K‑NN.  

**2. Penanganan data tidak seimbang**  
Dalam teks yang tersedia tidak ada penjelasan mengenai teknik khusus (mis. oversampling, SMOTE, undersampling, atau penyesuaian bobot) yang diterapkan untuk mengatasi masalah data tidak seimbang sebelum pemodelan.  

*Jawaban: algoritma K‑NN digunakan, tetapi nilai akurasi serta metode penanganan data tidak seimbang tidak ditemukan dalam dokumen yang di‑upload.*

### Sources / Similarity Score

- 6639-Article Text-25282-1-10-20230918.pdf p. 1
- 6639-Article Text-25282-1-10-20230918.pdf p. 2
- 6639-Article Text-25282-1-10-20230918.pdf p. 9
- 6639-Article Text-25282-1-10-20230918.pdf p. 3

### Observation

Jawaban tetap memberikan informasi yang sama seperti dua percobaan sebelumnya. Sumber yang ditemukan bertambah menjadi empat halaman, yaitu halaman 1, 2, 9, dan 3. Namun, tambahan sumber tersebut belum menghasilkan informasi baru yang bisa menjawab bagian akurasi dan metode penanganan data tidak seimbang.

------------------------------------------------------

## Kesimpulan Experiment TOP_K

Apakah TOP_K yang lebih besar selalu menghasilkan jawaban yang lebih baik?

TOP_K yang lebih besar menambah jumlah sumber yang diambil, tetapi isi jawaban tetap sama. Penambahan context belum tentu membuat jawaban lebih lengkap kalau informasi yang dibutuhkan memang tidak ditemukan di dokumen

Menurut kalian TOP_K mana yang paling cocok untuk PDF yang digunakan?

TOP_K = 4, karena sudah cukup mengambil informasi yang relevan dan cukup detail

Kenapa?

arena jawaban yang dihasilkan sudah cukup untuk menjawab pertanyaan, dengan sumber dari dua halaman dokumen. TOP_K = 1 memang lebih singkat, sedangkan TOP_K = 8 mengambil lebih banyak sumber tanpa memberikan informasi tambahan. 

------------------------------------------------------

# Experiment 3 - Chunk Size

Gunakan:

```text
CHUNK_OVERLAP = 20
```

untuk seluruh percobaan.

------------------------------------------------------

## Chunk Size = 50

### Chunks Stored

202 chunks

### Actual Output

**1. Algoritma yang digunakan:** Peneliti menerapkan algoritma **K‑Nearest Neighbors (K‑NN)** untuk membangun model prediksi churn pelanggan pada perusahaan telekomunikasi【Source: 6639-Article Text-25282-1-10-20230918.pdf | Page: 2】.  

**Akurasi model:** Persentase akurasi yang diperoleh dari evaluasi model tidak tercantum dalam dokumen yang diunggah, sehingga tidak dapat disampaikan.

**2. Penanganan data tidak seimbang:** Dokumen yang disediakan tidak menyebutkan metode apa pun yang digunakan peneliti untuk mengatasi masalah data tidak seimbang (imbalancing data) sebelum pemodelan.  

*Jawaban didasarkan pada informasi yang tersedia dalam dokumen; detail yang tidak ada tidak dapat disimpulkan.*

### Sources / Similarity Score

- 6639-Article Text-25282-1-10-20230918.pdf p. 1
- 6639-Article Text-25282-1-10-20230918.pdf p. 2
- 6639-Article Text-25282-1-10-20230918.pdf p. 3

### Observation

Dengan chunk size 50, jumlah chunk yang tersimpan mencapai 202. Jawaban berhasil menyebutkan algoritma KNN, tetapi informasi akurasi dan metode penanganan data tidak seimbang belum ditemukan. Source yang diambil mencakup halaman 1, 2, dan 3.

------------------------------------------------------

## Chunk Size = 100

### Chunks Stored

88 Chunks

### Actual Output

**1. Algoritma yang dipakai:** Peneliti menggunakan algoritma **K‑nearest neighbors (KNN)** untuk memprediksi churn pelanggan pada perusahaan telekomunikasi【Source: 6639-Article Text-25282-1-10-20230918.pdf | Page: 1】【Source: 6639-Article Text-25282-1-10-20230918.pdf | Page: 2】.  

**Persentase akurasi:** Tidak terdapat informasi mengenai nilai akurasi yang diperoleh dari evaluasi model dalam dokumen yang diunggah.  

**2. Penanganan data tidak seimbang:** Dokumen tidak menyebutkan metode apa pun yang diterapkan untuk mengatasi masalah data tidak seimbang (imbalancing data) sebelum pemodelan.  

*Jawaban di atas didasarkan pada konten yang tersedia; bila ada bagian lain dari dokumen yang memuat detail tersebut, informasi tersebut tidak ditemukan dalam cuplikan yang diberikan.*

### Sources / Similarity Score

- 6639-Article Text-25282-1-10-20230918.pdf p. 1
- 6639-Article Text-25282-1-10-20230918.pdf p. 2

### Observation

Jumlah chunk yang tersimpan turun menjadi 88. Jawaban masih sama seperti percobaan sebelumnya, yaitu menyebutkan KNN tanpa memberikan nilai akurasi dan metode penanganan data tidak seimbang. Source yang ditemukan hanya halaman 1 dan 2.

------------------------------------------------------

## Chunk Size = 120

### Chunks Stored

68 chunks

### Actual Output

**1. Algoritma yang dipakai:** Peneliti menggunakan algoritma **K‑Nearest Neighbors (KNN)** untuk memprediksi churn pelanggan pada perusahaan telekomunikasi.  
**Akurasi model:** Evaluasi menghasilkan **akurasi ≈ 81 %**【Source: 6639-Article Text-25282-1-10-20230918.pdf | Page 1】.

**2. Penanganan data tidak seimbang:** Dalam dokumen yang diberikan tidak ada penjelasan mengenai metode yang diterapkan untuk mengatasi masalah data tidak seimbang sebelum pemodelan. Jadi, informasi tersebut **tidak ditemukan** dalam sumber yang di‑upload.

### Sources / Similarity Score

- 6639-Article Text-25282-1-10-20230918.pdf p. 1
- 6639-Article Text-25282-1-10-20230918.pdf p. 2
- 6639-Article Text-25282-1-10-20230918.pdf p. 9

### Observation

Jumlah chunk yang tersimpan turun lagi menjadi 68. Model berhasil memberikan informasi akurasi sekitar 81% dari halaman 1, sementara metode penanganan data tidak seimbang tetap tidak ditemukan. Hasil ini menunjukkan bahwa ukuran chunk memengaruhi informasi yang berhasil ditemukan.

------------------------------------------------------

## Kesimpulan Experiment Chunk Size

Apa hubungan Chunk Size dengan jumlah chunk yang tersimpan?

Semakin besar chunk size, semakin sedikit jumlah chunk yang tersimpan. Pada pengujian ini, chunk size 50 menghasilkan 202 chunk, chunk size 100 menghasilkan 88 chunk, dan chunk size 120 menghasilkan 68 chunk.

Apakah chunk yang lebih kecil selalu menghasilkan retrieval yang lebih baik?

Tidak selalu. Chunk yang lebih kecil memang bisa mengambil informasi yang lebih spesifik, tetapi konteksnya bisa terpotong. Dari hasil pengujian, chunk size 50 dan 100 belum menghasilkan informasi akurasi, sedangkan chunk size 120 berhasil menemukannya.

Menurut kalian Chunk Size mana yang paling cocok?

chunk size 120

Kenapa?

Karena pada chunk size 120, model berhasil menemukan informasi akurasi sekitar 81% yang tidak muncul pada dua percobaan sebelumnya. Jumlah chunk yang tersimpan juga lebih sedikit, yaitu 68 chunk. Namun, hasil ini berlaku untuk pengujian yang dilakukan saja dan belum membuktikan bahwa chunk size 120 selalu lebih baik untuk dokumen lain.

------------------------------------------------------

# Experiment 4 - Chunk Overlap

Gunakan:

```text
CHUNK_SIZE = 100
```

untuk seluruh percobaan.

------------------------------------------------------

## Chunk Overlap = 0

### Chunks Stored

81 chunks

### Actual Output

**1. Algoritma yang dipakai:** Peneliti menggunakan algoritma **K‑Nearest Neighbors (K‑NN)** untuk memprediksi churn pelanggan pada perusahaan telekomunikasi【Source: 6639-Article Text-25282-1-10-20230918.pdf | Page: 1】【Source: 6639-Article Text-25282-1-10-20230918.pdf | Page: 2】.  

**Persentase akurasi:** Tidak terdapat informasi mengenai nilai akurasi yang diperoleh dari evaluasi model dalam dokumen yang diunggah.

**2. Penanganan data tidak seimbang:** Dokumen tidak menyebutkan metode apa pun yang diterapkan untuk mengatasi masalah data tidak seimbang (imbalancing data) sebelum pemodelan.

### Sources / Similarity Score

- 6639-Article Text-25282-1-10-20230918.pdf p. 1
- 6639-Article Text-25282-1-10-20230918.pdf p. 2
- 6639-Article Text-25282-1-10-20230918.pdf p. 9

### Observation

Jawaban menyebutkan algoritma KNN, tetapi informasi akurasi dan metode penanganan data tidak seimbang tidak ditemukan. Jumlah chunk yang tersimpan sebanyak 81. Source yang ditemukan mencakup halaman 1, 2, dan 9.

------------------------------------------------------

## Chunk Overlap = 20

### Chunks Stored

88 chunks

### Actual Output

**1. Algoritma yang dipakai:** Peneliti menggunakan algoritma **K‑nearest neighbors (KNN)** untuk memprediksi churn pelanggan pada perusahaan telekomunikasi【Source: 6639-Article Text-25282-1-10-20230918.pdf | Page: 1】【Source: 6639-Article Text-25282-1-10-20230918.pdf | Page: 2】.  

**Akurasi model:** Persentase akurasi hasil evaluasi model tidak tercantum dalam dokumen yang diunggah.  

**2. Penanganan data tidak seimbang:** Dokumen tidak menyebutkan metode apa pun yang diterapkan untuk mengatasi masalah data tidak seimbang (imbalancing data) sebelum pemodelan.  

### Sources / Similarity Score

- 6639-Article Text-25282-1-10-20230918.pdf p. 1
- 6639-Article Text-25282-1-10-20230918.pdf p. 2

### Observation

Jumlah chunk bertambah menjadi 88. Jawabannya masih sama seperti overlap 0, tetapi source yang ditemukan hanya halaman 1 dan 2. Penambahan overlap belum membuat model menemukan informasi akurasi atau metode penanganan data tidak seimbang.

------------------------------------------------------

## Chunk Overlap = 40

### Chunks Stored

183 chunks

### Actual Output

**1. Algoritma yang dipakai:** Peneliti menggunakan algoritma **K‑nearest neighbors (KNN)** untuk memprediksi churn pelanggan [Source: 6639‑Article Text‑25282‑1‑10‑20230918.pdf, p. 1].

**Akurasi model:** Persentase akurasi hasil evaluasi model tidak tercantum dalam dokumen yang di‑upload, sehingga tidak dapat disampaikan.

**2. Penanganan data tidak seimbang:** Dokumen tidak menyebutkan metode apa pun yang diterapkan untuk mengatasi masalah imbalancing data sebelum pemodelan.

### Sources / Similarity Score

- 6639-Article Text-25282-1-10-20230918.pdf p. 1
- 6639-Article Text-25282-1-10-20230918.pdf p. 2

### Observation

Jumlah chunk meningkat cukup banyak menjadi 183. Jawaban tetap menyebutkan KNN, sedangkan informasi akurasi dan metode penanganan data tidak seimbang masih belum ditemukan. Source yang digunakan juga hanya halaman 1 dan 2, jadi penambahan jumlah chunk belum memberikan informasi baru pada jawaban.

------------------------------------------------------

## Kesimpulan Experiment Chunk Overlap

Apa pengaruh Chunk Overlap yang kalian lihat?

Semakin besar nilai overlap, semakin banyak chunk yang tersimpan. Pada percobaan ini, jumlahnya meningkat dari 81 chunk pada overlap 0 menjadi 88 pada overlap 20, lalu 183 pada overlap 40. Tapi isi jawaban yang dihasilkan masih hampir sama.

Apakah overlap yang lebih besar selalu menghasilkan jawaban yang lebih baik?

Overlap yang besar memang bisa menjaga konteks antar-potongan teks, tapi juga membuat lebih banyak teks berulang. Terlihat overlap 40 menghasilkan chunk paling banyak, tapi belum memberikan informasi tambahan pada jawaban.

Menurut kalian nilai mana yang paling cocok?

Overlap 20

------------------------------------------------------

# Final Configuration

Setelah seluruh eksperimen, pilih konfigurasi yang menurut kalian menghasilkan hasil terbaik untuk PDF yang digunakan.

```text
Temperature: 0.0
TOP_K: 4
Chunk Size: 128
Chunk Overlap: 40
```


------------------------------------------------------

# Final Questions

### 1. Parameter mana yang paling terasa memengaruhi hasil aplikasi kalian?

Chunk Size.

### 2. Apakah Temperature memengaruhi Retrieval atau Generation? Jelaskan.

Temperature mempengaruh bagaimana llm menghasilkan jawaban (Generation). Dari eksperimen yang sudah dilakukan dapat terlihat jawaban dan cara penyampaian sedikit berbeda tapi tidak mempengaruhi detail informasi yang disampaikan dan sumber yang digunakan (Retrieval).

### 3. Apakah TOP_K yang lebih besar selalu menghasilkan jawaban yang lebih baik?

Tidak juga, Hasil eksperimen TOP_K 1, 4, dan 8 menghasilkan jawaban yang hampir sama. TOP_K yang lebih besar memang mengambil lebih banyak context, tetapi kalau informasi tambahannya kurang relevan, jawaban belum tentu menjadi lebih baik

### 4. Apa yang terjadi ketika Chunk Size dibuat lebih kecil?

Jumlah chunk yang dihasilkan menjadi lebih banyak. Chunk size 50 menghasilkan 202 chunk, ukuran 100 menghasilkan 88 chunk, dan ukuran 120 menghasilkan 68 chunk. Chunk yang lebih kecil bisa memberikan informasi yang lebih spesifik, tetapi konteksnya juga bisa terpotong.

### 5. Setelah melakukan eksperimen, apa fungsi Chunk Overlap menurut pemahaman kalian?

Fungsi Chunk Overlap adalah untuk menjaga konteks antar-potongan teks. Terlihat overlap 40 menghasilkan chunk paling banyak, tapi belum memberikan informasi tambahan pada jawaban.

### 6. Kenapa perubahan Chunk Size dan Chunk Overlap membutuhkan ingestion ulang?

Karena perubahan Chunk Size dan Chunk Overlap mengubah cara dokumen diproses menjadi potongan-potongan teks (chunks) sebelum dibuat embedding dan disimpan di Qdrant. 

### 7. Kenapa perubahan Temperature tidak membutuhkan ingestion ulang?

Karena temperature digunakan saat LLM menghasilkan jawaban, bukan saat dokumen diproses dan disimpan.

### 8. Menurut kalian, apakah ada satu konfigurasi RAG yang akan selalu paling bagus untuk semua jenis dokumen?

Menurut saya, tidak ada satu konfigurasi yang selalu paling bagus untuk semua dokumen. Setiap dokumen punya struktur dan informasi yang berbeda. Jadi, parameter RAG perlu disesuaikan dengan dokumen yang digunakan dan diuji untuk mendapatkan hasil terbaik.

------------------------------------------------------

# Personal Reflection

### Bagian eksperimen mana yang hasilnya paling berbeda dari dugaan kalian?

Eksperimen Chunk Size memberikan hasil yang paling berbeda dari dugaan awal. Saat menggunakan chunk size 50 dan 100, model belum menemukan informasi akurasi. Saya kira chunk size 120 tidak akan memberikan informasi akurasi juga. Ternyata malah chunk size yang paling besar justru mendapatkan informasi tentang akurasi tersebut.

### Parameter mana yang awalnya kalian anggap tidak terlalu penting tetapi ternyata berpengaruh?

Saya awalnya menganggap TOP_K tidak terlalu penting karena dari eksperimen TOP_K 1, 4, dan 8 menghasilkan jawaban yang hampir sama. Ternyata TOP_K cukup penting karena mempengaruhi berapa banyak konteks yang diberikan kepada LLM.

### Setelah mengerjakan tugas ini, bagaimana kalian menjelaskan hubungan antara Retrieval dan Generation pada RAG?

Retrieval bertugas mencari informasi dari dokumen, sedangkan Generation menyusun informasi tersebut menjadi jawaban. Keduanya saling berhubungan karena jawaban LLM bergantung pada konteks yang ditemukan Retrieval.


### Jika aplikasi ini dikembangkan lebih lanjut, parameter atau bagian apa lagi yang ingin kalian coba?

Saya ingin mencoba dengan dokumen lain yang memiliki struktur berbeda dan pertanyaan yang mudah dijawab.

------------------------------------------------------

# AI Usage

### AI tools yang digunakan

Gemini.

### AI digunakan untuk membantu bagian apa?

Membantu analisis dan mencari alasan mengenai hasil eksperimen.

### Bagian eksperimen mana yang kalian lakukan dan evaluasi sendiri?

Semua bagian eksperimen saya kerjakan sendiri.