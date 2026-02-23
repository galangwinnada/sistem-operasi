# PERTEMUAN 2

<h4> Nama : Galang Satriyo Anorrogo Winnada<h4>
<h4> NIM : 254107020231<h4>
<h4> Kelas : TI 1-H<h4>

## PRAKTIKUM 2.1 

### LATIHAN 2.1 
1. jumlah CPU(S) : 1
   core(S) per socket : 1
   thread(s) per core : 1
2. Total RAM : 16
3. Total wap :2.061

### LATIHAN 2.2
1. PERANGKAT PCI : Erhernet controller (0200)
    Vendor : Device ID (8086:001e)
    kernel drives in use : e1000
    kernel modules : e1000
   # FUNGSI
    1. VENDOR : Device ID (8086:001e)
    identitas ini merujuk pada Intel 82540EM Gigabit Ethernet Contoller.
        8086 : Adalah kode heksadesimal resmi untuk intel (diambil dari prosesor legendaris intel 8086)
        001e : Adalah model spesifik kartu jaringan gigabit yang sangat populer. Perangkat sering muncul di mesin virtual (seperti VirtualBox atau VMware) karena kompatibilitasnya yang sangat tinggi dengan hampir semua sistem operasi
    2. Fungsi Utama (Etthernet Controller - 0200)
    sebagai pengontrol Ethernet, perngkat ini berfungsi sebagai pinttu gerbang data antara komputer anda dan jaringan lokal (LAN) atau internet. Tugas utamanya meliputi:
        Enkapsulasi Data: Membungkus data dari sistem operasi ke dalam frame Ethernet agar bisa dikirim melalui kabel
        Manajemen Kecepatan : Mendukung teknologi gigabit, yNG Mmpu mentranfer data hingga 1 Gbps (1000Mbps).
        CSMA?CD: mengatur lalu lintas data untuk mencegah tabrakan paket (collision) di jaringan kabel
    3. Peran Kernel Driver & Module (e1000)
    driver e1000 adalah perangkat lunak di dalam kerne; (inti sistem operasi) yang bertugas memberikan langsung ke perngkat keras 
        Efisiensi : Driver ini sangat stabil dan mendukung fitur-fitur seperti Checksum Offloading (memindahkan beban perhitungan verifikasi data dari CPU ke kartu jaringan), sehingga performa komputer tetap ringan saat mengunduh data besar.
        Komatibilitas: karena perangkat sangat standar, driver e1000 biasanya sudah terpasang secara otomaatis di hampit semua distro Linuk dan Windows tanpa perlu instalasi manual

### LATIHAN 2.3
1. Dalam sistem operasi berbasis Unix/Linux, segala sesuatu dianggap sebagai fi;e, termasuk perangkat keras (hardware). Saat anda menjalankan perintah ls -1 pada direktori /dev, anda akan melihat karakter khusus di kolom pertama izin akses (permissions) yang mebedakan jenis perngkat tersebut.
    # Perbedaan utama antara Block Device dan Character Device
    1. Block device (Penanda b)
    perangkat blok mengirimkan data dalam bentuk paket besar yang disebut blok (biasanya berukuran 512 byte atau 4 KB)
        a. Akses Data: Dapat diakses secara acak (random acces).  anda bisa melompat ke bagian manapun dari data tanpa harus membaca dari awal
        b. Buffering: sistem operasi menggunakan chace atau bffer untuk menyimpan data sementara agar proses baca-tulis lebih cepat
        
    2. Character device (penanda c)
    perangkat karakter (sering disebut RAW devices) mengirimkan data sebagai aliran karakter atau byte demi byte secara beruntun
       a.  Akses data: diakses secara sekuensial (beruntun) Data yang masuk pertama harus 
       dibaca pertama kali (seperti aliran air)
        b. Buffering: biasanya tidak menggunakan buffer sistem secara masif karena data bersifat real-time (seperti ketikan keyboaard)

### LATIHAN 2.4
1. <img width="994" height="408" alt="Screenshot (12).png" src="C:\Users\LENOVO\OneDrive\Pictures\Screenshots" />

### LATIHAN 2.5
1. port : udp
   Process : users: (("system-resolve",pid=521, fd=16))
# Kegunaan Utama Proses Ini
    1. DNS Caching: Ia menyimpan hasil pencarian alamat IP dari nama domain (misal: menerjemahkan google.com menjadi 142.250.xxx.xxx). Dengan menyimpan cache, permintaan berikutnya untuk domain yang sama akan diproses jauh lebih cepat tanpa harus bertanya ke server internet lagi.

    2. Manajemen DNS Multi-Link: Jika Anda terhubung ke Wi-Fi dan VPN secara bersamaan, proses ini mengatur server DNS mana yang harus digunakan untuk rute tertentu.

    3. LLMNR (Link-Local Multicast Name Resolution): Melalui UDP port 5355, ia memungkinkan komputer dalam jaringan lokal yang sama untuk saling menemukan nama satu sama lain tanpa perlu server DNS pusat (mirip dengan fungsi mDNS/Bonjour).

    4. Validasi DNSSEC: Ia dapat memeriksa apakah data DNS yang diterima telah dimanipulasi atau benar-benar asli dari sumbernya.