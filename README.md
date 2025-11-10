# Lab7Web.

    Nama: Burhan Isnain Nur Huda
    NIM: 312410226
    Kelas: TI.24.A.2
    Mata Kuliah: Pemograman Web1

# Code

    <html lang="en">
    <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form Input Data Diri</title>
    </head>
     <body>
    <h2>Form Input Data Diri</h2>
     <form method="post">
        <label>Nama:</label>
        <input type="text" name="nama" required>
        <br><br>
        
        <label>Tanggal Lahir:</label>
        <input type="date" name="tanggal_lahir" required>
        <br><br>
        
        <label>Pekerjaan:</label>
        <select name="pekerjaan" required>
            <option value="">-- Pilih Pekerjaan --</option>
            <option value="Software Engineer">Software Engineer</option>
            <option value="Data Analyst">Data Analyst</option>
            <option value="Web Developer">Web Developer</option>
        </select>
        <br><br>
        
        <input type="submit" value="Kirim">
    </form>

    <?php
    if ($_SERVER["REQUEST_METHOD"] == "POST") {
        // Mengambil data dari form
        $nama = $_POST['nama'];
        $tanggal_lahir = $_POST['tanggal_lahir'];
        $pekerjaan = $_POST['pekerjaan'];
        
        // Menghitung umur
        $tgl_lahir = new DateTime($tanggal_lahir);
        $today = new DateTime();
        $umur = $today->diff($tgl_lahir)->y;
        
        // Menentukan gaji berdasarkan pekerjaan
        $gaji = 0;
        switch ($pekerjaan) {
            case 'Software Engineer':
                $gaji = 15000000;
                break;
            case 'Data Analyst':
                $gaji = 12000000;
                break;
            case 'Web Developer':
                $gaji = 10000000;
                break;
            default:
                $gaji = 0;
        }
        
        echo "<h3>Hasil Data Diri:</h3>";
        echo "Nama: " . $nama . "<br>";
        echo "Tanggal Lahir: " . $tanggal_lahir . "<br>";
        echo "Umur: " . $umur . " tahun<br>";
        echo "Pekerjaan: " . $pekerjaan . "<br>";
        echo "Gaji: Rp " . number_format($gaji, 0, ',', '.') . "<br>";
    }
    ?>
    </body>
    </html>

# Screenshoot

![Gambar WhatsApp 2025-11-10 pukul 16 14 24_6292d190](https://github.com/user-attachments/assets/28b7d8fc-8e0a-4719-a51d-8a86f3ec9945)
![Gambar WhatsApp 2025-11-10 pukul 16 15 21_0d9c17dc](https://github.com/user-attachments/assets/a3c386fc-9fa6-4a5e-ba94-28a2f3edb3cc)
![Gambar WhatsApp 2025-11-10 pukul 16 17 32_68f63c6c](https://github.com/user-attachments/assets/617fabec-50d3-43fd-a1e7-28b0802303b1)

# Style CSS

![Gambar WhatsApp 2025-11-10 pukul 15 44 04_1ce39e15](https://github.com/user-attachments/assets/7dba8bd0-334b-4813-815b-0f7438648568)
![Gambar WhatsApp 2025-11-10 pukul 15 45 43_549c0652](https://github.com/user-attachments/assets/835c224f-6d4f-4d77-b890-b94d255d658f)




