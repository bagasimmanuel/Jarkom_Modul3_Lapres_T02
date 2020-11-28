
# Lapres Modul 3 Jarkom T02 2020

### Oleh:
- Muhammad Sulthon Nashir (0511174000017)
- Bagas Immanuel Lodianto (05311840000026)

#### No. 1
Buat topologi jaringan seperti gambar dibawah ini
##### Penyelesaian
Buat topologi dengan setting seperti di bawah di server

![No 1](https://github.com/bagasimmanuel/Jarkom_Modul3_Lapres_T02/blob/main/img/1.PNG)

#### No. 2
Buat DHCP Relay server di Suarabaya
##### Penyelesaian
Install __isc-dhcp-server__ di uml Surabaya, lalu setting seperti di bawah

![No 2](https://github.com/bagasimmanuel/Jarkom_Modul3_Lapres_T02/blob/main/img/2.PNG)

#### No. 3
Client pada subnet 1 mendapatkan range IP dari 192.168.0.10 sampai 192.168.0.100 dan 192.168.0.110 sampai 192.168.0.200
##### Penyelesaian
Edit __/etc/dhcp/dhcpd.conf__ seperti dibawah

![No 3](https://github.com/bagasimmanuel/Jarkom_Modul3_Lapres_T02/blob/main/img/3.PNG)

#### No. 4
Client pada subnet 3 mendapatkan range IP dari 192.168.1.50 sampai 192.168.1.70.
##### Penyelesaian
Edit __/etc/dhcp/dhcpd.conf__ seperti dibawah

![No 4](https://github.com/bagasimmanuel/Jarkom_Modul3_Lapres_T02/blob/main/img/4.PNG)

#### No. 5
Client mendapatkan DNS Malang dan DNS 202.46.129.2 dari DHCP
##### Penyelesaian
Edit __/etc/dhcp/dhcpd.conf__ seperti dibawah

![No 5](https://github.com/bagasimmanuel/Jarkom_Modul3_Lapres_T02/blob/main/img/3.PNG)

#### No. 6
Client di subnet 1 mendapatkan peminjaman alamat IP selama 5 menit, sedangkan client pada subnet 3 mendapatkan peminjaman IP selama 10 menit.
##### Penyelesaian
Edit __/etc/dhcp/dhcpd.conf__ seperti dibawah

![No 6a](https://github.com/bagasimmanuel/Jarkom_Modul3_Lapres_T02/blob/main/img/3.PNG)

##### 6a

![No 6b](https://github.com/bagasimmanuel/Jarkom_Modul3_Lapres_T02/blob/main/img/4.PNG)

##### 6b
#### No. 7
Buat user autentifikasi proxy dengan username : userta_t02 dan password : inipassw0rdta_t02
##### Penyelesaian
Install apache-utils lalu buat file password baru di squid3 dengan command ```htpasswd -c /etc/squid3/passwd userta_t02```

![No 7a](https://github.com/bagasimmanuel/Jarkom_Modul3_Lapres_T02/blob/main/img/7.PNG)

##### 7a

![No 7b](https://github.com/bagasimmanuel/Jarkom_Modul3_Lapres_T02/blob/main/img/7B.PNG)

##### 7b

#### No. 8
Buat agar proxy hanya dapat digunakan (diakses) pada pukul 13:00 - 18:00 hari Selasa - Rabu
##### Penyelesaian
Buat file __acl.conf__ di squid3 dengan setting seperti berikut

![No 8](https://github.com/bagasimmanuel/Jarkom_Modul3_Lapres_T02/blob/main/img/8.PNG)

#### No. 9
Buat agar proxy hanya dapat digunakan (diakses) pada pukul 21:00 - 9:00 hari Selasa - Kamis (jadi pada jumat pukul 09:00 adalah waktu terakhir akses)
##### Penyelesaian
Buat file __acl.conf__ di squid3 dengan setting seperti berikut

![No 9](https://github.com/bagasimmanuel/Jarkom_Modul3_Lapres_T02/blob/main/img/8.PNG)

#### No. 10
Redirect google.com ke monta.if.its.ac.id
##### Penyelesaian
Edit file squid.conf dengan setting seperti berikut 

![No 10](https://github.com/bagasimmanuel/Jarkom_Modul3_Lapres_T02/blob/main/img/10.PNG)

#### No. 11
Ubah forbidden error page menjadi seperti yang diminta
##### Penyelesaian
Pertama download dulu file yang diminta di soal, lalu ekstrak. Setelah itu ganti __ERR_ACCESS_DENIED__ default di __/usr/share/squid3/errors/English__ dengan file yang didownload.

![No 11](https://github.com/bagasimmanuel/Jarkom_Modul3_Lapres_T02/blob/main/img/11.PNG)

Setelah itu bisa dicek

![No 11](https://github.com/bagasimmanuel/Jarkom_Modul3_Lapres_T02/blob/main/img/11B.PNG)

#### No. 12
Buat domain di IP Mojokerto dengan nama domain janganlupa-ta.t02.pw dengan proxy 8080
##### Penyelesaian
Buat dulu domain di Malang dengan __bind9__, lalu setting domain seperti di Modul 2 kemarin. Seharusnya akan bisa mengakses proxy dengan nama domain.

![No 12](https://github.com/bagasimmanuel/Jarkom_Modul3_Lapres_T02/blob/main/img/12.PNG)


