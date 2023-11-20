# Lab7web

Nama : Mohammad Azmi Abdussyukur 

NIM  : 312210109

Kelas : TI.22.A1

## DAFTAR ISI <br>
| No | Description | Link |
|-----|------|-----|
|1|Instruksi Praktikum|[Click Here](#instruksi-praktikum)|
|2|Langkah-langkah Praktikum|[Click Here](#langkah-langkah-praktikum)|
|3|Pertanyaan dan Tugas|[Click Here](#pertanyaan-dan-tugas)|


## Instruksi Praktikum
1. Persiapkan text editor misalnya VSCode.
2. Buat folder baru dengan nama lab7_php_dasar pada docroot webserver (htdocs)
3. Ikuti langkah-langkah praktikum yang akan dijelaskan berikutnya.
4. My Local Host Directory http://localhost/lab7_php_dasar/


## Langkah-langkah Praktikum
1. Install XAMPP Unduh XAMPP dari https://www.apachefriends.org/download.html dan pilih versi portable untuk memudahkan proses installasi. Kemudian extract file tersebut, seusikan direktorinya (misal: d:\xampp)

2. Memulai PHP Buat folder lab7_php_dasar pada root directory web server (d:\xampp\htdocs)

3. PHP Dasar Buat file baru dengan nama php_dasar.php pada directory tersebut. Kemudian buat kode seperti berikut :

```
    <!DOCTYPE html>
    <html lang="en">
        <head>
            <meta charset="UTF-8">
            <title>PHP Dasar</title>
        </head>
        <body>
            <h1>Belajar PHP Dasar</h1>
            <?php
            echo "Hello World";
            ?>
        </body>
    </html>
```

<img width="960" alt="helloworld" src="https://github.com/MohAzmii04/Lab7Web/assets/115864496/28ed1627-543c-4784-b4f7-1309804f7dbc">



4. Variable PHP :
```
    <?php
    $nim = "0411500400";
    $nama = 'Abdullah';
    echo "NIM : " . $nim . "<br>";
    echo "Nama : $nama";
    ?>
```

<img width="960" alt="helloworld2" src="https://github.com/MohAzmii04/Lab7Web/assets/115864496/ce6dacc5-0b70-4532-9d69-d9715d22b02c">

5. Predefine Variable $_GET :
```
    <?php
    echo 'Selamat Datang ' . $_GET['nama'];
    ?>
```


<img width="960" alt="Predefine Variable" src="https://github.com/MohAzmii04/Lab7Web/assets/115864496/2bca2aac-ae3a-4605-8f64-8c98dbbf9bc0">

6. Membuat Form :
```
    <!DOCTYPE html>
    <html lang="en">
        <head>
            <meta charset="UTF-8">
            <title>PHP Dasar</title>
        </head>
        <body>
            <h2>Form Input</h2>
            <form method="post">
                <label>Nama: </label>
                <input type="text" name="nama">
                <input type="submit" value="Kirim">
            </form>
            <?php
            echo 'Selamat Datang ' . $_POST['nama'];
            ?>
        </body>
    </html>
```


<img width="960" alt="FormInput" src="https://github.com/MohAzmii04/Lab7Web/assets/115864496/77dce903-7bd0-4199-a21c-5e281fe2d074">


7. Operator :
```
    <?php
    $gaji = 1000000;
    $pajak = 0.1;
    $thp = $gaji - ($gaji*$pajak);
    echo "Gaji sebelum pajak = Rp. $gaji <br>";
    echo "Gaji yang dibawa pulang = Rp. $thp";
    ?>
```


<img width="960" alt="Operator" src="https://github.com/MohAzmii04/Lab7Web/assets/115864496/ae40ba2a-e602-42a1-98b6-91a3c7170a0d">

8. Kondisi IF :
```
    <?php
    $nama_hari = date("l");
    if ($nama_hari == "Sunday") {
        echo "Minggu";
    } elseif ($nama_hari == "Monday") {
        echo "Senin";
    } else {
        echo "Selasa";
    }
    ?>
```


<img width="960" alt="Kondisi IF" src="https://github.com/MohAzmii04/Lab7Web/assets/115864496/9b7cc74b-9de3-4c6d-ad43-1e11282f927a">

9. Kondisi Switch :
```
    <?php
    $nama_hari = date("1");
    switch ($nama_hari) {
    case "Sunday":
        echo "Minggu";
        break;
    case "Monday":
        echo "Senin";
        break;
    case "Tuesday":
        echo "Selasa";
        break;
    default:
        echo "Sabtu";
    ?>
```


![7](https://github.com/syifaaurellia/Lab7web/assets/115867244/41ac2f08-8596-47b8-ac45-dd2424d14bdb)



10. Perulangan for :
```
    <?php
    echo "Perulangan 1 sampai 10 <br />";
    for ($i=1; $i<=10; $i++) {
        echo "Perulangan ke: " . $i . '<br />';
    }
    echo "Perulangan Menurun dari 10 ke 1 <br />";
    for ($i=10; $i>=1; $i--) {
        echo "Perulangan ke: " . $i . '<br />';
    }
    ?>
```


<img width="960" alt="Perulangan For" src="https://github.com/MohAzmii04/Lab7Web/assets/115864496/ed20d123-ccfe-4634-94c2-e5fd1f3785bf">

11. Perulangan while :
```
    <?php
    echo "Perulangan 1 sampai 10 <br />";
    $i=1;
    while ($i<=10) {
        echo "Perulangan ke: " . $i . '<br />';
        $i++;
    }
    ?>
```


<img width="960" alt="Perulangan while" src="https://github.com/MohAzmii04/Lab7Web/assets/115864496/532f3128-1d6d-432f-954f-04e3944fb1ff">

12. Perulangan dowhile :
```
    <?php
    echo "Perulangan 1 sampai 10 <br />";
    $i=1;
    do {
        echo "Perulangan ke: " . $i . '<br />';
        $i++;
    } while ($i<=10);
    ?>
```


![Uploading Perulangan dowhile.png…]()


## Pertanyaan dan Tugas 
> Buatlah program PHP sederhana dengan menggunakan form input yang menampilkan
nama, tanggal lahir dan pekerjaan. Kemudian tampilkan outputnya dengan menghitung
umur berdasarkan inputan tanggal lahir. Dan pilihan pekerjaan dengan gaji yang
berbeda-beda sesuai pilihan pekerjaan.

```
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form Input PHP</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
```

```
<?php
// Fungsi untuk menghitung umur berdasarkan tanggal lahir
function hitungUmur($tanggal_lahir) {
    $today = new DateTime();
    $tanggal_lahir = new DateTime($tanggal_lahir);
    $umur = $today->diff($tanggal_lahir);
    return $umur->y;
}

// Daftar pekerjaan beserta gaji
$pekerjaan_gaji = array(
    'Programmer' => 12000000,
    'Designer' => 8000000,
    'Analyst' => 9000000
);

// Memproses form jika sudah disubmit
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    // Mengambil data dari form
    $nama = $_POST["nama"];
    $tanggal_lahir = $_POST["tanggal_lahir"];
    $pekerjaan = $_POST["pekerjaan"];

    // Validasi data
    if (empty($nama) || empty($tanggal_lahir) || empty($pekerjaan)) {
        echo "Harap lengkapi semua field!";
    } else {
        // Menghitung umur
        $umur = hitungUmur($tanggal_lahir);

        // Menampilkan output
        echo "<h2>Hasil Output</h2>";
        echo "<p><span>Nama         :</span> $nama</p>";
        echo "<p><span>Tanggal Lahir:</span> $tanggal_lahir</p>";
        echo "<p><span>Pekerjaan    :</span> $pekerjaan</p>";
        echo "<p><span>Umur         :</span> $umur tahun</p>";
        echo "<p><span>Gaji         :</span> " . number_format($pekerjaan_gaji[$pekerjaan]) . "</p>";
    }
}
?>
```


```
<h2 class="form">Form Input</h2>
<div class="container">
    <form method="post" action="<?php echo htmlspecialchars($_SERVER["PHP_SELF"]);?>">
        <div class="input-group">
            <label for="nama">Nama </label>
            <input type="text" name="nama">
        </div>
        <div class="input-group">
            <label for="tanggal_lahir">Tanggal Lahir </label>
            <input type="date" name="tanggal_lahir">
        </div>
        <div class="input-group">
            <label for="pekerjaan">Pekerjaan </label>
            <select name="pekerjaan">
                <option value="Programmer">Programmer</option>
                <option value="Designer">Designer</option>
                <option value="Analyst">Analyst</option>
            </select>
        </div>
        
        <input type="submit" name="submit" value="Submit" class="btn">
    </form>
</div>

</body>
</html>
```



https://github.com/MohAzmii04/Lab7Web/assets/115867244/1a104ad5-1190-43b2-918f-3efdfe2d7e69


## Sekian, Terima Kasih 
