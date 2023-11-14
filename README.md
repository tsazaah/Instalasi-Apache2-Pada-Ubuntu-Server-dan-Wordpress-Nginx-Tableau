# Instalasi-Apache2-Pada-Ubuntu-Server-dan-Wordpress-Nginx-Tableau

## Daftar Isi
- [Instalasi Apache2 pada Ubuntu Server Serta Melakukan Remote](#Instalasi-Apache2-pada-Ubuntu-Server-Serta-Melakukan-Remote)
- [Instalasi Wordpress](#Instalasi-Wordpress)
- [Instalasi Nginx](#Instalasi-Nginx)
- [Instalasi Tableau](#Instalasi-Tableau)
  
## Langkah-langkah mendownload dan menampilkan Apache2
Untuk melakukan instalasi Apache2 pastikan Ubuntu Server telah terinstall pada perangkat yang kita gunakan. Lalu kita dapat melakukan login sebagai user root.

1. Lakukan update sistem terlebih dahulu sebelum melakukan penginstallan dengan menggunakan perintah
   ```bash
   apt update
   ```
2. Lakukan instalasi apache2 dengan menggunakan perintah
   ```bash
   apt-get install apache2
   ```
3. Kita dapat mengecek apakah apache2 yang kita install sudah active atau belum dengan printah
   ```bash
   systemctl status apache2
   ```
4. Setelah itu lakukan pengecekan terhadap ip kita dengan menggunakan
   ```bash
   hostname -I
   ```
5. Setelah itu masuk ke web browser dan masukkan ip kita tadi, maka akan muncul tampilan apache2
   ![image](https://github.com/tsazaah/Instalasi-Apache2-Pada-Ubuntu-Server-dan-Wordpress-Nginx-Tableau/assets/150001965/ef056079-bcd3-4d12-b8c8-c00d9b37bbcd)

## Melakukan Remote Ubuntu Server Menggunakan PuTTY dan CMD
### PuTTY
1. Mendownload PuTTY pada web browser
2. Setelah didownload lakukan penginstallan terhadap PuTTY
3. Setelah itu buka aplikasi PuTTY
4. Selanjutnya masukkan ip kita
5. Dan remote pun dapat digunakan.

### CMD
1. Buka Ubuntu server dan cek ip dari ubuntu server yang sedang digunakan, dengan menggunakan perintah
   ```bash
   hostname -I
   ```
3. Kemudian buka CMD dan ketik perintah
   ```bash
   ssh username@ipaddress
   ```
   jika username dan ip yang masukkan benar mak kita akan dinminta untuk memasukkan password. 
4. Selanjutnya jika sudah berhasil maka tampilannya akan seperti pada gambar dibawah ini.
   ![image](https://github.com/tsazaah/Instalasi-Apache2-Pada-Ubuntu-Server-dan-Wordpress-Nginx-Tableau/assets/150001965/ed8a51f9-32d6-45a2-83f3-a36bf73fe3e3)

6. Jika sudah berhasil kita dapat melakukan remote ubuntu server melalui CMD.

 


