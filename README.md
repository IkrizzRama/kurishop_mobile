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



Tugas 8:

1. Apa kegunaan const di Flutter? Jelaskan apa keuntungan ketika menggunakan const pada kode Flutter. Kapan sebaiknya kita menggunakan const, dan kapan sebaiknya tidak digunakan?
2. Jelaskan dan bandingkan penggunaan Column dan Row pada Flutter. Berikan contoh implementasi dari masing-masing layout widget ini!
3. Sebutkan apa saja elemen input yang kamu gunakan pada halaman form yang kamu buat pada tugas kali ini. Apakah terdapat elemen input Flutter lain yang tidak kamu gunakan pada tugas ini? Jelaskan!
4. Bagaimana cara kamu mengatur tema (theme) dalam aplikasi Flutter agar aplikasi yang dibuat konsisten? Apakah kamu mengimplementasikan tema pada aplikasi yang kamu buat?
5. Bagaimana cara kamu menangani navigasi dalam aplikasi dengan banyak halaman pada Flutter?

Jawab:
1. Dalam Flutter, const digunakan untuk menandai objek atau nilai sebagai konstan, yang berarti nilainya tidak akan pernah berubah sepanjang runtime aplikasi. const sangat berguna terutama dalam deklarasi widget yang sifatnya statis dan tidak berubah, seperti widget teks atau ikon. Berikut beberapa manfaat dan panduan penggunaannya dalam kode Flutter:

Keuntungan Menggunakan const
Optimasi Performa: Dengan mendeklarasikan widget sebagai const, Flutter dapat mendeteksi bahwa widget tersebut tidak perlu dibuat ulang setiap kali UI diperbarui. Hal ini membantu mengurangi penggunaan memori dan mempercepat rendering UI, karena objek const hanya dibuat satu kali dan digunakan kembali selama objek tersebut tidak diubah.

Pengurangan Rekonstruksi Widget: Saat UI diperbarui, widget const tidak akan dibangun ulang. Misalnya, jika Anda memiliki tampilan yang banyak menggunakan widget teks statis atau ikon, maka menggunakan const dapat membantu Flutter memahami bahwa widget tersebut tidak perlu dibuat ulang, menghemat waktu komputasi.

Pengembangan Lebih Rapi: Menggunakan const membantu Anda menunjukkan bagian mana dari kode yang benar-benar tidak akan berubah. Ini meningkatkan keterbacaan kode karena pembaca dapat dengan mudah membedakan antara nilai konstan dan nilai yang dinamis.

Kapan Sebaiknya Menggunakan const?
Widget Statis: Gunakan const untuk widget yang tidak berubah sepanjang waktu aplikasi berjalan, seperti judul aplikasi (AppBar title), ikon, teks deskriptif, atau elemen dekoratif lainnya.

Parameter dan Warna yang Tetap: Jika Anda memiliki nilai tetap, seperti warna atau padding, yang akan selalu sama, menggunakan const bisa membuat kode lebih efisien.

Dalam Koleksi Data: Jika Anda memiliki list atau map yang nilainya tidak berubah, menggunakan const pada deklarasi koleksi tersebut akan menghemat memori.

2. # Column
Arah Tata Letak: Column menyusun widget secara vertikal, dari atas ke bawah. Ini berguna ketika Anda ingin menampilkan elemen-elemen secara berurutan dalam satu kolom, seperti daftar atau form dengan beberapa field input.
Properti Utama:
mainAxisAlignment: Mengatur posisi widget di sepanjang sumbu utama (vertikal) dalam kolom. Pilihan yang umum meliputi:
MainAxisAlignment.start: Meletakkan semua widget di bagian atas kolom.
MainAxisAlignment.center: Memusatkan widget di tengah kolom.
MainAxisAlignment.end: Menyusun widget di bagian bawah kolom.
MainAxisAlignment.spaceBetween: Memberi jarak antar widget dengan spasi sama di antaranya, tanpa spasi di ujung atas dan bawah.
MainAxisAlignment.spaceAround: Memberi jarak antar widget dengan spasi sama di antaranya serta spasi kecil di ujung atas dan bawah.
MainAxisAlignment.spaceEvenly: Membagi spasi secara merata, termasuk di ujung atas dan bawah.
crossAxisAlignment: Mengatur posisi widget di sepanjang sumbu sekunder (horizontal) dalam kolom. Pilihan meliputi:
CrossAxisAlignment.start: Meletakkan semua widget di sisi kiri kolom.
CrossAxisAlignment.center: Memusatkan widget di tengah kolom.
CrossAxisAlignment.end: Meletakkan semua widget di sisi kanan kolom.
children: Daftar widget yang akan disusun dalam kolom.

# Row
Arah Tata Letak: Row menyusun widget secara horizontal, dari kiri ke kanan. Ini berguna ketika Anda ingin menampilkan elemen-elemen berdampingan dalam satu baris, seperti ikon dengan teks di samping atau tombol-tombol dalam satu baris.
Properti Utama:
mainAxisAlignment: Mengatur posisi widget di sepanjang sumbu utama (horizontal) dalam baris. Pilihan yang umum meliputi:
MainAxisAlignment.start: Menyusun widget di sisi kiri baris.
MainAxisAlignment.center: Memusatkan widget di tengah baris.
MainAxisAlignment.end: Menyusun widget di sisi kanan baris.
MainAxisAlignment.spaceBetween: Memberi jarak antar widget dengan spasi sama di antaranya, tanpa spasi di ujung kiri dan kanan.
MainAxisAlignment.spaceAround: Memberi jarak antar widget dengan spasi sama di antaranya serta spasi kecil di ujung kiri dan kanan.
MainAxisAlignment.spaceEvenly: Membagi spasi secara merata, termasuk di ujung kiri dan kanan.
crossAxisAlignment: Mengatur posisi widget di sepanjang sumbu sekunder (vertikal) dalam baris. Pilihan meliputi:
CrossAxisAlignment.start: Menyusun widget di bagian atas baris.
CrossAxisAlignment.center: Memusatkan widget di tengah baris.
CrossAxisAlignment.end: Menyusun widget di bagian bawah baris.
children: Daftar widget yang akan disusun dalam baris.
Perbandingan Utama

3. Dalam form ini, elemen input yang digunakan adalah sebagai berikut:

TextFormField untuk Name: Elemen input ini digunakan untuk memasukkan teks, di mana pengguna diharuskan mengisi nama item. Validasi diterapkan untuk memastikan bahwa pengguna tidak meninggalkan kolom ini kosong. Jika kolom ini kosong, pesan kesalahan akan muncul, yaitu “Name is required.”

TextFormField untuk Amount: Elemen input ini digunakan untuk memasukkan jumlah item dan menggunakan keyboard numerik agar input lebih mudah diisi dengan angka. Validasi pada kolom ini memastikan bahwa jumlah yang dimasukkan bukan hanya tidak kosong tetapi juga merupakan angka positif. Jika input tidak memenuhi syarat ini, pesan kesalahan seperti "Amount is required" atau "Enter a positive number" akan ditampilkan.

TextFormField untuk Description: Elemen input ini juga menerima teks dan digunakan untuk menambahkan deskripsi item. Sama seperti kolom Name, input ini memerlukan validasi yang memastikan bahwa kolom tidak kosong. Jika kosong, pesan kesalahan “Description is required” akan muncul.

4. Memory updated
Untuk mengatur tema dalam aplikasi Flutter, saya menggunakan properti theme pada widget MaterialApp. Dengan theme, saya bisa menentukan berbagai aspek tampilan secara konsisten di seluruh aplikasi, seperti warna utama (primaryColor), warna aksen (accentColor), font, dan gaya tombol. Ini dilakukan dengan mendefinisikan ThemeData di dalam theme, yang berisi semua pengaturan tampilan yang diinginkan.

Dengan menerapkan ThemeData, setiap elemen yang mengacu pada tema aplikasi akan secara otomatis menggunakan warna, gaya teks, dan bentuk yang sudah didefinisikan, sehingga memastikan konsistensi tanpa perlu mengatur gaya secara manual di setiap widget. Flutter juga mendukung tema gelap melalui darkTheme, yang memungkinkan transisi otomatis saat pengguna mengaktifkan mode gelap di perangkat mereka.

Jika tema sudah diterapkan pada aplikasi, maka akan lebih mudah mengatur ulang tampilan aplikasi secara keseluruhan hanya dengan mengubah ThemeData.

5. Dalam aplikasi Flutter dengan banyak halaman, saya menggunakan Navigator untuk menangani navigasi antar halaman dengan mulus. Navigator menyediakan metode seperti push dan pop, yang memungkinkan saya menambahkan dan menghapus halaman dari stack navigasi.

Berikut cara saya menangani navigasi dalam aplikasi dengan beberapa halaman:

Navigasi ke Halaman Baru: Untuk berpindah ke halaman baru, saya menggunakan Navigator.push. Ini memungkinkan halaman baru ditambahkan ke stack navigasi, yang dapat ditutup atau "pop" untuk kembali ke halaman sebelumnya. Biasanya, saya menerapkan metode Navigator.push(context, MaterialPageRoute(builder: (context) => HalamanBaru())) untuk berpindah halaman.

Kembali ke Halaman Sebelumnya: Untuk menutup halaman yang sedang dibuka dan kembali ke halaman sebelumnya, saya menggunakan Navigator.pop. Ini berguna ketika saya ingin memastikan bahwa pengguna bisa kembali tanpa perlu memulai ulang navigasi.

Navigasi Named Routes: Jika aplikasi memiliki banyak halaman yang sering dinavigasikan, saya biasanya menggunakan named routes. Dengan named routes, saya dapat mendefinisikan rute di dalam MaterialApp sehingga cukup memanggil nama rute ketika ingin melakukan navigasi. Ini meningkatkan keterbacaan dan memudahkan pengelolaan rute, terutama untuk aplikasi yang kompleks.

Menggunakan Drawer atau Bottom Navigation: Untuk aplikasi dengan banyak fitur atau halaman yang sering diakses, saya juga memanfaatkan widget Drawer atau BottomNavigationBar. Drawer biasanya menyediakan akses cepat ke berbagai halaman atau bagian aplikasi, sementara Bottom Navigation cocok untuk tata letak dengan beberapa fitur utama yang perlu diakses langsung.

Menggunakan teknik navigasi ini membantu menciptakan pengalaman pengguna yang konsisten dan memudahkan pengaturan serta pemeliharaan rute dalam aplikasi yang memiliki banyak halaman.