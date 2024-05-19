# OPERATOR LOGIKA DAN PEMBANDING
## AND
### Struktur 

```mysql
SELECT nama_kolom1,nama_kolom2 FROM nama_tabel WHERE nama_kolom3="nilai_kolom1" AND nama_kolom4="nama_kolom2";
```

### Contoh

```mysql
SELECT warna_pemilik FROM desc_mobil WHERE warna="Hitam" AND pemilik="Ibrahim";
```

### Hasil

![AND](and.jpg)



### Analisis 

Mengambil data dari tabel `desc_mobil` yang memenuhi dua kondisi: `warna` mobil adalah `Hitam` dan `pemilik` mobil adalah `Ibrahim`. Kemudian, program tersebut hanya mengambil kolom `warna_pemilik` dari hasil query. Dengan kata lain, program ini mencari mobil dengan warna hitam yang dimiliki oleh seseorang yang bernama Ibrahim.

### Kesimpulan 

Bahwa program tersebut mencari mobil dengan warna hitam yang dimiliki oleh seseorang yang bernama Ibrahim.

## OR
### Struktur 

```mysql
SELECT nama_kolom1,nama_kolom2 FROM nama_tabel WHERE nama_kolom3="nilai_kolom1" OR nama_kolom4="nama_kolom2";
```

### Contoh

```mysql
SELECT warna_pemilik FROM desc_mobil WHERE warna="Hitam" OR pemilik="Ibrahim";
```

### Hasil

![OR](or.jpg)

### Analisis 

Untuk mengambil data dari tabel `desc_mobil`. Pernyataan `SELECT` digunakan untuk memilih kolom `warna_pemilik` dari tabel tersebut. Kriteria seleksi ditetapkan dengan menggunakan pernyataan `WHERE`, dimana baris yang memiliki nilai `warna` sama dengan `Hitam` atau nilai `pemilik` sama dengan `Ibrahim` akan dipilih. Ini berarti program akan mengambil semua data pemilik mobil yang memiliki mobil berwarna hitam atau pemilik mobil yang bernama Ibrahim.

### Kesimpulan 

Program tersebut akan mengambil data mengenai pemilik mobil yang memiliki mobil berwarna hitam, serta data mengenai mobil yang dimiliki oleh seseorang bernama `Ibrahim`, dari tabel `desc_mobil`.

## BETWEEN-AND
### Struktur 

```mysql
SELECT * FROM nama_tabel WHERE nama_kolom BETWEEN nilai_kolom1 AND nilai_kolom2;
```

### Contoh

```mysql
SELECT * FROM desc_mobil WHERE harga_rental BETWEEN 100000 AND 200000;
```

### Hasil

![BETWEEN-AND](between_and.jpg)

### Analisis 

Untuk mengambil semua data dari tabel `desc_mobil` di mana nilai kolom `harga_rental` berada dalam rentang antara `100000` dan `200.000`. Ini menunjukkan bahwa program tersebut bertujuan untuk mengambil semua mobil yang memiliki harga sewa di antara rentang tersebut.

### Kesimpulan 

Digunakan untuk mengekstrak data mobil-mobil yang memiliki harga sewa dalam rentang tertentu, yaitu antara `100000` dan `200000`.

## <=
### Struktur 

```mysql
SELECT * FROM nama_tabel WHERE nama_kolom <= nilai_kolom;
```

### Contoh

```mysql
SELECT * FROM desc_mobil WHERE harga_rental <= 50000;
```

### Hasil

![<=](lebih_kecil_sama_dengan.jpg)

### Analisis 

Bertujuan untuk mengambil semua data dari tabel `desc_mobil` di mana harga rental mobil kurang dari atau sama dengan `50000`. Ini adalah contoh penggunaan klausa `WHERE` untuk melakukan filtering data berdasarkan kondisi tertentu. Dengan menggunakan `*`, program ini akan mengambil semua kolom yang ada dalam tabel `desc_mobil`.

### Kesimpulan 

Mengambil semua data mobil dari tabel `desc_mobil` yang memiliki harga rental kurang dari atau sama dengan `50000`.

## =>
### Struktur 

```
SELECT * FROM nama_tabel WHERE nama_kolom => nilai_kolom;
```

### Contoh

```mysql
SELECT * FROM desc_mobil WHERE harga_rental => 50000;

```

### Hasil

![=>](lebih_besar_sama_dengan.jpg)

### Analisis 

Mengambil data dari tabel `desc_mobil` di mana nilai kolom `harga_rental` lebih besar dari atau sama dengan `50000`. Ini berarti program ini akan mengembalikan semua baris dari tabel `desc_mobil` di mana harga rental mobilnya setidaknya `50000` atau lebih tinggi.

### Kesimpulan 

Digunakan untuk mengambil data `desc_mobil` dari sebuah tabel di mana harga rental mobilnya setidaknya `50000` atau lebih tinggi.

## <> Atau !=
### Struktur 

```mysql
SELECT * FROM nama_tabel
WHERE nama_kolom <> nama_nilai;

```
### Contoh

```mysql
SELECT * FROM desc_mobil WHERE harga_rental <> 50000;
```

### Hasil

![<>/!=](atau.jpg)

### Analisis 

Mengambil semua baris dari tabel `desc_mobil` di mana harga rental tidak sama dengan `50000`. Ini berarti hanya data mobil yang memiliki harga rental yang berbeda dari `50000` yang akan ditampilkan.

### Kesimpulan 

Bertujuan untuk memfilter data mobil dari tabel `desc_mobil` dimana harga rental tidak sama dengan `50000`.

# Tantangan
## Struktur 

```mysql
SELECT nama_kolom1 FROM nama_tabel WHERE nama_kolom2;
```

## Contoh

```
SELECT nama_asli FROM akun where id_akun=1;
```

## Hasil

![Tantangan-akun](Tantangan.jpg)

## Analisis 



## Kesimpulan 



# IN
## IN
### Struktur 

```mysql
SELECT * FROM nama_tabel WHERE nama_kolom IN ("nilai_kolom1","nilai_kolom2");
```

### Contoh

```mysql
SELECT * FROM desc_mobil WHERE warna IN ("Silver","Merah");
```

### Hasil

![IN](in.jpg)

### Analisis 

Mengambil semua data dari tabel `desc_mobil` di mana `warna` mobil adalah `Silver` atau `Merah`. Ini digunakan untuk menampilkan informasi tentang mobil-mobil dengan warna tertentu dalam basis data.

### Kesimpulan 

Untuk menampilkan semua data mobil yang memiliki warna `Silver` atau `Merah` dari tabel `desc_mobil`.
 
## IN-AND
### Struktur 

```mysql
 select * from nama_tabel
where nama_kolom1 in ("nilai_kolom1","nilai_kolom2")
and nama_kolom2 = nilai_kolom3;
```

### Contoh

```mysql
 select * from desc_mobil
where warna in ("Hitam","Silver")
and harga_rental = 50000;
```

### Hasil

![IN-AND](in_and.jpg)

### Analisis 

Mengambil semua baris dari tabel `desc_mobil` dimana nilai kolom warna adalah `Hitam` atau `Silver` dan nilai kolom `harga_rental` adalah `50000`. Ini menunjukkan bahwa program tersebut mencari mobil dengan warna `Hitam` atau `Silver` yang memiliki harga rental sebesar `50000`.

### Kesimpulan 

Bahwa pengguna ingin mencari mobil dengan warna `Hitam` atau `Silver` yang tersedia untuk disewa dengan harga rental sebesar `50000`.

## IN-OR
### Struktur 

```mysql
 select * from nama_tabel
where nama_kolom1 in ("nilai_kolom1","nilai_kolom2")
and nama_kolom2 = nilai_kolom3;
```

### Contoh

```mysql
 select * from desc_mobil
where warna in ("Hitam","Silver")
or harga_rental = 50000;
```

### Hasil

![IN-OR](in_or.jpg)

### Analisis 

Memilih semua kolom dari tabel `desc_mobil` dimana nilai kolom `warna` adalah `Hitam` atau `Silver`, atau nilai kolom `harga_rental` adalah `50000`. Ini akan mengembalikan baris-baris dari tabel `desc_mobil` yang memenuhi salah satu dari kondisi tersebut.

### Kesimpulan

Mengambil data dari tabel desc_mobil yang memiliki warna mobil `Hitam` atau `Silver`, atau memiliki harga rental sebesar `50000`.

## IN-AND-OPERATOR 
### Struktur 

```mysql
 select * from nama_tabel
where nama_kolom1 in ("nilai_kolom1","nilai_kolom2")
and nama_kolom2 > nilai_kolom3;
```

```mysql
 select * from nama_tabel
where nama_kolom1 in ("nilai_kolom1","nilai_kolom2")
and nama_kolom2 < nilai_kolom3;
```

### Contoh

```mysql
 select * from desc_mobil
where warna in ("Hitam","Silver")
and harga_rental > 50000;
```

```mysql
 select * from desc_mobil
where warna in ("Hitam","Silver")
and harga_rental < 100000;
```

### Hasil

![IN-AND-OPERATOR](in_and_lebihbesar.jpg)

![IN-AND-OPERATOR](in_and_lebihkecil.jpg)

### Analisis 

Mengambil data dari tabel `desc_mobil` dimana nilai kolom `warna` adalah `Hitam` atau `Silver`, dan nilai kolom `harga_rental` lebih besar dari `50000`. Analisisnya menunjukkan bahwa program ini bertujuan untuk menampilkan informasi tentang mobil-mobil dengan warna `Hitam` atau `Silver` yang memiliki harga rental lebih dari `50000`.

Bertujuan untuk menampilkan semua data dari tabel `desc_mobil` dimana `warna` mobil adalah `hitam` atau `silver`, dan harga rentalnya kurang dari `100000`. Ini menunjukkan bahwa pengguna tertarik untuk melihat mobil dengan warna tertentu yang juga memiliki harga sewa yang terjangkau.

### Kesimpulan 

Digunakan untuk mencari mobil-mobil dengan warna `Hitam` atau `Silver` yang memiliki harga rental lebih dari `50000` dalam tabel `desc_mobil`.

Mencari mobil dengan warna `hitam` atau `silver` dan harga sewa di bawah `100000`.

# LIKE
## Mencari awalan
### Struktur 

```mysql
  select * from nama_tabel
where nana_kolom like "nilai_kolom";
```

### Contoh

```mysql
  select * from desc_mobil
where pemilik like "Ib%";
```

### Hasil

![LIKE](mencari_awalan.jpg)

### Analisis 

Mengambil semua kolom dari tabel `desc_mobil` di mana nilai kolom `pemilik` dimulai dengan `Ib`. Ini adalah contoh penggunaan wildcard (`%`) dalam SQL untuk mencocokkan pola tertentu dari nilai kolom. Dalam hal ini, kita mencari pemilik mobil yang namanya dimulai dengan `Ib`.

### Kesimpulan 

Digunakan untuk mengambil data dari tabel `desc_mobil` di mana pemilik mobil memiliki nama yang dimulai dengan `Ib`.

## Mencari akhiran
### Struktur 

```mysql
  select * from nama_tabel
where nana_kolom like "nilai_kolom";
```

### Contoh

```mysql
  select * from desc_mobil
where pemilik like "%m";
```

### Hasil

![LIKE](mencari_akhiran.jpg)

### Analisis 

Melakukan seleksi dari tabel `desc_mobil` dimana nilai kolom `pemilik` berakhir dengan huruf `m`. Ini akan mengembalikan semua baris dalam tabel `desc_mobil` dimana nama pemilik mobil diakhiri dengan huruf `m`.

### Kesimpulan 

digunakan untuk mengambil data dari tabel `desc_mobil` dimana nama pemilik mobil diakhiri dengan huruf `m`.

## Mencari awalan & akhiran
### Struktur 

```mysql
  select * from nama_tabel
where nama_kolom like "nilai_kolom";
```

### Contoh

```mysql
  select * from desc_mobil
where pemilik like "b%m";
```

### Hasil

![LIKE](mencari_awalan_dan_akhiran.jpg)

### Analisis 

Mengambil semua data dari tabel `desc_mobil` di mana nilai kolom `pemilik` dimulai dengan huruf 'b' dan diikuti dengan huruf 'm'. Tanda '%' dalam kondisi `LIKE` merupakan wildcard yang akan cocok dengan nol atau lebih karakter apa pun. Jadi, program ini akan mengembalikan semua baris di mana nilai kolom `pemilik` dimulai dengan 'b' dan diikuti oleh 'm'.

### Kesimpulan 

mengambil semua entri dari tabel `desc_mobil` di mana nama pemilik mobil dimulai dengan huruf `b` dan diikuti oleh huruf `m`.

## Kombinasi 
### Struktur 

```mysql
  select * from nama_tabel
where nama_kolom like "nilai_kolom";
```

```mysql
  select * from nama_tabel
where nama_kolom like "nilai_kolom";
```

### Contoh

```mysql
  select * from desc_mobil
where pemilik like "__I%";
```

```mysql
  select * from desc_mobil
where pemilik like "_b%";
```

### Hasil

![LIKE](kombinasi1.jpg)

![LIKE](kombinasi2.jpg)

### Analisis 

Mengambil semua kolom dari tabel `desc_mobil` di mana nilai dalam kolom pemilik dimulai dengan dua karakter, diikuti oleh huruf `I`. dan kemudian karakter apa pun. Ini akan mengembalikan semua baris di mana pemilik mobil memiliki nama yang dimulai dengan `I`.

Mengambil semua data dari tabel `desc_mobil` dimana nilai kolom pemilik dimulai dengan huruf kedua `b` (huruf pertama bisa apa saja karena disimbolkan dengan _ ). Ini akan mengembalikan semua entri yang memiliki pemilik dengan awalan `b`.

### Kesimpulan 

Mengambil data dari tabel `desc_mobil` dimana pemilik mobil memiliki nama yang dimulai dengan huruf `I`.

Mengambil semua entri dari tabel `desc_mobil` dimana nama pemilik mobil dimulai dengan huruf `b` di posisi kedua. Ini dapat berguna untuk mengekstrak data terkait mobil yang dimiliki oleh pemilik dengan nama yang dimulai dengan huruf `b`.

## NOT LIKE
### Struktur 

```mysql
select * from nama_tabel where nama_kolom not like "nilai_kolom";
```

### Contoh

```mysql

select * from desc_mobil where peminjam not like "A%";
```

### Hasil

![LIKE](not_like.jpg)

### Analisis 

Melakukan pemilihan semua baris dari tabel `desc_mobil` di mana nilai kolom peminjam tidak dimulai dengan huruf `A`. Dengan kata lain, program ini akan mengembalikan semua catatan tentang mobil yang tidak dipinjam oleh seseorang yang namanya dimulai dengan huruf `A`.

### Kesimpulan 

Bertujuan untuk mengambil data dari tabel `desc_mobil` di mana mobil-mobil tersebut tidak dipinjam oleh peminjam yang namanya dimulai dengan huruf `A`.

# NULL & NOT
## Struktur 

```mysql
select distinct(nama_kolom) from nama_tabel;
```

```mysql
select distinct(nama_kolom) from nama_tabel order by nama_kolom desc;
```

## Contoh

```mysql
select distinct(pemilik) from desc_mobil;
```

```mysql
select distinct(harga_rental) from desc_mobil order by harga_rebtal desc;
```

## Hasil

![DISTINCT](distinct1.jpg)

![DISTINCT](distinct2.jpg)

## Analisis 

`SELECT DISTINCT(pemilik) FROM desc_mobil;`, digunakan untuk mengambil nilai unik dari kolom 'pemilik' dalam tabel `desc_mobil`. Ini akan menghasilkan daftar pemilik mobil yang berbeda tanpa ada duplikasi.

Mengambil nilai unik dari kolom `harga_rental` dari tabel `desc_mobil`, kemudian mengurutkannya secara descending (menurun). Dengan kata lain, program ini akan menampilkan daftar harga rental mobil tanpa ada nilai yang berulang, dan disusun dari harga yang tertinggi ke terendah.

## Kesimpulan 

Digunakan untuk menghasilkan daftar unik dari pemilik mobil yang terdaftar dalam tabel `desc_mobil`.

Memberikan daftar harga rental mobil yang unik dan diurutkan dari yang tertinggi ke terendah, sehingga memudahkan dalam memahami variasi `harga rental` mobil yang ada dalam database.

# CONCAT, CONCAT_WS, AS
## Menggabungkan kolom tanpa pemisah
### Struktur 

```mysql
select concat (nama_kolom1,nama_kolom2) from nama_tabel;
```

### Contoh 

```mysql
select concat (pemilik,warna) from desc_mobil;
```

### Hasil

![CONCAT](concat.jpg)

### Analisis 

Melakukan pengambilan data dari tabel `desc_mobil` dan menggabungkan nilai dari kolom `pemilik` dengan nilai dari kolom `warna` menggunakan fungsi `concat()`. Hasilnya adalah penggabungan dari nilai kedua kolom tersebut menjadi satu string untuk setiap baris dalam tabel `desc_mobil`.

### Kesimpulan 

Menghasilkan string yang merupakan gabungan antara nilai dari kolom `pemilik` dan kolom `warna` untuk setiap baris dalam tabel `desc_mobil`.

## Menggabungkan kolom dengan pemisah
### Struktur 

```mysql
SELECT CONCAT_WS("_",nama_kolom1,nama_kolom2,nama_kolom3) FROM nama_tabel;
```

### Contoh

```mysql
SELECT CONCAT_WS("-",no_plat,no_mesin,id_pelanggan) FROM desc_mobil;
```

### Hasil

![CONCAT_WS](concat_ws1.jpg)

### Analisis 

Menggabungkan nilai-nilai dari kolom-kolom tertentu dalam tabel `desc_mobil` menggunakan fungsi `CONCAT_WS`. Fungsi `CONCAT_WS` digunakan untuk menggabungkan beberapa string dengan menambahkan separator di antara mereka. Dalam hal ini, string-string yang digabungkan adalah `no_plat`, `no_mesin`, dan `id_pelanggan`, dipisahkan oleh tanda `-`. Hasilnya adalah gabungan nilai-nilai tersebut dalam format yang dipisahkan oleh tanda `-`.

### Kesimpulan 

Menghasilkan string baru yang merupakan gabungan dari nomor plat, nomor mesin, dan ID pelanggan dari tabel `desc_mobil`, dengan setiap nilai dipisahkan oleh tanda `"-"`.

## Memberikan nama kolom alias
### Struktur 

```mysql
SELECT CONCAT_WS("_",nama_kolom1, nama_kolom2) AS nama_kolom3 FROM nama_tabel;
```

### Contoh

```mysql
SELECT CONCAT_WS("+",pemilik, peminjam) AS COLLAB FROM desc_mobil;
```

### Hasil

![AS](as.jpg)

### Analisis 

Mengambil data dari tabel `desc_mobil` dan menggunakan fungsi `CONCAT_WS()` untuk menggabungkan nilai dari kolom pemilik dan peminjam, dengan tanda tambah `"+"` di antara keduanya. Hasilnya adalah kolom baru yang disebut `COLLAB`, yang berisi gabungan nama pemilik dan peminjam, dipisahkan oleh tanda tambah.

### Kesimpulan 

Menghasilkan kolom baru yang menggabungkan nama `pemilik` dan `peminjam` mobil, dipisahkan oleh tanda tambah.

# VIEW
## Membuat tabel virtual
### Struktur 

```mysql
CREATE VIEW nama_tabel AS
 SELECT nama_kolom1,nama_kolom2,nama_kolom3,nama_kolom4 
  FROM nama_tabel
 WHERE nama_kolom5 = "nilai_kolom";
```

### Contoh

```mysql
CREATE VIEW info_no_plat AS
 SELECT id_pelanggan,no_plat,pemilik,peminjam 
  FROM daftar_mobil
 WHERE pemilik = "Ibrahim";
```

### Hasil

![VIEW](membuat.jpg)

### Analisis 

Membuat sebuah view yang disebut `info_no_plat` yang berisi informasi tentang nomor plat mobil yang dimiliki oleh pemilik bernama Ibrahim. View ini akan menampilkan kolom `id_pelanggan`, `no_plat`, `pemilik`, dan `peminjam` dari tabel `daftar_mobil`, tetapi hanya baris-baris di mana pemilik mobil adalah "Ibrahim". Dengan demikian, view ini akan memberikan informasi terkait mobil-mobil yang dimiliki oleh Ibrahim.

### Kesimpulan 

Membuat sebuah view yang memfilter data dari tabel `daftar_mobil` untuk menampilkan informasi hanya tentang mobil-mobil yang dimiliki oleh `pemilik` dengan nama `Ibrahim`.

## Menampilkan tabel virtual
### Struktur 

```mysql
select * from nama_tabel;
```

### Contoh 

```mysql
select * from info_no_plat;
```

### Hasil

![VIEW](menampilkan.jpg)

### Analisis 

Untuk mengambil semua data dari tabel bernama `info_no_plat`. Dengan perintah `SELECT *`, program akan mengambil semua kolom yang ada di tabel tersebut.

### Kesimpulan 

digunakan untuk mengambil semua data dari tabel `info_no_plat`. Tujuan utamanya adalah untuk mengakses informasi yang tersimpan dalam tabel tersebut.

## Menghapus tabel virtual 
### Struktur 

```mysql
DROP VIEW nama_tabel;
```

### Contoh

```mysql
DROP VIEW info_no_plat;
```

### Hasil

![VIEW](menghapus.jpg)

### Analisis 

`DROP VIEW` digunakan untuk menghapus sebuah view dari database. Dalam hal ini, `info_no_plat` adalah nama `view` yang akan dihapus.

### Kesimpulan 

`DROP VIEW info_no_plat;` akan menghapus view dengan nama `info_no_plat` dari database.


# Tantangan 
## Tantangan 1
### query

```mysql
CREATE VIEW peminjam_NULL AS SELECT id_pelanggan,no_plat,peminjam,harga_rental FROM desc_mobil WHERE peminjam IS NULL;
```

### Hasil

![Tantangan](no1.jpg)

## Tantangan 2
### query

```mysql
UPDATE desc_mobil SET peminjam=NULL WHERE id_pelanggan=2;
```

### Hasil

![Tantangan](no2.jpg)

## Tantangan 3

>[!Tantangan3]-
>Tabel Virtual ini dibuat untuk menyediakan informasi tentang mobil yang saat ini tidak dipinjam (peminjamnya NULL), sehingga memudahkan pengelolaan dan pelacakan mobil yang tersedia untuk disewakan. Dengan demikian, orang dapat dengan mudah melihat daftar mobil yang tersedia untuk disewa tanpa harus memeriksa satu per satu dalam database.

# AGREGASI 
## Menghitung total nilai numerik suatu kolom
### Struktur 

```mysql
SELECT SUM(nama_kolom1) AS nama_kolom2 FROM nama_tabel;
```

### Contoh

```mysql
SELECT SUM(harga_rental) AS total_harga FROM daftar_mobil;
```

### Hasil

![AGREGASI](sum.jpg)

### Analisis 

Melakukan pengambilan total harga rental dari tabel `daftar_mobil` dengan menggunakan fungsi agregat `SUM()` untuk menjumlahkan nilai dari kolom `harga_rental`. Ini akan menghasilkan satu baris output yang berisi total harga rental dari semua mobil yang terdaftar dalam tabel tersebut.

### Kesimpulan 

Menghitung total `harga rental` dari semua mobil yang terdaftar dalam tabel `daftar_mobil`. Dengan menggunakan fungsi agregat `SUM()`, program ini memungkinkan untuk dengan cepat dan mudah mendapatkan informasi tentang total pengeluaran untuk rental mobil yang tercatat dalam database.

## Menghitung jumlah baris/data, biasanya berdasarkan kriteria tertentu
### Struktur 

```mysql
SELECT COUNT(nama_kolom1) AS nama_kolom2 FROM nama_tabel;
```

```mysql
SELECT COUNT(nama_kolom1) AS nama_kolom2 FROM nama_tabel;
```


### Contoh

```mysql
SELECT COUNT(pemilik) AS total_pemilik FROM daftar_mobil;
```

```mysql
SELECT COUNT(peminjam) AS total_peminjam FROM daftar_mobil;
```

### Hasil

![AGREGASI](count1.jpg)

![AGREGASI](count2.jpg)

### Analisis 

 `SELECT COUNT(pemilik) AS total_pemilik FROM daftar_mobil;`, menghitung jumlah baris dalam tabel `daftar_mobil` di mana kolom `pemilik` tidak null. Hasilnya adalah total jumlah pemilik mobil yang terdaftar dalam tabel `daftar_mobil`.

Melakukan penghitungan jumlah peminjam dalam tabel `daftar_mobil` dan memberikan hasilnya dalam kolom yang dinamai `total_peminjam`.

### Kesimpulan 

Kesimpulannya, digunakan untuk menghitung jumlah pemilik mobil yang terdaftar dalam tabel `daftar_mobil`.

Digunakan untuk menghitung total jumlah peminjam mobil dari tabel `daftar_mobil`, yang dapat memberikan pemahaman tentang tingkat popularitas atau penggunaan mobil-mobil tersebut dalam periode waktu tertentu.

## Menampilkan nilai terendah
### Struktur 

```mysql
SELECT MIN(nama_kolom1) AS nama_kolom2 FROM nama_tabel;
```

### Contoh

```mysql
SELECT MIN(harga_rental) AS minimum FROM daftar_mobil;
```

### Hasil

![AGREGASI](min.jpg)

### Analisis 

Mengambil nilai terkecil dari kolom `harga_rental` dari tabel `daftar_mobil` dan memberikan hasilnya sebagai kolom yang diberi nama `minimum`. Dengan kata lain, program ini akan menampilkan harga rental mobil terendah yang terdaftar dalam tabel `daftar_mobil`. 

### Kesimpulan 

Menemukan harga rental mobil terendah yang terdaftar dalam tabel `daftar_mobil` dengan menggunakan fungsi `MIN()` pada kolom `harga_rental`. 

## Menampilkan nilai tertinggi
### Struktur 

```mysql
SELECT MAX(nama_kolom1) AS nama_kolom2 FROM nama_tabel;
```

### Contoh

```mysql
SELECT MAX(harga_rental) AS maximum FROM daftar_mobil;
```

### Hasil

![AGREGASI](max.jpg)

### Analisis 

Mengambil nilai maksimum dari kolom `harga_rental` dari tabel `daftar_mobil` dan memberikan label 'maximum' pada hasilnya. Ini akan mengembalikan satu baris dengan nilai maksimum dari kolom tersebut. Itu bisa digunakan untuk mengetahui mobil mana yang memiliki harga rental tertinggi dalam daftar.

### Kesimpulan 

Digunakan untuk mencari nilai maksimum dari kolom `harga_rental` dalam tabel `daftar_mobil`, yang dapat memberikan informasi tentang mobil mana yang memiliki `harga rental` tertinggi dalam daftar tersebut.

## Menampilkan nilai rata-rata
### Struktur 

```mysql
SELECT AVG(nama_kolom1) AS nama_kolom2 FROM nama_tabel;
```


### Contoh

```mysql
SELECT AVG(harga_rental) AS rerata FROM daftar_mobil;
```

### Hasil

![AGREGASI](avg.jpg)

### Analisis 

Menghitung rata-rata harga rental dari tabel `daftar_mobil` dan memberikan hasilnya dengan nama kolom `rerata`. Ini bermanfaat untuk melihat nilai rata-rata dari harga rental mobil yang terdaftar dalam database.

### Kesimpulan 

Kesimpulannya, memberikan informasi tentang rata-rata harga rental mobil dari tabel `daftar_mobil`, yang dapat digunakan untuk analisis biaya sewa mobil secara keseluruhan.
