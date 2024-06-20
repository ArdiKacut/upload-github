# Instalasi MysQL

## Menggunakan termux

1. Buka Aplikasi Termux
2. Ketik "termux-setup-storage"
3. Ketik izinkan/allow access
4. Lakukan update atau upgrade paket. Ketik "pkg update && upgrade -y"
5. jika ada informasi untuk melanjutkan instalasi ketik "y"
6. Hasil aplikasi mariadb dengan mengetik "pkg install mariadb"
7. Ketika proses berhenti dan ada pilihan "y/n" ketik saja "y" untuk melanjutkan proses penginstalan
8. ketik "mysqld_safe" untuk memberi keamanan.
9. Ketik CNTRL+Z agar bisa ngesave datanya.
## Referensi Link Vidio YouTube 

https://youtu.be/dmhJQ4zs_WY?si=yLCNgx8ZNHbEbFDx
## QUERY

Perintah `mysql -u root` digunakan untuk masuk ke client MySQL dengan menggunakan nama pengguna "root". Ini akan memungkinkan Anda untuk terhubung ke server MySQL dan mengeksekusi perintah SQL atau mengelola basis data yang terhubung dengan akun "root".

## HASIL

![mysql -u root](mysql_-u_root.jpg)

## ANALISIS

Perintah mysql -u root digunakan untuk mengakses server MySQL menggunakan akun pengguna "root" dari baris perintah (command line). Analisis dari perintah ini akan tergantung pada apa yang ingin Anda ketahui atau lakukan setelah masuk ke dalam server MySQL dengan akun "root".

## Kesimpulan 

Perintah "mysql -u root" digunakan untuk masuk ke dalam server database MySQL menggunakan pengguna (user) "root". Dengan demikian, Anda akan dapat mengakses dan mengelola database MySQL menggunakan hak akses penuh yang dimiliki oleh pengguna root.

# Tipe Data
## Angka

1. **INT** (Integer)
   - Menyimpan angka bulat.
   - Rentang: -2,147,483,648 hingga 2,147,483,647.
   - Versi: `TINYINT`, `SMALLINT`, `MEDIUMINT`, `INT`, `BIGINT`.

2. **FLOAT** (Floating Point)
   - Menyimpan angka dengan titik desimal.
   - Rentang: Sekitar -3.402823466E+38 hingga 3.402823466E+38.
   - Presisi: Sekitar 7 digit.

3. **DOUBLE** (Double Precision Floating Point)
   - Menyimpan angka dengan titik desimal yang lebih presisi dibandingkan FLOAT.
   - Rentang: Sekitar -1.7976931348623157E+308 hingga 1.7976931348623157E+308.
   - Presisi: Sekitar 15 digit.

4. **DECIMAL** (Fixed Point)
   - Menyimpan angka desimal dengan presisi yang ditentukan.
   - Format: `DECIMAL(M, D)`, di mana `M` adalah total digit dan `D` adalah digit di sebelah kanan desimal.
   - Digunakan untuk keuangan dan situasi lain yang membutuhkan presisi tinggi.

5. **BIT**
   - Menyimpan nilai biner (0 atau 1).
   - Bisa menyimpan angka biner dengan panjang tertentu (1 hingga 64 bit).

![angka](contoh_angka.jpg)

Dalam contoh ini, INT, FLOAT, DOUBLE, DECIMAL dan BIT adalah tipe data angka yang digunakan untuk kolom-kolom tertentu dalam tabel.

## Teks

1. **CHAR(M)**:
   - Tipe data ini digunakan untuk menyimpan string dengan panjang tetap. Jika panjang string lebih pendek dari yang ditentukan, sisanya akan diisi dengan spasi.
   - Contoh: `CHAR(10)`

2. **VARCHAR(M)**:
   - Tipe data ini digunakan untuk menyimpan string dengan panjang variabel. Panjang maksimum string ditentukan oleh nilai M.
   - Contoh: `VARCHAR(255)`

3. **TEXT**:
   - Tipe data ini digunakan untuk menyimpan string panjang. Panjang maksimum data yang bisa disimpan adalah 65,535 karakter.
   - Contoh: `TEXT`

![text](contoh_teks.jpg)

Dalam contoh ini, CHAR, VARCHAR, dan TEXT adalah tipe data teks yang digunakan untuk kolom-kolom tertentu dalam tabel.

## Tanggal

1. **DATE**: Menyimpan tanggal dalam format `YYYY-MM-DD`. Contoh: `2023-06-20`.

2. **TIME**: Menyimpan waktu dalam format `HH:MM:SS`. Contoh: `14:30:00`.

3. **DATETIME**: Menyimpan kombinasi tanggal dan waktu dalam format `YYYY-MM-DD HH:MM:SS`. Contoh: `2023-06-20 14:30:00`.

4. **TIMESTAMP**: Menyimpan kombinasi tanggal dan waktu dalam format `YYYY-MM-DD HH:MM:SS`, tetapi juga mencatat waktu dalam UTC dan memperbarui secara otomatis dengan waktu saat ini saat ada perubahan pada baris tersebut (jika tidak diatur secara eksplisit). Contoh: `2023-06-20 14:30:00`.

5. **YEAR**: Menyimpan tahun dalam format `YYYY`. Contoh: `2023`.

![tanggal](contoh_tanggal.jpg)

Dalam contoh ini, DATE, TIME, DATETIME, TIMESTAMP, dan YEAR adalah tipe data yang digunakan untuk kolom-kolom tertentu dalam tabel untuk menyimpan informasi tanggal dan waktu.

## Boolean

- tipe data boolean digunakan untuk menyimpan nilai kebenaran, yaitu True (benar) atau False (salah). Tipe data boolean umumnya digunakan dalam kondisi percabangan dan pengambilan keputusan.

## Tipe Data Pilihan
### Enum

Tipe data ENUM (enumeration) dalam basis data adalah tipe data yang digunakan untuk mendefinisikan kumpulan nilai tetap yang dapat diidentifikasi oleh nama. Setiap nilai dalam ENUM diberi label dan harus dipilih dari daftar nilai yang telah ditentukan.

### Set

MySQL memiliki tipe data SET yang memungkinkan Anda untuk menyimpan himpunan nilai tetap yang telah ditentukan sebelumnya. Namun, penggunaannya harus dipertimbangkan dengan hati-hati karena dapat menyulitkan pengelolaan dan perubahan struktur data
# Insert
## Insert 1 Data
### Struktur

```mysql
insert into nama_table
    values ("nilai1","nilai2","nilai3","nilai4");
```

### Contoh

```mysql
insert into karyawan
   values ("1","ardiansya","ardi","0895333405540");
```

### Hasil

![insert 1 data](insert1_data.jpg)

### Analisis 

- `INSERT INTO karyawan` : Ini menentukan nama tabel dimana data akan dimasukkan, dalam hal ini, "karyawan".

- `VALUES ("1", "ardiansya", "ardi", "0895333405540")`: Ini menentukan nilai yang akan dimasukkan ke dalam setiap kolom tabel. Nilai yang diberikan adalah untuk kolom sesuai urutan kemunculannya di tabel.

- "1" untuk kolom pertama,
- "ardiansya" untuk kolom kedua,
- "ardi" untuk kolom ketiga,
- "0895333405540" untuk kolom keempat.

Akan menyisipkan baris baru ke dalam tabel "karyawan" dengan nilai yang ditentukan.

### Kesimpulan 

Kesimpulan dari perintah `INSERT INTO karyawan VALUES ("1", "ardiansya", "ardi", "0895333405540");` adalah data karyawan dengan ID 1, nama "ardiansya", nama panggilan "ardi", dan nomor telepon "0895333405540" telah dimasukkan ke dalam tabel karyawan.

## Insert >1 Data
### Struktur

```mysql
insert into nama_table 
     values ("nilai1","nilai2","nilai3","nilai4"),
("nilai1","nilai2","nilai3","nilai4"),
("nilai1","nilai2","nilai3","nilai4");
```

### Contoh

```mysql
insert into karyawan
    values ("2","farhan","far","08431279465"),
("3","fadhilamir","fadil","08846379542"),
("4","alfazari","raihan","08613452764");
```

### Hasil

![insert lebih besar 1 data](insert_lebih_besar1.jpg)

### Analisis

- Perintah: `INSERT INTO karyawan`
- Data yang dimasukkan:
  - Set 1: ("2654", "farhan", "far", "089753627153")
  - Set 2: ("2541", "raihan", "han", "08527383654")
  - Set 3: ("2331", "fadhil", "fadil", "08964321759")
- Tabel Tujuan: `karyawan`
- Kolom yang diisi:
  - `id_karyawan`: Nilai dari kolom ini adalah "2654", "2541", dan "2331" untuk masing-masing set data.
  - `nama_depan`: Nilai dari kolom ini adalah "farhan", "raihan", dan "fadhil" untuk masing-masing set data.
  - `nama_belakang`: Nilai dari kolom ini adalah "far", "han", dan "fadil" untuk masing-masing set data.
  - `no_telepon`: Nilai dari kolom ini adalah "089753627153", "08527383654", dan "08964321759" untuk masing-masing set data.

### Kesimpulan

Adalah bahwa query tersebut berhasil memasukkan tiga baris data baru ke dalam tabel karyawan dengan informasi yang terperinci mengenai setiap karyawan, termasuk ID, nama depan, nama belakang, dan nomor telepon mereka.

## Menyebut Kolom
### Struktur 

```mysql
insert into nama_table
    (kolom1,kolom2) values ("nilai1","nilai2");
```
### Contoh

```mysql
insert into karyawan
(nama_asli,nis_karyawan) values ("agus","5");
```

### Hasil

![[menyebut_kolom.jpg]]

### Analisis

- `INSERT INTO karyawan`: Ini adalah pernyataan SQL yang menunjukkan bahwa kita ingin menyisipkan data ke dalam tabel bernama `karyawan`.

- `(nama_asli, nis_karyawan)`: Bagian ini menentukan kolom-kolom di mana data akan dimasukkan. Dalam hal ini, kolom yang ditentukan adalah `nama_asli` dan `nis_karyawan`.

- `VALUES ("agus", "5")`: Ini adalah nilai yang ingin dimasukkan ke dalam kolom yang telah ditentukan sebelumnya. `"agus"` akan dimasukkan ke dalam kolom `nama_asli`, dan `"5"` akan dimasukkan ke dalam kolom `nis_karyawan`.

Jadi, secara keseluruhan, query ini akan menambahkan sebuah baris baru ke dalam tabel `karyawan` dengan nilai `"agus"` untuk kolom `nama_asli` dan nilai `"5"` untuk kolom `nis_karyawan`.

### Kesimpulan

Query ini merupakan sebuah perintah SQL untuk memasukkan data baru ke dalam tabel `karyawan`. Data yang dimasukkan adalah nama_asli "agus" dan nis_karyawan "5".

# Update (data)
## Struktur 

```mysql
update nama_tabel set nama_kolom1"nilai1" where nama_kolom2"nilai2;
```

## Contoh 

```mysql
update karyawan set no_telp="086451334044" where nis_karyawan="4";
```

## Hasil

![update baris](update_baris.jpg)

## Analisis 

- `UPDATE karyawan`: Bagian ini menentukan tabel yang akan diperbarui, yaitu "karyawan" dalam hal ini.

- `SET no_telp="086451334044"`: Bagian ini menetapkan nilai kolom "no_telp" menjadi "086451334044" untuk record yang sesuai dengan kondisi yang ditentukan pada klausa WHERE.

- `WHERE nis_karyawan="4"`: Bagian ini menentukan kondisi yang harus dipenuhi oleh catatan agar dapat diperbarui. Dalam hal ini, memperbarui record dimana nilai pada kolom "nis_karyawan" sama dengan "4".

## Kesimpulan 

sebuah perintah SQL untuk mengubah nilai kolom nama_asli menjadi "ardiansya" di dalam tabel karyawan dimana nis_karyawan memiliki nilai "4". Kesimpulannya, perintah tersebut bertujuan untuk memperbarui data karyawan dengan nis_karyawan tertentu dengan no_telp "086451334044".

# Delete (Hapus baris data)
## Struktur

```mysql
DELETE FROM nama_tabel WHERE nama_kolom"nilai";
```

## Contoh

```mysql
DELETE FROM karyawan WHERE nis_karyawan="3";
```

## Hasil

![delete nama tabel](delete_nama_tabel.jpg)

## Analisis

**Perintah:** `DELETE FROM karyawan`
- Ini adalah perintah untuk menghapus data dari tabel "karyawan".

**Kondisi WHERE:** `nis_karyawan=3
- Ini adalah klausa WHERE yang menentukan kriteria untuk baris-baris yang akan dihapus. Dalam hal ini, baris akan dihapus jika nilai kolom "nis_karyawan" sama dengan 3.

**Tabel:** `karyawan`
- Ini adalah nama tabel yang akan dihapus barisnya.

## Kesimpulan

Perintah SQL di atas menghapus baris data dari tabel "karyawan" di mana nilai kolom "nis_karyawan" sama dengan "3". Kesimpulannya, program ini digunakan untuk menghapus informasi karyawan dengan nomor identitas "3" dari basis data.

# Hapus Tabel
## Struktur

```mysql
drop table nama_table;
```

## Contoh

```mysql
drop table pelanggan;
```

## Hasil

![hapus table](hapus_tabel.jpg)

## Analisis 

"drop table pelanggan;" adalah tentang perintah SQL untuk menghapus tabel bernama "pelanggan" dari database. 

1. **Drop Table**: Ini adalah perintah SQL yang digunakan untuk menghapus tabel dari database.
  
2. **Pelanggan**: Ini adalah nama tabel yang akan dihapus.

Jadi, secara keseluruhan, query tersebut akan menghapus tabel bernama "pelanggan" dari database yang sedang digunakan. Dengan melakukan ini, semua data yang ada dalam tabel tersebut akan dihapus dan struktur tabelnya akan dihapus dari database.

## Kesimpulan 

Query "DROP TABLE pelanggan;" akan menghapus tabel bernama "pelanggan" dari database. Ini adalah perintah SQL yang digunakan untuk menghapus tabel beserta semua data yang terkait dengan tabel tersebut dari database. Proses ini bersifat permanen, artinya setelah tabel dihapus, data yang ada di dalamnya tidak dapat dikembalikan lagi kecuali jika backup telah dibuat sebelumnya.
