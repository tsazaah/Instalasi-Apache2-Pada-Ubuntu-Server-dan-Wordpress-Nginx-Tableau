# Instalasi-Apache2-Pada-Ubuntu-Server-dan-Wordpress-Nginx-Tableau

## Daftar Isi
- [Instalasi Apache2 pada Ubuntu Server](#Instalasi-Apache2-pada-Ubuntu-Server)
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

