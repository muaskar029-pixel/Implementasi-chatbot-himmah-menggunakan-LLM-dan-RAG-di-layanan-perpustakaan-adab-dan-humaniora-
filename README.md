# Himmah: Chatbot Referensi Perpustakaan FAH Berbasis LLM dan RAG

**Himmah** adalah prototipe chatbot referensi digital yang dikembangkan untuk mendukung layanan informasi di Perpustakaan Fakultas Adab dan Humaniora UIN Syarif Hidayatullah Jakarta. Chatbot ini menggunakan pendekatan **Large Language Model (LLM) open-source** dan **Retrieval-Augmented Generation (RAG)** agar jawaban yang diberikan dapat terhubung dengan sumber data lokal perpustakaan.

Proyek ini dikembangkan sebagai bagian dari penelitian berjudul:

**Implementasi Prototipe Chatbot LLM Open-Source Berbasis RAG dalam Mendukung Layanan Referensi Perpustakaan FAH**

## Deskripsi Singkat

Himmah dirancang sebagai asisten awal layanan referensi perpustakaan. Sistem ini dapat membantu pengguna dalam:

* Mencari informasi koleksi buku.
* Menampilkan informasi bibliografis seperti judul, pengarang, tahun terbit, penerbit, ISBN, dan tautan OPAC.
* Memberikan arahan awal dalam proses penelusuran informasi.
* Mengarahkan pengguna kepada sumber resmi atau pustakawan apabila pertanyaan tidak dapat dijawab secara memadai.

Chatbot ini tidak dimaksudkan untuk menggantikan pustakawan, tetapi sebagai alat bantu untuk memperluas akses awal terhadap layanan referensi digital.

## Teknologi yang Digunakan

* **LLM:** Qwen melalui Ollama
* **Metode:** Retrieval-Augmented Generation (RAG)
* **Backend:** FastAPI
* **Database/Retriever:** ChromaDB / pencarian berbasis data lokal
* **Frontend:** Web chatbot
* **Sumber Data:** OPAC FAH, Repository FAH, Jurnal Insaniyat, dan sumber lokal perpustakaan lain

## Arsitektur Sistem

Alur kerja sistem Himmah secara umum adalah sebagai berikut:

```text
User → Chatbot Web → Backend → Retriever/RAG → Database Koleksi → LLM Qwen → Jawaban
```

Penjelasan alur:

1. Pengguna mengajukan pertanyaan melalui antarmuka chatbot.
2. Pertanyaan dikirim ke backend.
3. Backend meneruskan pertanyaan ke sistem Retriever/RAG.
4. Retriever mencari data yang relevan dari database koleksi.
5. Data yang ditemukan digunakan sebagai konteks oleh LLM Qwen.
6. Chatbot menghasilkan jawaban yang lebih kontekstual berdasarkan sumber data lokal.

## Cara Menggunakan Chatbot Himmah

### 1. Masuk ke link chatbot

Buka link chatbot Himmah yang telah diberikan oleh pengembang atau peneliti.

```text
Masukkan link chatbot Himmah di sini
```

### 2. Masukkan pertanyaan

Ketik pertanyaan pada kolom chat. Contoh pertanyaan yang dapat diajukan:

```text
buku tentang psikologi sastra
```

```text
bagaimana cara mencari buku di OPAC FAH?
```

```text
saya mencari artikel tentang sejarah Islam
```

Tampilan chatbot Himmah:

![Tampilan Chatbot Himmah](https://raw.githubusercontent.com/muaskar029-pixel/Implementasi-chatbot-himmah-menggunakan-LLM-dan-RAG-di-layanan-perpustakaan-adab-dan-humaniora-/main/Screenshot_20260618_110249_com.android.chrome.jpg)

### 3. Lihat sumber jawaban

Setelah chatbot memberikan jawaban, pengguna dapat membuka bagian sumber untuk melihat data atau referensi yang digunakan oleh sistem.

Klik bagian sumber untuk melihat informasi lebih lanjut:

![Tampilan Sumber Chatbot Himmah](https://raw.githubusercontent.com/muaskar029-pixel/Implementasi-chatbot-himmah-menggunakan-LLM-dan-RAG-di-layanan-perpustakaan-adab-dan-humaniora-/main/Screenshot_20260618_110619_com.android.chrome_edit_505934460033419.jpg)

## Contoh Pertanyaan

Beberapa contoh pertanyaan yang dapat digunakan untuk menguji Himmah:

```text
buku tentang psikologi sastra
```

```text
buku tentang sejarah Islam
```

```text
cara mencari buku berdasarkan pengarang
```

```text
bagaimana cara menemukan artikel jurnal?
```

```text
apa yang harus dilakukan jika buku tidak ditemukan?
```

```text
bagaimana cara menghubungi pustakawan?
```

## Sumber Data

Basis pengetahuan Himmah pada tahap awal terdiri atas:

1. **OPAC FAH**
   Digunakan untuk pencarian metadata koleksi buku.

2. **Repository FAH**
   Digunakan untuk menelusuri karya ilmiah atau dokumen akademik lokal.

3. **Jurnal Insaniyat**
   Digunakan sebagai sumber artikel ilmiah yang relevan dengan bidang adab, humaniora, bahasa, sastra, budaya, dan kajian Islam.

Untuk pengembangan berikutnya, basis data dapat diperluas dengan:

* Panduan layanan perpustakaan.
* FAQ layanan perpustakaan.
* SOP peminjaman dan pengembalian.
* Panduan penggunaan OPAC.
* Kontak pustakawan.
* Informasi sumber elektronik resmi.

## Fungsi Utama

Himmah dapat digunakan untuk:

* Membantu pencarian koleksi perpustakaan.
* Memberikan informasi bibliografis.
* Menampilkan tautan OPAC jika tersedia.
* Memberikan jawaban awal terhadap pertanyaan referensi sederhana.
* Mengarahkan pengguna kepada pustakawan untuk pertanyaan yang lebih kompleks.

## Batasan Sistem

Karena masih berupa prototipe eksperimental, Himmah memiliki beberapa keterbatasan:

* Jawaban bergantung pada kelengkapan database.
* Chatbot belum dapat menggantikan analisis pustakawan.
* Informasi yang tidak tersedia dalam basis data dapat menyebabkan jawaban kurang lengkap.
* Pertanyaan yang kompleks tetap perlu diarahkan kepada pustakawan.
* Data perlu diperbarui secara berkala agar jawaban tetap relevan.

## Evaluasi Chatbot

Evaluasi kualitas jawaban Himmah dapat dilakukan menggunakan lima aspek:

1. **Accuracy**
   Ketepatan jawaban dan ketiadaan informasi keliru.

2. **Groundedness**
   Keterikatan jawaban dengan sumber data lokal perpustakaan.

3. **Elicitation**
   Kemampuan chatbot meminta klarifikasi jika pertanyaan belum jelas.

4. **Completeness**
   Kelengkapan jawaban terhadap kebutuhan pengguna.

5. **Further Assistance**
   Kemampuan chatbot mengarahkan pengguna ke OPAC, pustakawan, panduan layanan, atau sumber bantuan lain.

## Status Proyek

Proyek ini masih berada pada tahap:

```text
Eksperimental / Prototipe Penelitian
```

Himmah dikembangkan untuk menguji kelayakan awal penerapan chatbot LLM open-source berbasis RAG dalam layanan referensi Perpustakaan FAH.

## Tujuan Penelitian

Penelitian ini bertujuan untuk:

* Mengimplementasikan prototipe chatbot referensi berbasis LLM open-source dan RAG.
* Menghubungkan chatbot dengan sumber data lokal perpustakaan.
* Mengevaluasi kualitas jawaban chatbot berdasarkan rubrik evaluasi.
* Menunjukkan potensi AI sebagai sistem pendukung layanan referensi perpustakaan akademik.

## Pengembang

**Muhammad Suyuthi Alkautsar**
Program Studi Ilmu Perpustakaan
Fakultas Adab dan Humaniora
UIN Syarif Hidayatullah Jakarta

## Catatan

Himmah adalah alat bantu layanan referensi digital. Untuk pertanyaan yang membutuhkan analisis akademik, konsultasi penelitian, atau informasi resmi yang belum tersedia di sistem, pengguna tetap disarankan untuk menghubungi pustakawan.
