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