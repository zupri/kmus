## Latar belakang
Berawal dari mencari kamus untuk linux yang berbasis CLI, tanpa instalasi (portable), tanpa kompilasi, data mudah di edit dan ditambah tidak menemukan sesuai yang saya harapkan. Mulai berpikir untuk membuat aplikasi sendiri. Awalnya mau mengembangkan dengan python setelah beberapa pertimbangan lebih mudah untuk menggunakan file csv saja dan memanfaatkan command linux yang sudah ada seperti `grep` dan `more`.

kmus-db adalah file data kamus dengan format csv bukan aplikasi kamus, cara menggunakannya sangat sederhana cukup ketik `grep -riw ^kata-yang-dicari`.

Data kmus berisi kamus English, Indonesia, glossary dan istilah umum lainnya. Data kmus diambil dari gkamus, bank indonesia dll.

## Contoh penggunaan
```bash
$ grep -w ^ant kmus-db 
ant,"kb. semut. a. hill sarang semut, busut. flying a. kelekatu, laron. red a. kerangga. white a. anai-anai."
ant.,(Antara) Indonesian News Agency.
```
atau
```bash
$ grep -riw ^ant
kmus-db:ant,"kb. semut. a. hill sarang semut, busut. flying a. kelekatu, laron. red a. kerangga. white a. anai-anai."
kmus-db:ant.,(Antara) Indonesian News Agency.
```
-riw adalah optinal yang terdiri dari -r -i -w :

-r : recursive yang artinya pencarian tidak hanya pada data csv saja tapi file lain seperti readme juga akan dicari.

-i : ignore-case mengabaikan huruf besar atau kecil.

-w : word-regexp pencarian untuk kata lengkap.

^ : artinya pencarian dilakukan diawal baris.


contoh lain
```bash
$ grep ^ant kmus-db
```
atau
```bash
$ grep -w ^ant kmus-db
```
atau
```bash
$ grep -wi ^ant kmus-db
```
atau (rekomendasi)
```bash
$ more kmus-db | grep -wi ^ant
```
dengan `more` pencarian berikutnya lebih mudah tinggal tekan tombol panah atas dan hapus kata lama dan ganti dengan kata baru.

## Menambahkan data
Untuk menambah data disarankan dengan format csv meski bisa tanpa csv, hal ini untuk memudahkan jika mau dikonversi ke format lain.

contoh :
```bash
$ echo \nkata-baru, arti kata >> kmus-db
$ echo grep, \(linux-cli\) pencarian konten file dengan pola. >> kmus-db
```
atau kita edit di file lain misal `new-data.csv` dan dilakukan merge
```bash
$ more new-data.csv >> kmus-db
```

isi file dalam format csv lihat file `contoh.md`.

contoh
```
kata, (konteks/kepanjangan/maksud) arti kata.
```
tambahkan tanda kutip dua (`"`) jika dalam kata atau arti kata ada koma (`,`)
```
kata baru, "arti,kata"
"kata,baru", "arti,kata"
```