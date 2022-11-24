# counter_7

## Jelaskan apa yang dimaksud dengan stateless widget dan stateful widget dan jelaskan perbedaan dari keduanya.
Stateless widget merupakan widget yang kondisinya tidak pernah berubah. Sebaliknya, stateful widget dapat berubah kondisi ketika terdapat action yang dilakukan/ketika user berinteraksi dengan widget tersebut.
## Sebutkan widget apa saja yang kamu pakai di proyek kali ini dan jelaskan fungsinya.
Widget yang digunakan pada Tugas 7 ini adalah `FloatingActionButton` widget tersebut di-bind oleh fungsi yang akan increment dan decrement _counter dan juga menampilkan informasi "GANJIL" dan "GENAP" sesuai kondisional yang telah dibuat. Selain itu, pada widget pun dibuat kondisional, yaitu ketika counter bernilai 0, maka `FloatingActionButton` akan diubah dengan `sizedBox` transparan.
## Apa fungsi dari setState()? Jelaskan variabel apa saja yang dapat terdampak dengan fungsi tersebut.
SetState berfungsi untuk memberi tahu ketika ada internal state yang berubah sehingga state yang ditampilkan akan berubah juga. Misal, untuk tugas 7 ini, variabel yang terdampak adalah _counter.
## Jelaskan perbedaan antara const dengan final.
`const` berfungsi untuk men-_declare_ variabel yang immutable lalu value nya harus dipastikan sudah diketahui saat compile. Sementara `final` berfungsi untuk men-_declare_ variabel immutable yang valuenya boleh belum diketahui atau sudah diketahui saat compile.
## Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas.
1. run `flutter create counter_7`
2. mengedit `main.dart` pada /lib
3. membuat fungsi decrementCounter untuk variabel _counter.
4. Menambahkan widget floatingActionButton dengan flex row dan padding serta alignment spaceBetween (widget akan mengisi tiap ujung dari container). Selain itu membuat kondisional untuk button decrement. Ketika value counter bernilai 0, button decrement akan diganti oleh `sizedBox` transparan.
5. Bind tiap button dengan fungsi increment dan decrement yang sudah dibuat sebelumnya.
6. Membuat widget Text dengan kondisional apabila value dari _counter bernilai genap atau ganjil.
7. melakukan testing dengan command `flutter run`

# Tugas 8 : Flutter Form

## Jelaskan perbedaan Navigator.push dan Navigator.pushReplacement
`Navigator.push` akan menambahkan (push) sebuah rute ke tumpukan (_stack_) Navigator. Sedangkan `Navigator.pushReplacement` akan mengganti rute yang sedang ditampilkan dengan *push* route atau halaman baru ke stack Navigator.

## Sebutkan widget apa saja yang kamu pakai di proyek kali ini dan jelaskan fungsinya.
`TextFormField` field untuk menerima input dari user. <br>
`Drawer` sebagai hamburger menu untuk navigasi ke page berbeda. <br>
`DropdownButtonFormField` sebagai dropdown untuk menentukan input yang diberikan merupakan pemasukan atau pengeluaran. <br>
`FloatingActionButton` sebagai button yang di-bind untuk menambah data ke dalam list <br>
`Card` untuk menampilkan data input yang ada pada list.

##  Sebutkan jenis-jenis event yang ada pada Flutter (contoh: onPressed).
1. `onPressed()`
2. `onTap()`
3. `onChanged()`
4. `onSaved()`

##  Jelaskan bagaimana cara kerja Navigator dalam "mengganti" halaman dari aplikasi Flutter.
Navigator bekerja seperti struktur data stack, yaitu konsep _Last In First Out_. Setiap tampilan akan di-_push_ ke stack Navigator untuk ditampilkan. Jadi, tampilan yang ditampilkan merupakan halaman yang terakhir di-_push_ atau berada pada posisi paling atas pada stack.

## Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas.
1. Membuat widget drawer untuk navigasi ke halaman lain.
2. Membuat file form.dart untuk menerima input dari user. Judul dan Nominal menerima input menggunakan TextFormField sementara untuk tipe pemasukan dan pengeluaran menggunakan DropdownButtonFormField.
3. Membuat FloatingActionButton yang di-bind untuk menyimpan input. Selain itu, mem-validasi apakah input sudah terisi benar atau belum.
4. Menambahkan input yang sudah tervalidasi ke dalam list data.
5. Membuat data.dart untuk menampilkan data input yang sudah disimpan.
5. Mengimport file .dart agar list input data dapat diakses pada data.dart.
6. Menampilkan data pada list dengan menggunakan builder ListView.builder().
7. Membuat Card untuk menampilkan judul, nominal, jenis budget.

# Tugas 9
## Apakah bisa kita melakukan pengambilan data JSON tanpa membuat model terlebih dahulu? Jika iya, apakah hal tersebut lebih baik daripada membuat model sebelum melakukan pengambilan data JSON?
Bisa, ketika data yang ada pada JSON tidak banyak. Karena jika data JSON sudah banyak, maka jika terjadi ketidaksesuaian struktur, kita susah untuk memperbaikinya. Membuat model akan menjaga kejelasan kode dan efisiensi.
## Sebutkan widget apa saja yang kamu pakai di proyek kali ini dan jelaskan fungsinya.
`Card` untuk menampilkan data judul yang ada pada JSON. <br>
`Text` untuk menampilkan teks. <br>
`Checkbox` untuk menerima input berupa onChanged. Jadi ketika ada perubahan value dari checkbox, akan dijalankan kondisional <br>
`FutureBuilder` untuk membangun tampilan dirinya sendiri. Berguna untuk menampilkan berbagai widget yang sama dengan data yang berbeda. <br>
`Column` Menampilkan susunan isi widget / children secara vertikal. <br>
`Row` Menampilkan susunan isi children secara horizontal.
## Jelaskan mekanisme pengambilan data dari json hingga dapat ditampilkan pada Flutter.
1. Melakukan pub get http
2. Membuat model serialisasi data JSON
3. Melakukan fetch data dengan get HTTP request
4. Serialisasi data JSON sesuai model dan simpan ke dalam list
5. Tampilkan data dengan widget
## Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas.
1. Menambah dependensi HTTP dengan pub get http
2. Menambahkan model serialisasi data JSON
3. Fetch data dari web heroku pada tugas 3, lalu serialize data tersebut. Lalu menambahkan pula permission untuk android
4. Membuat halaman baru untuk menampilkan data JSON pada card
5. Membuat navigator.push dan routing ke halaman detail
6. Membuat kalaman detail yang menampilkan data atribut-atribut dari objek-objek model watchlist