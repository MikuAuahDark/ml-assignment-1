Ringkasan Pertemuan 1
=====

_Association rules_ adalah aturan (namanya "rules") yang memberi asosiasi antara objek 1 dan objek lainnya.
Aturan asosiasi `A => B` berarti:

1. `A` dan `B` adalah himpunan-himpunan objek yang saling terpisah.

2. `A` adalah bagian kiri (_left-hand side_/**_lhs_**) dan `B` adalah bagian kanan (_right-hand side_/**_rhs_**)

Umumnya, ada 3 ukuran yang dipakai untuk memilih aturan, yaitu:

1. Support, persentase objek muncul pada transaksi, atau banyak transaksi mengandung A dibagi dengan jumlah transaksi.

2. Confidence, persentase objek A dan B muncul pada transaksi dibagi persentase objek A muncul.

3. Lift, perbandingan confidence dengan transaksi yang mengandung B.

Rumus-rumusnya adalah sebagai berikut:

```
Support:
  supp(A) = Transaksi mengandung A : Jumlah transaksi

Confidence:
  conf(A, B) = supp(A gabung B)             : supp(A)
             = Transaksi mengandung A dan B : Transaksi mengandung A

Lift:
  lift(A, B) = conf(A, B) : supp(B)
             = supp(A gabung B) : (supp(A) * supp(B))
```

Algoritma yang bisa dipakai ada 2: **A Priori** dan **FP Growth**.

Ada baiknya jika data di pre-process terlebih dahulu agar hasilnya maksimal. Contohnya ditulis dengan bahasa R tetapi
R hanya bersifat pengenalan dan selebihnya menggunakan Python.
