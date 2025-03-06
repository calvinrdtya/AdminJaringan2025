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
    <strong>2 D3 IT A</strong>
  </p>

<h3 style="text-align: center;line-height: 1.5">Politeknik Elektronika Negeri Surabaya<br>Departemen Teknik Informatika Dan Komputer<br>Program Studi Teknik Informatika<br>2025/2026</h3>
  <hr>
</div>
<br>

# Instalasi Sistem Operasi & Manajemen Paket  

## 1. Instalasi Sistem Operasi  

### a. Distribusi Linux dan FreeBSD  
- Distribusi Linux dan FreeBSD memiliki prosedur instalasi yang cukup sederhana, terutama untuk instalasi dasar menggunakan GUI yang intuitif.

### b. Instalasi Fisik vs. Virtual  
- **Mesin Fisik**: Booting dapat dilakukan melalui **CD, DVD, atau USB drive**.  
- **Mesin Virtual**: Proses booting dilakukan melalui **file ISO**.  
- Instalasi OS dasar biasanya mudah dilakukan dengan bantuan aplikasi GUI.  

### c. Instalasi Jaringan  
Ketika harus menginstal sistem operasi pada banyak komputer, **instalasi melalui jaringan** lebih efisien dibandingkan menggunakan media fisik.  
- Menggunakan protokol **DHCP dan TFTP** untuk booting tanpa media fisik.  
- File instalasi diunduh dari server melalui **HTTP, FTP, atau NFS**.  

### d. Metode PXE (Preboot eXecution Environment)  
- PXE memungkinkan instalasi otomatis tanpa memerlukan media fisik.  
- Standar dari **Intel** yang memungkinkan boot dari antarmuka jaringan.  
- **Keuntungan PXE**:  
  - Booting dari satu server untuk semua PC yang mendukung PXE.  
  - Tidak memerlukan driver khusus untuk setiap kartu jaringan.  


## 2. Sistem Manajemen Paket Linux  

### a. Format Paket 

Format paket yang umum digunakan dalam distribusi Linux:  

| **Format** | **Digunakan oleh** |
|-----------|---------------------|
| **RPM**   | Red Hat, CentOS, SUSE, Amazon Linux |
| **DEB**   | Debian, Ubuntu |

Meskipun memiliki perbedaan format, kedua paket ini secara fungsional sangat mirip.

### b. Alat Manajemen Paket  
#### **Alat Tingkat Rendah**  
- **rpm** → untuk paket **RPM**.  
- **dpkg** → untuk paket **.deb**.  

#### **Alat Manajemen Paket Tingkat Tinggi** 

Memungkinkan pengguna untuk menginstal, menghapus, dan memperbarui paket dengan lebih mudah.  

- **yum** → Digunakan untuk sistem berbasis RPM.  
- **APT (Advanced Package Tool)** → Digunakan untuk sistem berbasis Debian.  

| **Alat APT**       | **Fungsi** |
|---------------------|-----------|
| **apt-get**        | Instalasi, pembaruan, dan penghapusan paket |
| **apt-cache**      | Pencarian dan query paket APT |
| **apt-file**       | Mencari file dalam paket |
| **apt-show-versions** | Menampilkan versi paket |
| **aptitude**       | Antarmuka manajemen paket tingkat tinggi |
| **apt-mirror**     | Mencerminkan repositori paket |

---

## 3. Repositori Paket  
Repositori adalah sumber utama paket perangkat lunak untuk sistem operasi berbasis Linux.  

- **Release** → Snapshot konsisten dari seluruh paket.  
- **Component** → Subset perangkat lunak dalam sebuah release.  
- **Architecture** → Kompatibilitas perangkat keras dengan sistem.  

---

## 4. Lokalisasi dan Konfigurasi Perangkat Lunak  
Menyesuaikan sistem dengan lingkungan lokal (atau cloud) adalah langkah penting dalam administrasi sistem.  

- **Pendekatan yang terstruktur dan dapat direproduksi sangat penting** untuk menghindari sistem yang sulit dipulihkan.  
- Gunakan metode otomatisasi untuk **memudahkan konfigurasi ulang sistem** jika terjadi kegagalan.  

---

Dokumentasi ini memberikan gambaran lengkap tentang **instalasi sistem operasi dan manajemen paket** dalam distribusi Linux dan FreeBSD. Otomasi dan skalabilitas adalah kunci untuk mengelola sistem dalam skala
