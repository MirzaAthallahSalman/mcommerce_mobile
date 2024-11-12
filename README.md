Tugas 8 : 
1. Kegunaan const di Flutter: const dipakai untuk membuat widget yang tidak berubah-ubah jadi "immutable" (tidak perlu dibangun ulang saat UI di-render). Keuntungan pakai const adalah mengurangi beban render ulang sehingga lebih efisien dan performa aplikasi meningkat. Sebaiknya pakai const untuk widget yang statis atau tidak perlu diperbarui. Hindari pakai const kalau widgetnya dinamis atau berubah-ubah nilainya.
2. Perbandingan Column dan Row di Flutter:
Column menampilkan widget secara vertikal, sedangkan Row menampilkan widget secara horizontal.
3. Elemen Input pada Halaman Form: Pada tugas ini, elemen input yang dipakai misalnya TextField, DropdownButton, dan Checkbox. Elemen input lain yang belum digunakan bisa jadi Slider, Switch, atau RadioButton, yang sesuai dipakai untuk input nilai bertingkat atau pilihan tunggal.
4. Pengaturan Tema di Flutter: Tema (theme) di Flutter diatur menggunakan ThemeData, yang bisa di-set pada MaterialApp. Ini berguna supaya warna, font, dan gaya komponen konsisten di seluruh aplikasi. Kalau pakai dark mode atau light mode, bisa disesuaikan di sini
5. Navigasi pada Aplikasi dengan Banyak Halaman: Navigasi di Flutter bisa dilakukan dengan Navigator untuk push dan pop halaman. Untuk struktur aplikasi besar, bisa pakai Navigator.pushNamed() dengan routes yang didefinisikan di MaterialApp.
