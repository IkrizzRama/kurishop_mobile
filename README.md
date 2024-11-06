README TUGAS 7 
1. Jelaskan apa yang dimaksud dengan stateless widget dan stateful widget, dan jelaskan perbedaan dari keduanya.
2. Sebutkan widget apa saja yang kamu gunakan pada proyek ini dan jelaskan fungsinya.
3. Apa fungsi dari setState()? Jelaskan variabel apa saja yang dapat terdampak dengan fungsi tersebut.
4. Jelaskan perbedaan antara const dengan final.
5. Jelaskan bagaimana cara kamu mengimplementasikan checklist-checklist di atas.

Jawab:
1. - Widget Stateful adalah yang mengubah propertinya selama run-time. Mereka dinamis yaitu, mereka dapat berubah dan dapat ditarik beberapa kali dalam masa pakainya. Ini dapat mengubah tampilannya sebagai respons terhadap peristiwa yang dipicu oleh interaksi pengguna atau saat menerima data.
- Widget stateless adalah widget yang tidak berubah yaitu tidak dapat diubah. Penampilan dan propertinya tetap tidak berubah sepanjang masa pakai widget. Dengan kata sederhana, widget Stateless tidak dapat mengubah statusnya selama runtime aplikasi, yang berarti widget tidak dapat digambar ulang saat aplikasi sedang beraksi.

2. Widget yang Digunakan:
Scaffold: Menyediakan struktur dasar untuk material design visual layout. Ini mencakup AppBar, body, dan Snackbar.

AppBar: Bagian atas aplikasi yang biasanya berisi judul, tombol navigasi, atau tindakan lain yang relevan.

Column: Menyusun widget dalam satu kolom vertikal.

ElevatedButton: Membuat tombol yang dapat ditekan dengan gaya elevasi (terangkat) yang dapat mencakup ikon dan teks.

Icon: Menampilkan ikon dari Material Icons atau ikon kustom lainnya.

Text: Menampilkan teks dalam aplikasi.

Snackbar: Menampilkan pesan sementara di bagian bawah layar untuk memberikan informasi kepada pengguna.

Padding: Menambahkan ruang di sekitar widget lainnya.


3. Fungsi setState() digunakan untuk memperbarui status (state) pada komponen React. Ini sangat penting dalam siklus hidup komponen React karena memungkinkan antarmuka pengguna (UI) untuk diperbarui secara dinamis sesuai dengan perubahan data. Dengan kata lain, setState() memungkinkan komponen untuk merender ulang dirinya sendiri ketika data internalnya berubah.

Variabel yang dapat terdampak oleh fungsi setState() adalah:
State Variabel: Variabel-variabel yang ditentukan dalam state dari suatu komponen React. Ketika setState() dipanggil, React menggabungkan perubahan dengan status yang ada dan kemudian merender ulang komponen untuk mencerminkan perubahan tersebut.

Props: Meskipun setState() tidak mengubah props secara langsung (karena props adalah nilai-nilai yang diturunkan dari komponen induk dan bersifat read-only), perubahan pada state dapat menyebabkan perubahan pada cara komponen menangani atau menampilkan props.

4. const
Konstanta Waktu Kompilasi: Variabel atau objek yang dideklarasikan dengan const adalah konstanta pada waktu kompilasi. Artinya, nilai dari const harus sudah diketahui pada saat kompilasi.
Immutability: Objek yang dibuat dengan const tidak dapat diubah. Baik referensi maupun isi dari objek tersebut tetap konstan.


final
Inisialisasi Sekali: Variabel atau objek yang dideklarasikan dengan final hanya dapat diinisialisasi sekali. Setelah itu, nilainya tidak dapat diubah.
Mutable Content: Sementara referensi ke objek final tidak dapat diubah, isi dari objek tersebut dapat diubah jika objeknya bukan konstanta.

5. Membuat sebuah program flutter:
Pada awalnya saya hanya mengikuti tutorial untuk membuat flutternya yakni dengan flutter create dan nama program saya yakni kurishop

Membuat tiga tombol sederhana dengan ikon dan teks untuk melihat daftar produk, menambah produk, dan logout:
Untuk ketiga tombol ini saya membuatnya pada menu.dart tepatnya di class homepage dengan membuat masing2 tombolnya mulai dari lihat daftar produk, tambah produk, dan logout.

Mengimplementasikan warna-warna yang berbeda untuk setiap tombol:
Untuk pewarnaan saya harus menambahkan satu variable baru di menu.dart yakni Color untuk pada akhirnya saya menambahkan warna yang berbeda untuk masing2 tombol yang telah saya buat pada poin sebelumnya.

Memunculkan snackbar dengan tulisan:
Untuk masing2 tulisan disini saya implementasikan dalam scaffoldnya agar nanti akan muncul tulisan sesuai dengan tombol yang ditekan oleh user yang mengakses program ini.
