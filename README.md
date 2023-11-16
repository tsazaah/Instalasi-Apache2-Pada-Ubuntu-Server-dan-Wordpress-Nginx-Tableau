# Instalasi-Apache2-Pada-Ubuntu-Server-dan-Wordpress-Nginx-Tableau

## Daftar Isi
- [Instalasi Apache2 pada Ubuntu Server Serta Melakukan Remote](#Instalasi-Apache2-pada-Ubuntu-Server-Serta-Melakukan-Remote)
- [Instalasi Wordpress](#Instalasi-Wordpress)
- [Instalasi Nginx](#Instalasi-Nginx)
- [Instalasi Tableau](#Instalasi-Tableau)
  
## Instalasi Apache2 pada Ubuntu Server Serta Melakukan Remote
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

## Instalasi Wordpress
Sebelum melakukan instalasi masuk sebagai user root terlebih dahulu

1. Pertama lakukan instalasi MySQL dengan menggunakan perintah
   ```bash
   apt install mysql-server
   ```
2. Kemudian lakukan pengaturan terhadap keaman untuk melakukan perlindungan terhadap database dengan perintah
   ```bash
   mysql_sequre_installation
   ```
3. Selanjutnya adalah melakukan install PHP
   ```bash
   apt install php libapache2-mod-php php-mysql
   ```
4. Kemudian install extension PHP dengan menggunakan perintah
   ```bash
   sudo apt install php-curl php-gd php-mbstring php-xml php xmlrpc php-soap php-intl php-zip.
   ```
5. Selanjutnya adalah menginstall Wordpress, untuk menginstall wodpress kita harus masuk ke web server root dan masuk ke direktori `cd /var/www/html/`
6. selanjutnya install wordpress menggunakan perintah
   ```bash
   wget http://wordpress.org/latest.zip
   ```
   Setelah itu ketikkan perintah `tar -xzvf latest.tar.gz`
7. Kemudian buat database untuk wordpress pada mysql
   ```bash
   sudo -u root -p
   ```
   lalu buatlah database, contohnya seperti pada gambar dibawah ini.
   ![image](https://github.com/tsazaah/Instalasi-Apache2-Pada-Ubuntu-Server-dan-Wordpress-Nginx-Tableau/assets/150001965/21293681-9dea-431c-87e3-ad8ab9cec116)
8. Selanjutnya berikan perizinan untuk dapat mengakses wordpress folder dengan perintah
   ```bash
   chmod -R 777 wordpress/
   ```
9. Setelah itu lakukan konfigurasi file pada wordpress, masuk ke direktori wordpress `cd wordpress/` dengan menggunakan perintah `mv wp- config-sample.php wp-config.php` setelah itu `nano wp.config.php`, kemudian lakukan konfigurasi dengan mengubahnya sesuai database yang telah kita buat.
    ![image](https://github.com/tsazaah/Instalasi-Apache2-Pada-Ubuntu-Server-dan-Wordpress-Nginx-Tableau/assets/150001965/b0df0afa-f177-499e-8605-1997ed1ac1df)
10. selanjutnya adalah membuka wordpress ada halaman web
    ```bash
    https://localhost/wordpress
    ```
    ![image](https://github.com/tsazaah/Instalasi-Apache2-Pada-Ubuntu-Server-dan-Wordpress-Nginx-Tableau/assets/150001965/491ce837-617e-44c2-93b4-12bb2ad3665f)

## Instalasi NGINX

1. Gunakan perintah perintah
   ```bash
   sudo apt install nginx
   ```
2. Kemudian cek apakah nginx sudah teristall
   ```bash
   sudo ufw app list
   sudo ufw allow 'Nginx HTTP'
   ```
4. Kemudian cek status dari nginx, sebelumnya jika telah menginstall apache2 maka apache2 harus di stop terlebih dahulu menggunakan `systemctl stop apache2` kemudian mulai menggunakan nginx dengan menggunakan perintah `systemctl start nginx`, setelah itu cek status dari nginx `systemctl status nginx`.
5. Kemudian cek ip address kita dan buka web browser masukkan `ipaddress/index.nginx-debian.html` dan akan muncul tulisan welcome to nginx
   ![image](https://github.com/tsazaah/Instalasi-Apache2-Pada-Ubuntu-Server-dan-Wordpress-Nginx-Tableau/assets/150001965/6884f96d-842c-4ed4-ae91-66da8660ae56)

## Instalasi Tableau

1. Pertama cari tableau pada web browser
2. Kemudian disini saya akan mengistall tableau public, jadi saya mengklik pilihan tableau public
3. Selanjutnya klik pada tulisan create, disana akan terdapat pilihan download tableau public edition dan klik piliha tersebut
4. Kemudian kita akan diarahkan untuk mengisi data terlebih dahulu, baru kemudian kita dapat melakun download.
5. Selanjutnya selah proses download selesai, lakukan instalasi tableau pada komputer
6. Dan tableau public sudah bisa digunakan untuk visualisasi data.
   ![image](https://github.com/tsazaah/Instalasi-Apache2-Pada-Ubuntu-Server-dan-Wordpress-Nginx-Tableau/assets/150001965/38c28a4b-2d35-45c6-9d97-5ea263e8e2d4)
7. Kita dapat memilih pilihan pada bagian sebelah kiri untuk memasukkan data yang akan kita gunakan untuk visualisasi, pilih sesuai bentu data yang akan kita olah.
8. Kemudian setelah itu tampilannya akan seperti pada gambar dibawah ini, untuk
melakukan visualisasi data klik tulisan sheet pada bagian kiri bawah, kemudian kita dapat melakukan visualisasi data.
  ![image](https://github.com/tsazaah/Instalasi-Apache2-Pada-Ubuntu-Server-dan-Wordpress-Nginx-Tableau/assets/150001965/fb3ba91c-4231-4625-a748-49cd70ff5af6)
9. Setelah mengklik pilihan sheet kita dapat melakukan visualisasi data sesuai kebutuhan kita. Visualisasi data dapat dilakukan dengan menyeret bagian tables ke rows atau pun column kemudian setelah selesai kita dapat menyimpan hasil visualisasi data tersebut.
   ![image](https://github.com/tsazaah/Instalasi-Apache2-Pada-Ubuntu-Server-dan-Wordpress-Nginx-Tableau/assets/150001965/41e23a28-2714-48f3-8895-adcc2ec71600)

10. Dari dataset tersebut dapat divisualisaikan mahasiswa yang lulus cepat, dengan yang tidak lulus cepat. Kemudian kita juga dapat melihat IPK, jumlah organisasi yang diikuti, serta berapa kali mahasiswa tersebut mengikuti forum komunikasi.
    
  ![image](https://github.com/tsazaah/Instalasi-Apache2-Pada-Ubuntu-Server-dan-Wordpress-Nginx-Tableau/assets/150001965/52a7e3dc-48d7-49d3-a668-99d572a50c75)






 


