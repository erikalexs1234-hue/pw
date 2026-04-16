### **1. Point (Titik Utama)**
Isi papan tulis tersebut adalah **Modul Pembelajaran DOM & JS Vanilla (Native)** yang disusun oleh **OS-Widya MD**. Fokus utamanya adalah membedah bagaimana JavaScript murni bekerja sebagai pengendali utama (*Logic*) untuk memanipulasi elemen-elemen di halaman web sehingga tercipta interaktivitas antara pengguna dan sistem.

### **2. Reason (Alasan)**
Alasan mengapa materi ini dipaparkan secara terbagi-bagi adalah untuk menjelaskan bahwa pembuatan website interaktif harus memiliki pondasi yang kuat pada tiga pilar utama:
* **HTML:** Sebagai struktur atau "Berkat" (kerangka dasar).
* **CSS:** Sebagai "Tampilan" atau "Template" (estetika).
* **JavaScript (JS):** Sebagai "Otak" (logika yang memerintah).
Tanpa memahami cara kerja JavaScript secara murni (*Native*), seorang pengembang akan kesulitan memahami bagaimana data mengalir dari layar pengguna menuju sistem, terutama saat ingin membangun fungsi dinamis tanpa bergantung pada alat bantu pihak ketiga (*Framework*).



### **3. Example (Penjelasan Rinci Seluruh Poin Papan Tulis)**

Papan tulis tersebut membagi proses teknis menjadi tiga kolom utama yang saling berurutan:

**Kolom 1: DOM Selector (Proses Pemilihan)**
Ini adalah tahap pertama di mana JavaScript harus mengenali atau "memegang" elemen yang ada di halaman web.
* **Metode Spesifik:** Menggunakan perintah untuk mencari identitas tunggal yang unik pada sebuah elemen.
* **Optimasi (Metode Fleksibel):** Di papan tulis dijelaskan optimasi menggunakan cara yang lebih modern (*Query Selection*). Cara ini lebih hebat karena bisa mencari target berdasarkan:
    * **Class:** Mencari elemen berdasarkan kategori kelompoknya.
    * **Id:** Mencari elemen yang memiliki nama identitas unik.
    * **Elemen/Component/Tag:** Mencari berdasarkan jenis tag aslinya (seperti judul, kotak input, atau tombol).

**Kolom 2: Event Listener (Pendeteksi Aksi)**
Setelah target dipilih, langkah selanjutnya adalah menentukan kapan perintah harus dijalankan. Ini dilakukan dengan mendengarkan aktivitas pengguna.
* **Fungsi Bawaan:** Menggunakan fungsi yang akan berjalan secara otomatis saat ada pemicu (*Callback*).
* **Jenis-jenis Pemicu (Event):**
    * `Onclick`: Perintah berjalan saat pengguna **menekan/mengklik** elemen.
    * `Onchange`: Perintah berjalan saat pengguna **mengubah** isi atau nilai elemen (misal memilih opsi lain).
    * `Onfocus`: Perintah berjalan saat elemen tersebut **sedang disorot atau aktif** (misal kursor masuk ke kolom ketikan).

**Kolom 3: Data Mining & Execution (Pengambilan Data & Hasil)**
Ini adalah tahap akhir di mana logika dieksekusi berdasarkan input pengguna.
* **Input User:** Di papan tulis dicontohkan jika pengguna memasukkan kata "Hi" pada sebuah kolom.
* **Data Mining (Value):** Sistem akan menggali atau menarik "Nilai" (Value) dari input tersebut untuk diproses.
* **Function (Hasil):** Setelah data didapat, sistem akan memberikan respon berupa:
    * `Alert`: Memunculkan pesan pop-up di layar untuk memberikan informasi ke pengguna.
    * `Console`: Mengirim data ke catatan teknis di dalam browser untuk diperiksa oleh pengembang (berguna untuk melihat apakah data sudah benar).



### **4. Point (Kesimpulan Akhir)**
Seluruh poin di papan tulis ini menegaskan bahwa untuk membangun interaktivitas yang lengkap, kita harus mengikuti urutan: **Menentukan target mana yang akan diatur (Selector) $\rightarrow$ Menentukan tindakan apa yang ditunggu (Event) $\rightarrow$ Mengambil informasi yang masuk (Data Mining) $\rightarrow$ Menampilkan hasil akhirnya (Output).** Ini adalah standar operasional untuk membuat fitur-fitur pada website profesional agar dapat berfungsi dengan tepat dan optimal.
