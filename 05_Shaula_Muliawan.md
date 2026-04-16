1. Console (Konsol JavaScript)
P (Point):
Console adalah panel khusus di peramban modern yang bertindak sebagai "panggung belakang" bagi kode JavaScript. Ia tidak terlihat oleh pengunjung biasa, tetapi menjadi jendela utama bagi pengembang untuk memantau apa yang sebenarnya terjadi di balik layar halaman web.
R (Reason):
Ketika sebuah program web berjalan, banyak proses internal terjadi secara diam-diam: penyimpanan sementara, perhitungan logika, hingga pengiriman data. Jika terjadi kesalahan, halaman tidak akan berteriak kepada pengguna. Console hadir sebagai alat pencatat otomatis. Ia bisa menerima perintah dari kode kita untuk menuliskan informasi, seperti buku harian digital. Dengan console, kita bisa melihat nilai suatu variabel pada waktu tertentu, mengetahui urutan eksekusi fungsi, atau mendeteksi di mana letak kesalahan sintaks maupun logika.

E (Example):
Misalnya, Anda membuat fitur kalkulator diskon. Saat pengguna memasukkan harga asli dan persen diskon, Anda bisa menyisipkan perintah console.log("Harga setelah diskon: Rp" + hasil) di dalam kode. Hasilnya tidak tampil di layar, tetapi bisa dibaca di Console. Jika tiba-tiba hasilnya minus, Console akan menampilkan galat atau nilai aneh yang membantu Anda melacak bahwa ada kesalahan rumus di baris ke-12.

P (Point):
Singkatnya, Console adalah sahabat setia debugging. Tanpanya, mencari sumber error di JavaScript seperti mencari jarum dalam tumpukan jerami tanpa senter.

2. DOM (Document Object Model) dan Vanilla JavaScript
P (Point):
DOM adalah representasi pohon dari halaman HTML yang dibuat oleh browser di memori. Vanilla JavaScript adalah bahasa murni tanpa pustaka tambahan yang digunakan untuk mengakses dan memanipulasi pohon tersebut secara langsung.

R (Reason):
Browser tidak menampilkan file HTML begitu saja. Ia membaca baris per baris, lalu membangun model objek terstruktur di mana setiap tag, atribut, dan teks menjadi sebuah simpul (node). Dengan Vanilla JavaScript, kita bisa menelusuri pohon itu, mengubah isi simpul, menambah atau menghapus cabang, tanpa perlu memuat ulang halaman. Inilah inti dari halaman web dinamis: konten berubah berdasarkan aksi pengguna, bukan berdasarkan permintaan baru ke server.

E (Example):
Bayangkan sebuah daftar belanja online. Di dalam DOM, setiap item adalah simpul <li>. Saat pengguna mengeklik tombol "Beli", Vanilla JavaScript dapat langsung menemukan simpul item tersebut, mengubah teksnya menjadi "Sudah dibeli", serta mengubah warna latarnya menjadi hijau. Semua ini terjadi dalam sekejap karena JavaScript bekerja pada salinan DOM di memori, bukan pada file HTML asli di server.

P (Point):
Jadi, DOM yang dikendalikan Vanilla JavaScript adalah fondasi interaktivitas web modern. Tanpa ini, setiap perubahan kecil akan membutuhkan penyegaran halaman total.

3. ID, Class, Tag, dan DOM Selector (Down Selection)
P (Point):
Dalam dokumen HTML, ID, Class, dan Tag berfungsi sebagai tanda pengenal. Sementara DOM Selector adalah metode di JavaScript untuk mencari dan memilih elemen berdasarkan tanda-tanda tersebut, dalam proses yang disebut down selection (pemilihan ke bawah dari akar pohon DOM).

R (Reason):
Agar JavaScript bisa mengubah suatu elemen, ia harus tahu persis elemen mana yang dituju. Ketiga pengenal ini memiliki karakteristik berbeda:
ID bersifat unik dalam satu halaman. Cocok untuk elemen yang hanya muncul sekali, seperti formulir login utama.
Class bisa dipakai banyak elemen sekaligus. Berguna untuk kelompok, misalnya semua tombol dengan gaya yang sama.
Tag merujuk pada jenis elemen seperti <div> atau <p>. Biasanya digunakan ketika kita ingin memilih semua elemen sejenis tanpa perlu memberi class.
DOM Selector seperti getElementById, querySelector, atau getElementsByClassName bekerja dengan cara menyusuri pohon DOM dari atas ke bawah, lalu mengembalikan referensi elemen yang cocok.

E (Example):
Misalkan halaman memiliki tiga tombol dengan class .btn-hapus dan satu tombol dengan ID #btn-simpan.
Dengan document.querySelectorAll('.btn-hapus'), JavaScript akan mendapatkan ketiga tombol hapus.
Dengan document.getElementById('btn-simpan'), ia langsung menunjuk ke tombol simpan tanpa perlu repot mencari.
Sedangkan document.getElementsByTagName('button') akan mengembalikan keempat tombol sekaligus.

P (Point):
Kesimpulannya, memilih pengenal yang tepat dan menggunakan DOM Selector yang sesuai adalah langkah awal yang wajib dikuasai agar JavaScript bisa "bercakap-cakap" dengan elemen halaman.

4. Event Listening (Pendengar Peristiwa)
P (Point):
Event listening adalah mekanisme di JavaScript yang memungkinkan suatu elemen DOM "mendengarkan" aksi tertentu dari pengguna (klik, ketik, gerakan mouse) dan menjalankan fungsi sebagai reaksinya.

R (Reason):
Tanpa event listener, kode JavaScript hanya akan dieksekusi sekali saat halaman dimuat, lalu selesai. Agar halaman bisa merespons interaksi seperti sentuhan tombol atau isian formulir, kita perlu memasang "penjaga" yang siaga. Penjaga ini akan memicu fungsi yang sudah disiapkan setiap kali aksi terjadi. Dengan kata lain, event listening mengubah halaman statis menjadi aplikasi yang hidup dan responsif.

E (Example):
Coba bayangkan sebuah galeri foto. Anda ingin ketika pengguna mengarahkan kursor ke thumbnail, foto besar muncul di samping. Kodenya:
Pilih elemen thumbnail dengan querySelector.
Pasang event listener mouseenter padanya.
Di dalam fungsi yang dipanggil, ubah sumber gambar besar sesuai thumbnail yang diarahi.
Saat kursor keluar, event mouseleave akan mengembalikan gambar besar ke default. Ini semua terjadi tanpa perlu tombol refresh.

P (Point):
Event listening adalah denyut nadi interaktivitas web. Ia menghubungkan kehendak pengguna (dalam bentuk peristiwa) dengan logika program (dalam bentuk fungsi).

5. Data Attribute dan Data Mining
P (Point):
Data attribute adalah atribut HTML khusus dengan awalan data- yang menyimpan informasi tersembunyi pada suatu elemen. Data mining di sini berarti proses membaca nilai atribut tersebut menggunakan JavaScript untuk keperluan logika aplikasi.

R (Reason):
Terkadang, sebuah elemen perlu membawa "kartu identitas" atau metadata yang tidak perlu dilihat pengguna, misalnya ID produk dari database, batas stok, atau status khusus. Menyimpannya di atribut data-* lebih rapi dan aman daripada menaruhnya di dalam teks atau variabel global yang bisa kacau. JavaScript dapat menggali (mine) nilai ini kapan saja, lalu mengambil keputusan berdasarkan data yang diperoleh.

E (Example):
Bayangkan sebuah daftar film dengan tombol "Tonton". Setiap kartu film menyimpan data-id="123" dan data-umur="17". Saat pengguna mengeklik tombol, JavaScript melakukan data mining: membaca data-umur. Jika umur minimum 17 tetapi profil pengguna baru berusia 15, aplikasi akan memunculkan peringatan "Konten tidak cocok" tanpa perlu memeriksa database. Jika cocok, ia mengambil data-id untuk memutar film yang tepat.

P (Point):
Dengan data attribute dan kemampuan mining-nya, elemen HTML menjadi lebih pintar. Mereka bisa membawa konteks sendiri, sehingga JavaScript tidak perlu lagi menyimpan semua data secara terpisah di luar DOM. Ini membuat kode lebih terstruktur dan mudah dipelihara.
