# LAPRES Jarkom-Modul-1-E16-2023

## SOAL 3
Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut:
a. Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?
b. Protokol layer transport apa yang digunakan?

### Jawaban
#### a. Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?
- ##### Penjelasan
  `(ip.src == 239.255.255.250 && udp.srcport == 3702) || (ip.dst == 239.255.255.250 && udp.dstport == 3702)`, digunakan untuk menyaring paket berdasarkan alamat IP sumber dan tujuan, serta port sumber dan tujuan. 

1. `(ip.src == 239.255.255.250 && udp.srcport == 3702)`: Ini memeriksa paket yang memiliki alamat IP sumber 239.255.255.250 dan port sumber UDP 3702. Ini berarti mencari paket yang dikirim oleh host dengan alamat IP ini dan menggunakan port UDP 3702 sebagai sumber.

2. `(ip.dst == 239.255.255.250 && udp.dstport == 3702)`: Ini memeriksa paket yang memiliki alamat IP tujuan 239.255.255.250 dan port tujuan UDP 3702. Ini berarti mencari paket yang dikirim ke host dengan alamat IP ini dan menggunakan port UDP 3702 sebagai tujuan.

Dengan kombinasi dari kedua kondisi ini (disjungsi dengan `||` yang berarti "atau"), dapat menyaring paket yang terkait dengan lalu lintas yang melibatkan alamat IP 239.255.255.250 dengan port UDP 3702 baik sebagai sumber atau tujuan. Hanya saja satu memeriksa 

- ##### Screenshoot
- ##### Kendala
  Tidak ada

#### b. Protokol layer transport apa yang digunakan?
- ##### Penjelasan
 Seperti yang terlihat di packet tersebut bahwa protokol yang di gunakan adalah UDP 
- ##### Screenshoot
- ##### Kendala
  Tidak ada

  
## SOAL 7
Berapa jumlah packet yang menuju IP 184.87.193.88?

### Jawaban
- ##### Penjelasan
Langkah-langkah untuk menghitung jumlah paket yang menuju alamat IP 184.87.193.88 di Wireshark adalah sebagai berikut:
- Buka aplikasi Wireshark dan buka file capture Wireshark yang berisi riwayat packet yang ingin Anda analisis.
- Di bagian atas jendela Wireshark, akan ada kolom "Display Filter." Klik pada kolom tersebut.
- Ketikkan filter berikut di kolom Display Filter dan tekan Enter:
```
ip.dst == 184.87.193.88
```
Filter ini akan mencocokkan semua packet yang memiliki alamat IP tujuan 184.87.193.88 dan hasil filteringnya berupa jumlah paket yaitu ada 6 paket. 
- ##### Screenshoot
- ##### Kendala
  Tidak ada

  
## SOAL 10
Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet

### Jawaban
- ##### Penjelasan
Untuk menemukan kredensial yang benar ketika user mencoba login menggunakan Telnet dalam Wireshark, berikut adalah langkah-langkahnya :
- Buka file capture Wireshark yang berisi riwayat packet saat aktivitas Telnet berlangsung.
- Gunakan "Login" sebagai kata kunci pencarian. Berikut langkah-langkahnya:
   a. Klik pada kolom "Display Filter" di bagian atas jendela Wireshark.
   b. Ketikkan filter berikut dan tekan Enter:
      ```
      telnet && frame contains "Login"
      ```
      Filter ini akan mencari packet Telnet yang mengandung kata "Login."
- Klik pada salah satu packet Telnet yang muncul di daftar.
- Dalam jendela "Packet Details" di bagian bawah, klik kanan pada packet tersebut dan pilih "Follow" > "TCP Stream." Ini akan membuka jendela baru yang menampilkan percakapan Telnet.
- Di dalam jendela TCP Stream, akan ada komunikasi antara client dan server Telnet. Biasanya, username dan password akan muncul di sini.
- Cari bagian yang mengandung informasi login, seperti username dan password. Dan disini muncul, username adalah "dhafin" dan password adalah "kesayangannyak0k0."
- ##### Screenshoot
- ##### Kendala
Sempat salah pada username karena menulis dengan kata aslinya tanpa membedakan warna merah dan biru nyaa, yang awalnya adlaah ddhhaaffiinn tapi seharusnya adalah dhafin
