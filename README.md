[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/s7OBVfDF)
| Name           | NRP        | Kelas     |
| ---            | ---        | ----------|
| Hilmi Fawwaz Sa'ad | 5025221103 | Jaringan Komputer (A) |
| Lathiifah Nabiila Bakhtiar | 5025221130 | Jaringan Komputer (A) |


## Put your topology config image here!
![image](https://github.com/user-attachments/assets/e34f4cc2-b410-43a4-8706-3bcde8edaa0e)

## Put your VLSM calculation here!
![e1c8a09b-f33f-4492-9510-196e4a383606](https://github.com/user-attachments/assets/78e3509e-87b5-41e0-87a0-7258a76271e4)
![image](https://github.com/user-attachments/assets/c3014ee7-3b2e-4067-83b7-809057132a74)

<b>Tree:</b>
![image](https://github.com/user-attachments/assets/a697c9fe-199b-4619-b55d-ac7a13eaf31b)

- Link
  ```
  https://miro.com/app/board/uXjVL9b1q6k=/?share_link_id=215931836124
  ```

## Put your IP route here!
### Konfigurasi
  - Heiji:
    ```
    auto eth0 
    iface eth0 inet dhcp
    
    auto eth1
    iface eth1 inet static
    	address 10.14.0.1
    	netmask 255.255.255.252
    
    auto eth2
    iface eth2 inet static
    	address 10.14.0.13
    	netmask 255.255.255.252
    ```
  - Agasa:
    ```
    auto eth0
    iface eth0 inet static
    	address 10.14.0.2
    	netmask 255.255.255.252
    	gateway 10.14.0.1
    	up echo nameserver 192.168.122.1 > /etc/resolv.conf
    
    auto eth1
    iface eth1 inet static
    	address 10.14.0.5
    	netmask 255.255.255.252
    
    auto eth2
    iface eth2 inet static
    	address 10.14.4.1
    	netmask 255.255.252.0
    ```
  - Kazuha:
    ```
    auto eth0
    iface eth0 inet static
    	address 10.14.0.6
    	netmask 255.255.255.252
    	gateway 10.14.0.5
    	up echo nameserver 192.168.122.1 > /etc/resolv.conf
    
    auto eth1
    iface eth1 inet static
    	address 10.14.8.1
    	netmask 255.255.248.0
    
    auto eth2
    iface eth2 inet static
    	address 10.14.0.9
    	netmask 255.255.255.252
    ```
  - Haibara:
    ```
    auto eth0
    iface eth0 inet static
    	address 10.14.8.2
    	netmask 255.255.248.0
    	gateway 10.14.8.1
    	up echo nameserver 192.168.122.1 > /etc/resolv.conf
    ```
  - Sonoko:
    ```
    auto eth0
    iface eth0 inet static
    	address 10.14.0.10
    	netmask 255.255.255.252
    	gateway 10.14.0.9
    	up echo nameserver 192.168.122.1 > /etc/resolv.conf
    ```
  - Ran:
    ```
    auto eth0
    iface eth0 inet static
    	address 10.14.4.2
    	netmask 255.255.252.0
    	gateway 10.14.4.1
    	up echo nameserver 192.168.122.1 > /etc/resolv.conf
    ```
  - Ayumi:
    ```
    auto eth0
    iface eth0 inet static
    	address 10.14.0.14
    	netmask 255.255.255.252
    	gateway 10.14.0.13
    	up echo nameserver 192.168.122.1 > /etc/resolv.conf
    
    auto eth1
    iface eth1 inet static
    	address 10.14.0.17
    	netmask 255.255.255.252
    
    auto eth2
    iface eth2 inet static
    	address 10.14.0.129
    	netmask 255.255.255.128
    ```
  - Mitsuhiko:
    ```
    auto eth0
    iface eth0 inet static
    	address 10.14.0.18
    	netmask 255.255.255.252
    	gateway 10.14.0.17
    	up echo nameserver 192.168.122.1 > /etc/resolv.conf
    
    auto eth1
    iface eth1 inet static
    	address 10.14.0.21
    	netmask 255.255.255.252
    
    auto eth2
    iface eth2 inet static
    	address 10.14.2.1
    	netmask 255.255.254.0
    ```
  - Megure:
    ```
    auto eth0
    iface eth0 inet static
    	address 10.14.0.22
    	netmask 255.255.255.252
    	gateway 10.14.0.21
    	up echo nameserver 192.168.122.1 > /etc/resolv.conf
    ```
  - Genta:
    ```
    auto eth0
    iface eth0 inet static
    	address 10.14.2.2
    	netmask 255.255.254.0
    	gateway 10.14.2.1
    	up echo nameserver 192.168.122.1 > /etc/resolv.conf
    ```
  - Kogoro:
    ```
    auto eth0
    iface eth0 inet static
    	address 10.14.3.1
    	netmask 255.255.254.0
    	gateway 10.14.2.1
    	up echo nameserver 192.168.122.1 > /etc/resolv.conf
    ```
  - Shinichi:
    ```
    auto eth0
    iface eth0 inet static
    	address 10.14.0.130
    	netmask 255.255.255.128
    	gateway 10.14.0.129
    	up echo nameserver 192.168.122.1 > /etc/resolv.conf
    ```
  - Conan:
    ```
    auto eth0
    iface eth0 inet static
    	address 10.14.0.192
    	netmask 255.255.255.128
    	gateway 10.14.0.129
    	up echo nameserver 192.168.122.1 > /etc/resolv.conf
    ```
    
### Routing
  - Heiji:
    ```
    post-up route add -net 10.14.0.4 netmask 255.255.255.252 gw 10.14.0.2
    post-up route add -net 10.14.8.0 netmask 255.255.248.0 gw 10.14.0.2
    post-up route add -net 10.14.0.8 netmask 255.255.255.252 gw 10.14.0.2
    post-up route add -net 10.14.4.0 netmask 255.255.252.0 gw 10.14.0.2
    post-up route add -net 10.14.0.16 netmask 255.255.255.252 gw 10.14.0.14
    post-up route add -net 10.14.0.20 netmask 255.255.255.252 gw 10.14.0.14
    post-up route add -net 10.14.2.0 netmask 255.255.254.0 gw 10.14.0.14
    post-up route add -net 10.14.0.128 netmask 255.255.255.128 gw 10.14.0.14
    ```
  - Agasa:
    ```
    post-up route add -net 10.14.8.0 netmask 255.255.248.0 gw 10.14.0.6
    post-up route add -net 10.14.0.8 netmask 255.255.255.252 gw 10.14.0.6
    ```
  - Ayumi:
    ```
    post-up route add -net 10.14.0.20 netmask 255.255.255.252 gw 10.14.0.18
    post-up route add -net 10.14.2.0 netmask 255.255.254.0 gw 10.14.0.18
    ```
    
## Soal 1

> Bagaimana cara mengkonfigurasi iptables pada router bernama 'Heiji' agar memungkinkan jaringan mengakses internet melalui interface eth0 menggunakan SNAT tanpa menggunakan MASQUERADE?

> _How to configure iptables on a router named ‘Heiji’ to allow the network to access the internet through interface eth0 using SNAT without using MASQUERADE?_

**Answer:**

- Screenshot
  ![image](https://github.com/user-attachments/assets/4496eaf2-2820-49c9-b16f-7d23d3f812c3)

- Configuration
  ```
  iptables -t nat -A POSTROUTING -s 10.14.0.0/20 -o eth0 -j SNAT --to-source $(hostname -I | awk '{print $1}')
  ```

- Explanation

  Konfigurasi `iptables` tersebut digunakan untuk mengatur aturan dalam tabel NAT pada jaringan, mengimplementasikan `Souce Network Addres Translation (SNAT)` dengan
  - `-t nat` untuk memberi tahu iptables bahwa aturan ini ditambahkan ke tabel NAT.
  - `-A POSTROUTING` untuk memodifikasi alamat sumber paket yang keluar dari server.
  - `-s 10.14.0.0/20` aturan hanya berlaku untuk paket yang berasal dari rentang IP `10.14.0.0 - 10.14.15.255`
  - `-o eth0` aturan hanya berlaku untuk paket yang keluar melalui `eth0`.
  - `-j SNAT` untuk menentukan tindakan yang diambil jika paket cocok dengan aturan, yaitu mengubah alamat IP sumber dari paket yang sesuai dengan aturan.
  - `--to-source` untuk menentukan alamat IP baru yang akan menggantikan alamat sumber asli dari paket.
  - `$(hostname -I | awk '{print $1}')` untuk mendapatkan alamat IP sistem.
    - `hostname -I` untuk menampilkan semua alamat IP pada sistem.
    - `awk '{print $1}'` untuk mengambil alamat IP pertama dari hasil tersebut.
    
    Hasil akhirnya adalah alamat IP publik dari antarmuka host, yang digunakan untuk menggantikan alamat sumber paket.
<br>

## Soal 2

> Kalian diminta untuk melakukan drop semua paket masuk TCP kecuali pada port 1744 pada node Shinichi.

> _You are asked to drop all incoming TCP packets except on port 1744 on Shinichi's node_

**Answer:**

- Screenshot
  ![image](https://github.com/user-attachments/assets/5c49d462-6eda-4f4d-bb52-c6dcdda7a44f)

- Configuration
  #### Shinichi
  ```
  iptables -A INPUT -p tcp --dport 1744 -j ACCEPT
  iptables -A INPUT -p tcp -j DROP
  ```

- Explanation

  Konfigurasi tersebut mengizinkan lalu lintas masuk ke `port 1744` melalui protokol `TCP` dan menolak lalu lintas `TCP` lain yang tidak sesuai dengan aturan sebelumnya. Misal, lalu lintas masuk yang menggunakan port selain 1744 akan ditolak paket `TCP`nya.
<br>

## Soal 3

> Lakukan pembatasan sehingga koneksi SSH pada semua Web Server hanya dapat dilakukan oleh user yang berada pada node Ran.

> _Make restrictions so that SSH connections to all Web Servers can only be made by users who are on the Ran node._

**Answer:**

- Screenshot

  node selain `Ran`

  ![image](https://github.com/user-attachments/assets/7e243cad-5a9b-42cf-971a-82ccc340bdea)

  node `Ran`

  ![image](https://github.com/user-attachments/assets/e2dbbded-cd5e-492c-8558-7598ac1079a5)

- Configuration
  ```
  iptables -A INPUT -p tcp --dport 22 -s 10.14.4.0/22 -j ACCEPT
  iptables -A INPUT -p tcp --dport 22 -j REJECT
  ```

- Explanation

  Konfigurasi tersebut hanya mengizinkan lalu lintas masuk ke `port 22` melalui protokol `TCP` dari subnet `10.14.4.0/22` atau node `Ran` dan menolak lalu lintas `TCP` lain yang tidak sesuai dengan aturan sebelumnya. Misal, lalu lintas masuk yang menggunakan port selain 22 dan atau bukan berasal dari subnet `10.14.4.0/22` akan ditolak paket `TCP`nya.
<br>

## Soal 4

> Semua subnet hanya dapat mengakses Web Server pada port 80 dan 443 (Conan, Sonoko, dan Megure) pada hari Senin-Jumat, pukul 07:00- 19:00.

> _All subnets can access the Web Server (Conan, Sonoko, and Megure) only on ports 80 and 443, from Monday to Friday, between 07:00-19:00._

**Answer:**

- Screenshot
  ![image](https://github.com/user-attachments/assets/893bbc5b-a02e-42f1-9ed0-34035960def8)

- Configuration
  ```
  iptables -A INPUT -p tcp -m multiport --dports 80,443 -m time --weekdays Mon,Tue,Wed,Thu,Fri --timestart 07:00 --timestop 19:00 -j ACCEPT
  iptables -A INPUT -j REJECT
  ```

- Explanation

  Konfigurasi tersebut mengizinkan lalu lintas masuk ke `port 80 dan 443` melalui protokol `TCP` hanya pada weekdays `--weekdays Mon,Tue,Wed,Thu,Fri` pukul `07:00 - 19:00` dan menolak lalu lintas `TCP` lain yang tidak sesuai dengan aturan sebelumnya. Misal, lalu lintas masuk yang menggunakan port selain 80 dan 443 dan atau di luar waktu yang telah ditentukan akan ditolak paket `TCP`nya.
<br>

## Soal 5

> Ternyata subnet Haibara memiliki akses tambahan, yaitu dapat mengakses Web Server pada port 80 dan 443 di luar hari Senin-Jumat (hari Sabtu dan Minggu), tanpa pembatasan waktu.

> _The Haibara subnet has additional access, allowing it to access the Web Server on ports 80 and 443 outside of Monday to Friday (on Saturday and Sunday), with no time restrictions._

**Answer:**

- Screenshot
  ![image](https://github.com/user-attachments/assets/381bdedd-daba-40e2-84d0-0dd67ddef885)

- Configuration
  ```
  iptables -I INPUT 3 -p tcp -m multiport --dports 80,443 -s 10.14.8.0/21 -j ACCEPT
  ```

- Explanation

  Konfigurasi tersebut menyisipkan aturan ke rantai INPUT pada posisi ke-3 `-I INPUT 3`, mengizinkan lalu lintas masuk ke `port 80 dan 443` melalui protokol `TCP` dari subnet `10.14.8.0/21` atau node `Haibara`, dan menolak lalu lintas `TCP` lain yang tidak sesuai dengan aturan sebelumnya. Misal, lalu lintas masuk yang menggunakan port selain 80 dan 443 dan atau bukan berasal dari subnet `10.14.8.0/21` akan ditolak paket `TCP`nya.
<br>

## Soal 6

> Akses ke Web Server Conan, Sonoko, dan Megure pada port 80 dan 443 dilarang pada hari Jumat, pukul 11:00-13:00 (maklum, Jumatan rek).

> _Access to the Web Server (Conan, Sonoko, and Megure) on ports 80 and 443 is prohibited on Fridays between 11:00-13:00 (It's Friday prayer time)._

**Answer:**

- Screenshot
  ![image](https://github.com/user-attachments/assets/9d8bb92f-4651-4f84-9551-86ebbd05f4a4)

- Configuration
  ```
  iptables -I INPUT 3 -p tcp -m multiport --dports 80,443 -m time --weekdays Fri --timestart 11:00 --timestop 13:00 -j DROP
  ```

- Explanation

  Konfigurasi tersebut menyisipkan aturan ke rantai INPUT pada posisi ke-3 `-I INPUT 3`, lalu melakukan drop paket `TCP` yang masuk ke `port 80 dan 443` melalui protokol `TCP` hanya pada hari Jumat `--weekdays Fri` pukul `11:00 - 13:00` dan menerima paket `TCP` pada waktu selain yang telah ditentukan.
<br>

## Soal 7

> Tambahkan logging paket yang di-drop di setiap node server dan router.

> _Enable logging for dropped packets on every server node and router._

**Answer:**

- Screenshot

  Genta -> Megure

  ![d99a7737-0d3d-4ca7-8835-3c131b17640f](https://github.com/user-attachments/assets/ce5aa497-713a-477e-b5e4-baadf0b6390e)

  Mitsuhiko (Router yang dilewati Genta -> Megure)

  ![aa54818f-97d5-4b27-b66f-d3e2eeb9e003](https://github.com/user-attachments/assets/0b573fcc-0254-424d-9c1c-6bd5557f847b)

  Megure

  ![f2ae6862-cbad-4728-8c75-724ce9251d03](https://github.com/user-attachments/assets/d1a02557-b652-4726-8024-8bad8ce2dd69)

- Configuration
  #### Router
  ```
  iptables -I FORWARD 1 -j LOG --log-prefix "DROP: "
  ```
  #### Web Server
  ```
  iptables -I INPUT 1 -j LOG --log-prefix "DROP: "
  ```

- Explanation

    Perintah iptables yang diberikan berfungsi untuk mencatat (log) paket yang di-drop pada router dan web server. Pada router, perintah `iptables -I FORWARD 1 -j LOG --log-prefix "DROP: "` akan mencatat semua paket yang diteruskan (forward) melalui router yang di-drop, dan menambahkan prefix `"DROP: "` pada log tersebut. Sementara itu, pada web server, perintah `iptables -I INPUT 1 -j LOG --log-prefix "DROP: "` akan mencatat semua paket yang diterima oleh web server yang di-drop, juga dengan prefix `"DROP: " pada log`.
<br>

## Soal 8

> Untuk keperluan maintenance, pilih salah satu Subnet dan lakukan blokir terhadap semua request protokol ICMP (ping) dari luar subnet terhadap subnet tersebut.

> _For maintenance purposes, select one Subnet and block all ICMP (ping) protocol requests from outside the subnet to that subnet._

**Answer:**

- Screenshot
  ![image](https://github.com/user-attachments/assets/483b57f9-22b0-4fe5-afba-1ad4f95f47b9)

- Configuration
  ```
  iptables -A INPUT -p icmp --icmp-type echo-request ! -s 10.14.2.0/23 -d 10.14.2.0/23 -j DROP
  ```

- Explanation

  Konfigurasi tersebut menambahkan aturan ke rantai INPUT `-A INPUT` yang berlaku untuk protokol ICMP `-p icmp`. Menerapkan aturan untuk tipe ICMP `echo-request` yang digunakan untuk permintaan ping, mengecualikan lalu lintas yang berasal dari subnet `10.14.2.0/23`, membatasi aturan hanya untuk lalu lintas yang ditujukan ke subnet `10.14.2.0/23`, dan `-j DROP` menolak lalu lintas yang cocok untuk aturan ini.
<br>

## Soal 9

> Untuk meningkatkan keamanan, setiap Web Server harus bisa melakukan blok terhadap IP yang melakukan scanning port dalam jumlah yang tidak wajar (maksimal 10 scan port) di dalam selang waktu 1 menit. 

> _To enhance security, each Web Server must be able to block IP addresses that perform an excessive number of port scans (a maximum of 10 port scans) within a 1-minute interval._

**Answer:**

- Screenshot

  ![26b2bbcd-77fe-43a7-880a-fa76758c1ba0](https://github.com/user-attachments/assets/1c2ff965-a906-4b1b-b76b-e555b8510741)

- Configuration
  ```
  iptables -I INPUT 1 -m recent --name SCAN_PORT --update --seconds 60 --hitcount 10 -j DROP
  iptables -I INPUT 2 -m recent --name SCAN_PORT --set -j ACCEPT
  ```

- Explanation
  - `iptables -I INPUT 1 -m recent --name SCAN_PORT --update --seconds 60 --hitcount 10 -j DROP`

    Konfigurasi tersebut menyisipkan aturan ke rantai INPUT pada posisi ke-1 `-I INPUT 1`, menggunakan modul recent untuk mencatat IP pengirim `-m recent`, memberi nama untuk daftar IP yang dicatat sebagai `SCAN_PORT`, lalu dengan `--update` memeriksa apakah IP yang sama sudah terdaftar di daftar `SCAN_PORT`. Dengan `--seconds 60`, mengecek apakah aktivitas terjadi dalam 60 detik terakhir, `--hitcount 10` akan memblokir jika aktivitas dari IP yang sama telah mencapai 10 kali dalam rentang waktu yang ditentukan, dan `-j DROP` menolak lalu lintas dari IP yang melanggar aturan ini.
  - `iptables -I INPUT 2 -m recent --name SCAN_PORT --set -j ACCEPT`

    Konfigurasi tersebut menyisipkan aturan ke rantai INPUT pada posisi ke-2 `-I INPUT 2`, `--set` menambahkan IP pengirim ke daftar `SCAN_PORT`, dan `-j ACCEPT` mengizinkan lalu lintas dari IP tersebut.
<br>

## Soal 10

> Akses dari client ke WebServer Conan pada port 80 akan didistribusikan bergantian antara Web Server Conan dan Web Server Sonoko. Sebaliknya akses pada Web Server Sonoko pada port 443 akan didistribusikan bergantian antara Web Server Conan dan Web Server Sonoko. Lakukan evaluasi menggunakan Jmeter terhadap berbagai metode load balancing seperti Round-Robin dan lain-lainnya.

> _Client access to the Conan Web Server on port 80 should be alternated between the Conan Web Server and the Sonoko Web Server. Conversely, access to the Sonoko Web Server on port 443 should be alternated between the Conan Web Server and the Sonoko Web Server. (Evaluate various load balancing methods, such as Round-Robin and others, using JMeter.)_

**Answer:**

- Screenshot

  htop 1

  ![254577cb-5ae0-46cd-912c-0f513c74e49b](https://github.com/user-attachments/assets/b91d25d7-dade-4099-9b25-1f1c4597d4ca)

  ab 1
  
  ![74c8b045-af3a-406e-82ac-70be4377f7e4](https://github.com/user-attachments/assets/f969e6f0-0f72-486c-a206-aeafa7d29501)

  htop 2
  
  ![1dcb72e8-ee67-48d0-91c6-74fef178e21e](https://github.com/user-attachments/assets/332ffadf-a35a-45b1-8ef5-3cc5d5d5b5e6)

  ab 2

  ![09938c61-4a9a-4c51-8ef2-74db47a5a8c4](https://github.com/user-attachments/assets/e6493e3d-e271-455b-9980-62a971da2007)

  htop 3

  ![fbb38bac-a7ef-4e22-b6f2-19c778075654](https://github.com/user-attachments/assets/da9c23e4-024a-460c-83b3-37b1fd8c7982)

  ab 3
  
  ![3dbb6194-b509-4b39-b4e9-97611de6c75a](https://github.com/user-attachments/assets/517d6e24-b121-4a94-a03e-a91118eb0c99)

- Configuration
  #### Kogoro
    ```bash
      CONAN=10.14.0.192
      SONOKO=10.14.0.10

      iptables -t nat -A PREROUTING -p tcp --dport 80 -m statistic --mode nth --every 2 --packet 0 -j DNAT --to-destination $CONAN:80
      iptables -t nat -A PREROUTING -p tcp --dport 80 -j DNAT --to-destination $SONOKO:80
      iptables -t nat -A POSTROUTING -p tcp -d $CONAN --dport 80 -j MASQUERADE
      iptables -t nat -A POSTROUTING -p tcp -d $SONOKO --dport 80 -j MASQUERADE
    ```
  #### Kazuha
    ```bash
      iptables -A FORWARD -s 10.14.8.2 -d 10.14.0.192 -j REJECT  
      iptables -A FORWARD -s 10.14.8.2 -d 10.14.0.10 -j REJECT   
      iptables -A FORWARD -s 10.14.8.2 -d 10.14.3.1 -j ACCEPT 
    ```

- Explanation

    Konfigurasi ini mengatur Load Balancer di node Kogoro dan firewall di node Kazuha. Di Kogoro, trafik HTTP pada `port 80` didistribusikan menggunakan metode Round-Robin antara dua web server: `Conan (IP: 10.14.0.192)` dan `Sonoko (IP: 10.14.0.10)`. Aturan `PREROUTING` dengan iptables melakukan `DNAT (Destination NAT)` untuk mengarahkan permintaan secara bergantian ke Conan atau Sonoko, sedangkan aturan `POSTROUTING` dengan `MASQUERADE` memastikan bahwa paket yang diteruskan memiliki alamat sumber yang sesuai agar respons kembali ke Kogoro. Di Kazuha, firewall membatasi akses langsung dari `Haibara (IP: 10.14.8.2)` ke Conan dan Sonoko dengan aturan REJECT, tetapi tetap mengizinkan akses ke Load Balancer `Kogoro (IP: 10.14.3.1)` menggunakan `ACCEPT`. 

  #### Cara Testing:
    Di Haibara
    ```bash
    curl 10.14.3.1 (lb - bisa)
    curl 10.14.0.192 (conan - gak bisa)
    curl 10.14.0.10 (sonoko - gak bisa)
    ```
      
    Jangan lupa tes juga menggunakan apache benchmark
<br>
  
## Problems

## Revisions (if any)
