# Praktikum 5 : Javascript
### Membuat Dasar Pemrograman Di Javascript "Hello World" , Operasi dasar aritmatika, Pembuatan Form, HTML DOM Pilihan menggunakan checkBox dengan perhitungan otomatis

|                |                    |
| ------------------ | ------------------ |
|      _Nama_    | Dwi Okta Ramadhani |
|      _NIM_     |      312410056     |
|     _Kelas_    |      TI.24.A1      |
|  _Mata Kuliah_ | Bahasa Pemrograman Web 1 |

## Deskripsi
Praktikum ini bertujuan untuk mengenalkan dasar-dasar pemrograman JavaScript di dalam halaman web.
Melalui berbagai contoh sederhana, saya belajar bagaimana JavaScript berinteraksi dengan elemen HTML untuk menampilkan teks, melakukan operasi logika dan aritmatika, mengelola input dari pengguna, serta memanipulasi elemen HTML secara dinamis menggunakan HTML DOM (Document Object Model).

## Tujuan Praktikum                                                         
|                |                     
| ------------------ | 
| 1.	Memahami cara kerja dasar JavaScript pada halaman HTML.           |
| 2.	Menggunakan JavaScript untuk menampilkan data dan pesan ke layar. |
| 3.	Mempelajari operasi dasar seperti aritmatika serta seleksi kondisi (if-else & switch).                                                       |
| 4.    Menggunakan form untuk mengambil dan mengolah input dari pengguna.|
| 5. 	Memahami dasar manipulasi HTML DOM, termasuk penerapan event dan  | | checkbox dengan perhitungan otomatis.                                   |

## Langkah-Langkah Praktikum

|                |                     
| ------------------ | 
| Program Pertama digunakan untuk menampilkan teks Hello World menggunakan document.write() dan console.log().                                       | 

**INPUT**
```
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Mengenal JavaScript</title>
</head>
<body>
    <h1>Pengenalan JavaScript</h1>
    <h3>Contoh document.write dan console.log</h3>
    <script>
        document.write("Hello World");
        console.log("Hello World");
    </script>
</body>
</html>

Javascrip Dasar
Pemakaian Alert sebagai property window.
<html>
<head>
    <title>alert box</title>
</head>
<body>
    <script language="javascript">
    <!--
        window.alert("ini merupakan pesan untuk anda");
    //-->
    </script>
</body>
</html>

Pemakaian method dalam objek
<html>
<head>
    <title>skrip javascript</title>
</head>
<body>
    percobaan memakai javascript:<br>
    <script language="javascript">
    <!--
        document.write("selamat mencoba javascript<br>");
        document.write("semoga sukses!");
    //-->
    </script>
</body>
</html>

Pemakaian Prompt
<html>
<head>
    <title>pemasukan data</title>
</head>
<body>
    <script language="javascript">
    <!--
        var nama = prompt("siapa nama anda?", "masukkan nama anda");
        document.write("hai, " + nama);
    //-->
    </script>
</body>
</html>

Pembuatan fungsi dan cara pemanggilannya
<html>
<head>
    <title>contoh program javascript</title>
    <script language="javascript">
        function pesan() {
            alert("memanggil javascript lewat body onload");
        }
    </script>
</head>
<body onload="pesan()">
</body>
</html>
```

**OUTPUT**
-----


|                |                     
| ------------------|
| Program Kedua Dasar Pemrograman di Javascript Operasi dasar aritmatika |                       

**INPUT**
```
<html>
<head>
    <title>contoh program javascript</title>
    <script language="javascript">
        function test(val1, val2) {
            document.write("<br>perkalian : val1 * val2 = " + (val1 * val2) + "<br>");
            document.write("pembagian : val1 / val2 = " + (val1 / val2) + "<br>");
            document.write("penjumlahan : val1 + val2 = " + (val1 + val2) + "<br>");
            document.write("pengurangan : val1 - val2 = " + (val1 - val2) + "<br>");
            document.write("modulus : val1 % val2 = " + (val1 % val2) + "<br>");
        }
    </script>
</head>
<body>
    <input type="button" name="button1" value="arithmetic" onclick="test(9,4)">
</body>
</html>

Seleksi kondisi (if..else)
<html>
<head>
    <title>contoh if-else</title>
</head>
<body>
    <script language="javascript">
    <!--
        var nilai = prompt("nilai (0-100): ", 0);
        var hasil = "";
        if (nilai >= 60)
            hasil = "lulus";
        else
            hasil = "tidak lulus";
        document.write("hasil: " + hasil);
    //-->
    </script>
</body>
</html>

Penggunaan operator switch untuk seleksi kondisi
<html>
<head>
    <title>contoh program javascript</title>
    <script language="javascript">
        function test() {
            var val1 = window.prompt("input nilai (1-5):");
            switch (val1) {
                case "1":
                    document.write("bilangan satu");
                    break;
                case "2":
                    document.write("bilangan dua");
                    break;
                case "3":
                    document.write("bilangan tiga");
                    break;
                case "4":
                    document.write("bilangan empat");
                    break;
                case "5":
                    document.write("bilangan lima");
                    break;
                default:
                    document.write("bilangan lainnya");
            }
        }
    </script>
</head>
<body>
    <input type="button" name="button1" value="switch" onclick="test()">
</body>
</html>
```

**OUTPUT**
-----


|                |                     
| ------------------|
| Program Kedua Dasar Pemrograman di Javascript Operasi dasar aritmatika | 

|                |                     
| ------------------ | 
|Program Ketiga Pembuatan Form 
|Form Input Mengambil input angka dan menampilkan hasil ganjil/genap secara otomatis. |

**INPUT**
```
<html>
<head>
    <title>contoh program javascript</title>
    <script language="javascript">
        function test() {
            var val1 = document.kirim.T1.value;
            if (val1 % 2 == 0)
                document.kirim.T2.value = "bilangan genap";
            else
                document.kirim.T2.value = "bilangan ganjil";
        }
    </script>
</head>
<body>
    <form method="POST" name="kirim">
        <p>BIL <input type="text" name="T1" size="20">
        MERUPAKAN BIL <input type="text" name="T2" size="20"></p>
        <p><input type="button" value="TEBAK" name="B1" onclick="test()"></p>
    </form>
</body>
</html>

Form Button.
<html>
<head>
    <title>objek document</title>
</head>
<body>
    <script language="javascript">
    <!--
        function ubahWarnaLB(warna) {
            document.bgColor = warna;
        }
        function ubahWarnaLD(warna) {
            document.fgColor = warna;
        }
    //-->
    </script>

    <h1>tes</h1>
    <form>
        <input type="button" value="Latar Belakang Hijau" onClick="ubahWarnaLB('GREEN')">
        <input type="button" value="Latar Belakang Putih" onClick="ubahWarnaLB('WHITE')">
        <input type="button" value="Teks Kuning" onClick="ubahWarnaLD('YELLOW')">
        <input type="button" value="Teks Biru" onClick="ubahWarnaLD('BLUE')">
    </form>

    <script language="javascript">
    <!--
        document.write("Dimodifikasi terakhir pada " + document.lastModified);
    //-->
    </script>
</body>
</html>
```

**OUTPUT**
-----

Program KeEmpat HTML DOM
CheckBox dengan Perhitungan Otomatis
Membuat form daftar menu dengan harga yang otomatis dijumlahkan saat checkbox dipilih.

**INPUT**
```
HTML DOM
Pilihan menggunakan checkBox dengan perhitungan otomatis
<html>
<head>
    <title>Daftar Menu</title>
    <script>
        function hitung(ele) {
            var total = document.getElementById('total').value;
            total = (total ? parseInt(total) : 0);
            var harga = 0;

            if (ele.checked) {
                harga = ele.value;
                total += parseInt(harga);
            } else {
                harga = ele.value;
                if (total > 0) {
                    total -= parseInt(harga);
                }
            }
            document.getElementById('total').value = total;
        }
    </script>
</head>
<body>
    <h1>Daftar Menu Makanan</h1>
    <label><input type="checkbox" value="5000" id="menu1" onclick="hitung(this);" /> Ayam Goreng Rp. 5.000</label><br />
    <label><input type="checkbox" value="500" id="menu2" onclick="hitung(this);" /> Tempe Goreng Rp. 500</label><br />
    <label><input type="checkbox" value="2500" id="menu3" onclick="hitung(this);" /> Telur Dadar Rp. 2.500</label><hr />
    <strong>Total Bayar: Rp. <input id="total" type="text" /></strong>
</body>
</html>
```

**OUTPUT**
-----


## Kesimpulan
Dari praktikum ini, saya belajar dasar-dasar pemrograman JavaScript di dalam halaman web, mulai dari menampilkan teks sederhana hingga memanipulasi elemen HTML secara dinamis.
Melalui berbagai contoh seperti alert, prompt, operasi aritmatika, seleksi kondisi, form input, dan HTML DOM, saya memahami bahwa JavaScript sangat berperan penting dalam membuat halaman web menjadi interaktif dan dinamis.
Praktikum ini juga memberikan pemahaman awal mengenai bagaimana logika pemrograman, fungsi, dan event handling diterapkan langsung di dalam struktur HTML untuk menciptakan pengalaman pengguna yang lebih baik.

## Terima Kasih

