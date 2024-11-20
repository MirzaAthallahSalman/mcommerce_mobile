Tugas 8 : 
1. Kegunaan const di Flutter: const dipakai untuk membuat widget yang tidak berubah-ubah jadi "immutable" (tidak perlu dibangun ulang saat UI di-render). Keuntungan pakai const adalah mengurangi beban render ulang sehingga lebih efisien dan performa aplikasi meningkat. Sebaiknya pakai const untuk widget yang statis atau tidak perlu diperbarui. Hindari pakai const kalau widgetnya dinamis atau berubah-ubah nilainya.
2. Perbandingan Column dan Row di Flutter:
Column menampilkan widget secara vertikal, sedangkan Row menampilkan widget secara horizontal.
3. Elemen Input pada Halaman Form: Pada tugas ini, elemen input yang dipakai misalnya TextField, DropdownButton, dan Checkbox. Elemen input lain yang belum digunakan bisa jadi Slider, Switch, atau RadioButton, yang sesuai dipakai untuk input nilai bertingkat atau pilihan tunggal.
4. Pengaturan Tema di Flutter: Tema (theme) di Flutter diatur menggunakan ThemeData, yang bisa di-set pada MaterialApp. Ini berguna supaya warna, font, dan gaya komponen konsisten di seluruh aplikasi. Kalau pakai dark mode atau light mode, bisa disesuaikan di sini
5. Navigasi pada Aplikasi dengan Banyak Halaman: Navigasi di Flutter bisa dilakukan dengan Navigator untuk push dan pop halaman. Untuk struktur aplikasi besar, bisa pakai Navigator.pushNamed() dengan routes yang didefinisikan di MaterialApp.

Tugas 9 : 
1. Kenapa Perlu Model untuk JSON?
Rapi: Model bikin data terstruktur, gampang diolah.
Validasi: Ngecek data biar sesuai format.
Error Handling: Kalau ada data yang salah, cepat ketahuan.
Pemeliharaan: Kode jadi lebih gampang dibaca dan dikelola.
Kalau nggak pakai model, rawan error kayak salah tipe data, key yang hilang, atau parsing gagal.

2. Fungsi Library http
Kirim Data: Bisa GET, POST, dll, buat komunikasi ke server.
Ambil Data: Parsing respons JSON dari server.
Atur Header: Misal buat autentikasi.
Asynchronous: Prosesnya nggak ganggu UI.

3. Apa Itu CookieRequest?
Atur Cookie: Biar login tetap aktif.
Autentikasi: Nyimpan status user login.
Keamanan: Cookie nggak asal dikirim.
Shared State: Semua komponen pakai cookie yang sama.
Harus dibagi ke semua komponen biar konsisten, terutama buat autentikasi.

4. Mekanisme Kirim Data di Flutter
User input data → dikirim lewat http.post.
Django terima, proses (misal simpan ke database).
Django kirim respons JSON ke Flutter.
Flutter olah data dan tampilkan di UI.

5. Mekanisme Login, Register, Logout
Login:
. User masukin email & password → kirim ke Django.
Django cek database → kirim cookie/token ke Flutter.
Flutter simpan cookie/token → user bisa akses menu.
Register:

User daftar → kirim data ke Django.
Django buat akun → kirim respons sukses ke Flutter.
Logout:

Flutter kirim request logout → Django hapus sesi.
Cookie/token dihapus dari app → user balik ke halaman login.

6. Langkah-langkah Implementasi Checklist Secara Step-by-Step
Persiapan Django:

Buat aplikasi baru untuk autentikasi (login, register, logout) dan tambahkan ke INSTALLED_APPS.
Instal library django-cors-headers untuk mengizinkan akses dari Flutter.
Tambahkan fungsi login, register, dan logout di views.py, lalu definisikan rutenya di urls.py.
Persiapan Flutter:

Instal paket provider dan pbp_django_auth untuk kebutuhan autentikasi.
Buat halaman login dan register, lalu atur halaman login sebagai halaman pertama aplikasi.
Membuat Model Kustom:

Gunakan Quicktype untuk membuat model yang sesuai dengan format JSON dari Django.
Simpan model tersebut di folder models pada proyek Flutter.
Membuat Halaman Katalog Barang:

Buat halaman untuk daftar barang (list_product.dart) yang mengambil dan menampilkan data dari JSON.
Integrasikan halaman katalog ini ke sidebar (left_drawer.dart) dan jadikan bagian dari halaman utama.
Membuat Halaman Detail Barang:

Tambahkan halaman khusus untuk detail barang, lengkap dengan semua atributnya.
Hubungkan katalog dengan halaman detail menggunakan navigasi ketika item di klik.
Filter Barang Berdasarkan User:

Tambahkan fungsi di Django untuk mengembalikan data barang yang hanya terkait dengan user yang sedang login.
Sesuaikan URL permintaan di Flutter agar hanya mengambil data barang milik user tersebut.







