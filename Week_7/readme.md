<div align="center">
  <h1 style="text-align: center;font-weight: bold">Laporan Praktikum<br>Workshop Administrasi Jaringan</h1>
  <h4 style="text-align: center;">Dosen Pengampu : Dr. Ferry Astika Saputra, S.T., M.Sc.</h4>
</div>
<br />
<div align="center">
  <img src="./img/pens.png" alt="Logo PENS">
  <h3 style="text-align: center;">Disusun Oleh :</h3>
  <p style="text-align: center;">
    <strong>Calvin Raditya Sandy Winarto</strong><br>
    <strong>3123500009</strong><br>
    <strong>2 D3 Teknik Informatika A</strong>
  </p>

<h3 style="text-align: center;line-height: 1.5">Politeknik Elektronika Negeri Surabaya<br>Departemen Teknik Informatika Dan Komputer<br>Program Studi Teknik Informatika<br>2025/2026</h3>
  <hr>
</div>
<br>

## Syarat & Ketentuan
Memerlukan instalasi WinBox untuk melakukan pengujian hubungan antar jaringan.

#### Layer Network

Percobaan ini bertujuan menghubungkan perangkat MikroTik antar kelompok agar laptop di masing-masing LAN bisa saling ping. Setiap kelompok menggunakan IP 10.252.108.5x, di mana x adalah nomor kelompok. Karena kelompok saya adalah kelompok 7, maka IP-nya 10.252.108.57.

Setelah MikroTik terhubung ke jaringan LAN melalui kabel, pengujian koneksi dilakukan dengan perintah ping via Command Prompt di Windows.

### Ping ke device di kelompok lain

Setelah berhasil ping antar IP MikroTik, tahap selanjutnya adalah memastikan konektivitas antar perangkat di jaringan. Laptop yang terhubung ke LAN otomatis mendapat IP 192.168.x.0/24, di mana x adalah nomor kelompok. Kelompok saya menggunakan 192.168.4.0/24 dengan gateway 10.252.108.57.

Tujuan tahap ini adalah agar laptop dapat ping ke IP jaringan kelompok lain, seperti 192.168.1.0, 192.168.2.0, 192.168.3.0, dan seterusnya.

### 1. Menambahkan IP device pada kelompok lain beserta IP gateaway-nya
Langkah pertama yang perlu dilakukan adalah menambahkan alamat IP jaringan dari kelompok lain beserta gateway-nya secara manual. Gateway yang digunakan adalah alamat IP MikroTik milik masing-masing kelompok.

Proses ini dilakukan agar perangkat dalam jaringan dapat saling terhubung dan melakukan komunikasi lintas kelompok. Untuk menambahkan IP dan gateway secara statis, buka aplikasi WinBox, lalu masuk ke menu Terminal dan jalankan perintah yang sesuai. Perintah ini akan mengarahkan lalu lintas menuju jaringan kelompok lain melalui gateway yang telah ditentukan.

`/ip route add dst-address=192.168.x.0/24 gateaway=10.252.108.5x`

Dimana x adalah nomer kelompok, dst-address adalah destination address dan gateaway adalah IP dari MikroTik-nya.

 [![img-1](img/1.jpg)](img)

Jika sudah ditambahkan semua seperti di atas, maka bisa di cek menggunakan Route List di WinBox dan seharusnya akan muncul seperti ini

 [![img-1](img/2.jpg)](img)

### 2. Test ping ke device kelompok lain

Setelah tahap pertama sudah selesai, maka bisa lakukan test ping seperti di bawah ini

 [![img-1](img/3.jpg)](img)
 [![img-1](img/4.jpg)](img)

Jika test ping seperti di atas sudah berhasil, dan status dari setiap test ping kosong, maka koneksi antar device beda kelompok sudah berhasil dilakukan.