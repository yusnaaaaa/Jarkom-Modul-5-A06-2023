# Jarkom-Modul-5-A06-2023

## Group Member

| NRP        | Name                        |
| ---------- | --------------------------- |
| 5025211057 | Salsabila Fatma Aripa       |
| 5025211254 | Yusna Millaturrosyidah      |

## Daftar Isi
- [Topologi](#topologi)
- [Soal 1](#soal-1)
	- [Penyelesaian soal 1](#penyelesaian-soal-1)
- [Soal 2](#soal-2)
	- [Penyelesaian soal 2](#penyelesaian-soal-2)
- [Soal 3](#soal-3)
	- [Penyelesaian soal 3](#penyelesaian-soal-3)
- [Soal 4](#soal-4)
	- [Penyelesaian soal 4](#penyelesaian-soal-4)
- [Soal 5](#soal-5)
	- [Penyelesaian soal 5](#penyelesaian-soal-5)
- [Soal 6](#soal-6)
	- [Penyelesaian soal 6](#penyelesaian-soal-6)
- [Soal 7](#soal-7)
	- [Penyelesaian soal 7](#penyelesaian-soal-7)
- [Soal 8](#soal-8)
	- [Penyelesaian soal 8](#penyelesaian-soal-8)
- [Soal 9](#soal-9)
	- [Penyelesaian soal 9](#penyelesaian-soal-9)
- [Soal 10](#soal-10)
	- [Penyelesaian soal 10](#penyelesaian-soal-10)

## Topologi
![topologi modul 5](https://github.com/yusnaaaaa/Jarkom-Modul-5-A06-2023/assets/114417418/05f5091c-9e3f-4cf8-981d-87cb6c9e77d2)

## Prefix IP
Kelompok A06 memiliki prefix IP `10.2`
## Tree
![image](https://github.com/yusnaaaaa/Jarkom-Modul-5-A06-2023/assets/114417418/58cf07a7-d134-434a-8427-fd9572da4829)

## Pembagian IP
![image](https://github.com/yusnaaaaa/Jarkom-Modul-5-A06-2023/assets/114417418/9d9a0e34-cc7b-4aea-ac9e-8aa1fd77ac3c)

## Konfigurasi Network
##### Atur Konfigurasi pada Router
- Aura
```
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
	address 10.2.14.133
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 10.2.14.129
	netmask 255.255.255.252
```
- Hieter
```
auto eth0
iface eth0 inet static
	address 10.2.14.130
	netmask 255.255.255.252
	gateway 10.2.14.129
	up echo nameserver 192.168.122.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 10.2.0.1
	netmask 255.255.248.0

auto eth2 
iface eth2 inet static
	address 10.2.8.1
	netmask 255.255.252.0
```
- Frieren
```
auto eth0
iface eth0 inet static
	address 10.2.14.134
	netmask 255.255.255.252
	gateway 10.2.14.133  
	up echo nameserver 192.168.122.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 10.2.14.137
	netmask 255.255.255.252

auto eth2 
iface eth2 inet static
	address 10.2.14.141
	netmask 255.255.255.252
````

- Himmel
```
auto eth0
iface eth0 inet static
	address 10.2.14.142
	netmask 255.255.255.252
	gateway 10.2.14.141
	up echo nameserver 192.168.122.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 10.2.12.1
	netmask 255.255.254.0

auto eth2 
iface eth2 inet static
	address 10.2.14.1
	netmask 255.255.255.128
```
- Fern
```
auto eth0
iface eth0 inet static
	address 10.2.14.2
	netmask 255.255.255.128
	gateway 10.2.14.1
	up echo nameserver 192.168.122.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 10.2.14.145
	netmask 255.255.255.252

auto eth2 
iface eth2 inet static
	address 10.2.14.149
	netmask 255.255.255.252
```

##### Atur Konfigurasi DNS SERVER
- Ricter
```
auto eth0
iface eth0 inet static
	address 10.2.14.146
	netmask 255.255.255.252
	gateway 10.2.14.145
	up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

##### Atur Konfigurasi DHCP SERVER
- Revolte
```
auto eth0
iface eth0 inet static
	address 10.2.14.150
	netmask 255.255.255.252
	gateway 10.2.14.149
	up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

##### Atur Konfigurasi WEB SERVER
- Stark
```
auto eth0
iface eth0 inet static
	address 10.2.14.138
	netmask 255.255.255.252
	gateway 10.2.14.137
	up echo nameserver 192.168.122.1 > /etc/resolv.conf
```
- Sein
```
auto eth0
iface eth0 inet static
	address 10.2.8.2
	netmask 255.255.255.128
	gateway 10.2.8.1
	up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

##### Atur Konfigurasi Client
- Turk Region
```
auto eth0
iface eth0 inet dhcp
#	address 10.2.0.2
#	netmask 255.255.248.0
	gateway 10.2.0.1
	up echo nameserver 192.168.122.1 > /etc/resolv.conf
```
- Grobe Forest
```
auto eth0
iface eth0 inet dhcp
#	address 10.2.8.3
#	netmask 255.255.255.128
	gateway 10.2.8.1
	up echo nameserver 192.168.122.1 > /etc/resolv.conf
```
- Laubhils
```
auto eth0
iface eth0 inet dhcp
#	address 10.2.12.2
#	netmask 255.255.254.0
	gateway 10.2.12.1
	up echo nameserver 192.168.122.1 > /etc/resolv.con
```
- SchwerMountain
```
auto eth0
iface eth0 inet dhcp
#iface eth0 inet static
#	address 10.2.14.2
#	netmask 255.255.255.128
	gateway 10.2.14.1
	up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

##### Atur Konfigurasi DHCP
- Revolte - dhcp.conf
```
apt update
apt install isc-dhcp-server -y
echo ‘INTERFACESv4=”eth0”’ > /etc/default/isc-dhcp-server

echo ‘
subnet 10.2.14.128 netmask 255.255.255.252 {
}
subnet 10.2.14.132 netmask 255.255.255.252 {
}

subnet 10.2.14.136 netmask 255.255.255.252 {
}

subnet 10.2.14.140 netmask 255.255.255.252 {
}

subnet 10.2.14.144 netmask 255.255.255.252 {
}

subnet 10.2.14.148 netmask 255.255.255.252 {
}

subnet 10.2.14.0 netmask 255.255.255.128 {
	range 10.2.14.3 10.2.14.126;
	option routers 10.2.14.1;
	option broadcast-address 10.2.14.127;
	option domain-name-servers 10.2.14.146;
	default-lease-time 180;
	max-lease-time 5760;	
}

subnet 10.2.12.0 netmask 255.255.254.0 {
	range 10.2.12.3 10.2.13.254;
	option routers 10.2.12.1;
	option broadcast-address 10.2.13.255;
	option domain-name-servers 10.2.14.146;
	default-lease-time 180;
	max-lease-time 5760;	
}

subnet 10.2.0.0 netmask 255.255.248.0 {
	range 10.2.0.3 10.2.7.254;
	option routers 10.2.0.1;
	option broadcast-address 10.2.7.255;
	option domain-name-servers 10.2.14.146;
	default-lease-time 180;
	max-lease-time 5760;	
}

subnet 10.2.8.0 netmask 255.255.252.0 {
	range 10.2.8.3 10.2.11.254;
	option routers 10.2.8.1;
	option broadcast-address 10.2.11.255;
	option domain-name-servers 10.2.14.146;
	default-lease-time 180;
	max-lease-time 5760;	
}’ >  /etc/dhcp/dhcpd.conf

service isc-dhcp-server start
```

##### Atur Konfigurasi DHCP RELAY
```
apt-get update
apt-get install isc-dhcp-relay -y
service isc-dhcp-relay start

echo ‘
SERVERS="10.2.14.150"

# On what interfaces should the DHCP relay (dhrelay) serve DHCP requests?
INTERFACES="eth0 eth1 eth2"

# Additional options that are passed to the DHCP relay daemon?
OPTIONS=""
‘ > /etc/default/isc-dhcp-relay
```

## Soal 1
Agar topologi yang kalian buat dapat mengakses keluar, kalian diminta untuk mengkonfigurasi Aura menggunakan iptables, tetapi tidak ingin menggunakan MASQUERADE.

### Penyelesaian soal 1
Supaya Aura dapat terhubung dengan node lain tanpa menggunakan MASQUERADE dapat menggunakan syntax seperti dibawah ini : 
```
IPETH0="$(ip -br a | grep eth0 | awk '{print $NF}' | cut -d'/' -f1)"
iptables -t nat -A POSTROUTING -o eth0 -j SNAT --to-source "$IPETH0" -s 10.2.0.0/20
```
Penjelasan Syntax : 
```IPETH0="$(ip -br a | grep eth0 | awk '{print $NF}' | cut -d'/' -f1)"``` : Baris ini digunakan untuk mengambil alamat IP dari antarmuka jaringan eth0 dan menyimpannya dalam variabel IPETH0. 

```iptables -t nat -A POSTROUTING -o eth0 -j SNAT --to-source "$IPETH0" -s 10.2.0.0/20``` : Baris ini digunakan untuk menambahkan aturan iptables pada tabel nat.

Hasil dari nomor ini nantinya tiap route dapat melakukan ping keluar (misalnya: google.com) seperti gambar dibawah ini :

## Soal 2
Kalian diminta untuk melakukan drop semua TCP dan UDP kecuali port 8080 pada TCP.

### Penyelesaian soal 2
Soal ini dapat diselesaikan dengan menggunakan syntax seperti berikut : 
```
iptables -A INPUT -p tcp --dport 8080 -j ACCEPT
iptables -A INPUT -p tcp ! --dport 8080 -j DROP
iptables -A INPUT -p udp -j DROP
```

Dari syntax tersebut, terlihat bahwa node hanya dapat menerima koneksi yang berasal dari port 8080 dan menggunakan protokol TCP.
Untuk membuka koneksi dari client dapat menggunakan command seperti dibawah ini :
```
nc -l -p 8080
```

Berikut merupakan testing dengan port 8080 dan selain port 8080 : </br>

<img width="700" alt="no2a" src="https://github.com/yusnaaaaa/Jarkom-Modul-5-A06-2023/assets/91377793/978f7d1e-e0e4-44e2-bc8d-e5b20d5783f4"></br>

<img width="700" alt="no2b" src="https://github.com/yusnaaaaa/Jarkom-Modul-5-A06-2023/assets/91377793/d988c011-cbb3-4fa3-9af9-a5d7b1e9ce2f"></br>

<img width="700" alt="no2c" src="https://github.com/yusnaaaaa/Jarkom-Modul-5-A06-2023/assets/91377793/ceed8ca8-7191-4a5a-904f-ae8207f132af"></br>

<img width="700" alt="no2d" src="https://github.com/yusnaaaaa/Jarkom-Modul-5-A06-2023/assets/91377793/a89f7442-8c02-4af5-a748-821a00b1da76"></br>

Dari hasil testing, terlihat bahwa koneksi yang menggunakan port 8080 memiliki kemampuan untuk mengirim dan menerima pesan, sementara untuk koneksi melalui selain port 8080 tidak.


## Soal 3
Kepala Suku North Area meminta kalian untuk membatasi DHCP dan DNS Server hanya dapat dilakukan ping oleh maksimal 3 device secara bersamaan, selebihnya akan di drop.

### Penyelesaian soal 3
Soal ini dapat diselesaikan dengan menggunakan syntax seperti berikut : 
```
iptables -A INPUT -m state --state ESTABLISHED,RELATED -j ACCEPT
iptables -A INPUT -p icmp -m connlimit --connlimit-above 3 --connlimit-mask 0 -j DROP
```

Berikut merupakan hasil testing dengan ping 4 node :

Apabila berhasil maka hasilnya pada node ke 4 akan gagal melakukan ping dan gagal tersambung ke node tujuan.

## Soal 4
Lakukan pembatasan sehingga koneksi SSH pada Web Server hanya dapat dilakukan oleh masyarakat yang berada pada GrobeForest.

### Penyelesaian soal 4
Untuk soal no 4 kita diminta untuk melakukan pembatasan subnet dari GrobeForest dan hanya bisa diakses oleh ip 22 atau SSH. Dalam mengerjakan soal ini dapat menggunakan syntax sebagai berikut pada masing-masing Web Server : 
```
iptables -A INPUT -p tcp --dport 22 -s 10.2.8.0/22 -j ACCEPT
iptables -A INPUT -p tcp --dport 22 -j DROP
```
Kemudian untuk melakukan testing dapat menggunakan command seperti dibawah ini : 
```
nc -l -p 22
```
Berikut merupakan hasil testing yang telah dilakukan :
Testing pada GrobeForest :
<img width="700" alt="no4grobe" src="https://github.com/yusnaaaaa/Jarkom-Modul-5-A06-2023/assets/91377793/2e398c57-e8fe-4724-963f-310cdac7663b"></br>

Pada GrobeForest menunjukkan hasil open yang artinya tersambung. 
Testing di selain GrobeForest :
<img width="700" alt="no4selaingrobe" src="https://github.com/yusnaaaaa/Jarkom-Modul-5-A06-2023/assets/91377793/dee4fea7-d935-483e-870d-ec0126b01660"></br>

Sedangkan untuk node lain filtered atau tidak berhasil tersambung.

## Soal 5
Selain itu, akses menuju WebServer hanya diperbolehkan saat jam kerja yaitu Senin-Jumat pada pukul 08.00-16.00.

### Penyelesaian soal 5
Untuk menyelesaikan soal 5 dapat menggunakan syntax sebagai berikut : 
```
iptables -A INPUT  -m time --weekdays Mon,Tue,Wed,Thu,Fri --timestart 08:00 --timestop 16:00 -p tcp --dport 22 -s 10.2.8.0/22 -j ACCEPT
```
Untuk melakukan testing sesuai dengan hari yang diinginkan kita dapat menambahkan command `date -u MMDDTTSSYYYY`
Berikut merupakan hasil testing yang telah dilakukan : 


<img width="700" alt="no5open" src="https://github.com/yusnaaaaa/Jarkom-Modul-5-A06-2023/assets/91377793/6c091116-2ea9-47fb-beee-c24dc4b7392e"></br>

<img width="700" alt="no5filtered" src="https://github.com/yusnaaaaa/Jarkom-Modul-5-A06-2023/assets/91377793/363e100d-fc90-445a-b599-82f18aed1f8b"></br>
Hasil akan menunjukkan open apabila webserver diakses oleh GrobeForest dengan date yang sesuai dan Hasil akan menunjukkan filtered apabila date nya tidak sesuai.

## Soal 6
Lalu, karena ternyata terdapat beberapa waktu di mana network administrator dari WebServer tidak bisa stand by, sehingga perlu ditambahkan rule bahwa akses pada hari Senin - Kamis pada jam 12.00 - 13.00 dilarang (istirahat maksi cuy) dan akses di hari Jumat pada jam 11.00 - 13.00 juga dilarang (maklum, Jumatan rek).

### Penyelesaian soal 6
Setup Pada Stark dan Sein
```
iptables -A INPUT -p tcp --dport 22 -s 10.2.8.0/22 -m time --timestart 12:00 --timestop 13:00 --weekdays Mon,Tue,Wed,Thu -j DROP

iptables -A INPUT -p tcp --dport 22 -s 10.2.8.0/22 -m time --timestart 11:00 --timestop 13:00 --weekdays Fri -j DROP
```
`-A INPUT` : Menambahkan aturan pada chain INPUT (penerimaan paket masuk).
`-p tcp` : Menentukan protokol yang digunakan (TCP).
dport 22: Menentukan port tujuan (22 untuk SSH).
`-s 10.2.8.0/22` : Menentukan alamat sumber yang diizinkan (subnet 10.2.8.0/22).
`-m time --timestart 12:00 --timestop 13:00 --weekdays Mon,Tue,Wed,Thu` : Menggunakan modul waktu untuk menentukan waktu akses yang dibatasi. Aturan ini berlaku pada hari Senin hingga Kamis dari pukul 12:00 hingga 13:00.
`-j DROP` : Menetapkan tindakan untuk menjatuhkan (DROP) paket yang sesuai dengan aturan di atas.

Penjelasan baris ke 2 dengan baris pertama, hanya aturan ini berlaku pada hari Jumat (Fri) dari pukul 11:00 hingga 13:00.

### Hasil

![6mod5](https://github.com/yusnaaaaa/Jarkom-Modul-5-A06-2023/assets/114417418/89fb3227-2102-4133-9dc5-9f2f22b93b14)

![6mod51](https://github.com/yusnaaaaa/Jarkom-Modul-5-A06-2023/assets/114417418/61580053-9d9d-43b9-ae05-cfdbca176148)


## Soal 7
Karena terdapat 2 WebServer, kalian diminta agar setiap client yang mengakses Sein dengan Port 80 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan dan request dari client yang mengakses Stark dengan port 443 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan.

### Penyelesaian soal 7
Setup pada Heiter
```
iptables -A PREROUTING -t nat -p tcp --dport 80 -d 10.2.8.2 -m statistic --mode nth --every 2 --packet 0 -j DNAT --to-destination 10.2.8.2

iptables -A PREROUTING -t nat -p tcp --dport 80 -d 192.177.4.2 -j DNAT --to-destination 10.2.14.138
```
```
iptables -A PREROUTING -t nat -p tcp --dport 443 -d 10.2.14.138 -m statistic --mode nth --every 2 --packet 0 -j DNAT --to-destination 10.2.14.138

iptables -A PREROUTING -t nat -p tcp --dport 443 -d 192.177.0.18 -j DNAT --to-destination 10.2.8.2
```

`-A PREROUTING:` Menambahkan aturan pada chain PREROUTING (praproses sebelum routing).
`-t nat:` Menentukan tabel nat untuk manipulasi alamat jaringan.
`-p tcp:` Menentukan protokol yang digunakan (TCP).
`--dport 80:` Menentukan port tujuan (80 untuk HTTP). Pada bagian ini portnya dapat disesuaikan dengan port yang diinginkan.
`-d 10.2.8.2:` Menentukan alamat tujuan (Sein).
`-m statistic --mode nth --every 2 --packet 0:` Menggunakan modul statistik untuk distribusi paket setiap dua kali pertama. Ini berarti paket-paket pertama akan diarahkan ke Sein.
`-j DNAT --to-destination 10.2.8.2:` Menetapkan tindakan untuk merubah alamat tujuan (Destination NAT) ke alamat Sein. Pada bagian ini dapat diubah dapa IP tujuan yang diinginkan

Lakukan testing pada SEIN dan STARK
- Untuk Port 80
``` 
while true; do nc -l -p 80 -c 'echo "ini sein"'; done
while true; do nc -l -p 80 -c 'echo "ini stark"'; done
```
- Untuk Port 443 
```
while true; do nc -l -p 443 -c 'echo "ini sein"'; done
while true; do nc -l -p 443 -c 'echo "ini stark"'; done
```
### Hasil

IP Sein

![7a](https://github.com/yusnaaaaa/Jarkom-Modul-5-A06-2023/assets/114417418/0bda3754-acca-401e-92c7-5a58c4045063)

IP Stark

![7b](https://github.com/yusnaaaaa/Jarkom-Modul-5-A06-2023/assets/114417418/eb4d54ee-d971-484b-b1b6-73b5065e6112)

## Soal 8
Karena berbeda koalisi politik, maka subnet dengan masyarakat yang berada pada Revolte dilarang keras mengakses WebServer hingga masa pencoblosan pemilu kepala suku 2024 berakhir. Masa pemilu (hingga pemungutan dan penghitungan suara selesai) kepala suku bersamaan dengan masa pemilu Presiden dan Wakil Presiden Indonesia 2024.

### Penyelesaian soal 8
Setup pada Stark dan Sein
```
Revolte_Subnet="10.2.14.148/30"
Pemilu_Start=$(date -d "2023-10-19T00:00" +"%Y-%m-%dT%H:%M")
Pemilu_End=$(date -d "2024-02-15T00:00" +"%Y-%m-%dT%H:%M")
iptables -A INPUT -p tcp -s $Revolte_Subnet --dport 80 -m time --datestart "$Pemilu_Start" --datestop "$Pemilu_End" -j DROP
```
- Menetapkan nilai variabel `Revolte_Subnet` dengan subnet yang diidentifikasi sebagai "Revolte." Subnet ini adalah 10.2.14.148/30
- Menetapkan nilai variabel `Pemilu_Start` dengan tanggal dan waktu mulai pemilu (19 Oktober 2023 pukul 00:00).
- Menetapkan nilai variabel `Pemilu_End` dengan tanggal dan waktu berakhirnya pemilu (15 Februari 2024 pukul 00:00).

`-A INPUT:` Menambahkan aturan pada chain INPUT (penerimaan paket masuk).
`-p tcp:` Menentukan protokol yang digunakan (TCP).
`-s $Revolte_Subnet:` Menentukan alamat sumber yang diizinkan (subnet Revolte).
`--dport 80:` Menentukan port tujuan (80 untuk HTTP).
`-m time --datestart "$Pemilu_Start" --datestop "$Pemilu_End":` Menggunakan modul waktu untuk menentukan periode akses yang dibatasi. Aturan ini berlaku mulai dari Pemilu_Start hingga Pemilu_End.
`-j DROP:` Menetapkan tindakan untuk menjatuhkan (DROP) paket yang sesuai dengan aturan di atas.

### Hasil

![85](https://github.com/yusnaaaaa/Jarkom-Modul-5-A06-2023/assets/114417418/4e9d6365-30bd-459e-a351-2fb748d6f22d)

## Soal 9
Sadar akan adanya potensial saling serang antar kubu politik, maka WebServer harus dapat secara otomatis memblokir  alamat IP yang melakukan scanning port dalam jumlah banyak (maksimal 20 scan port) di dalam selang waktu 10 menit. 
(clue: test dengan nmap)

### Penyelesaian soal 9
Setup pada Stark dan Sein
```
iptables -N portcheck
```
Menambahkan chain baru dengan nama portcheck menggunakan perintah -N.
```
iptables -A INPUT -m recent --name portcheck --update --seconds 600 --hitcount 20 -j DROP
iptables -A FORWARD -m recent --name portcheck --update --seconds 600 --hitcount 20 -j DROP
```
`iptables -A INPUT:` Menambahkan aturan pada chain INPUT (penerimaan paket masuk).
`iptables -A FORWARD:` Menambahkan aturan pada chain FORWARD (penerusan paket).
`-m recent --name portcheck:` Menggunakan modul recent untuk melacak status paket berdasarkan nama recent (portcheck).
`--update --seconds 600 --hitcount 20:` Menentukan bahwa aturan ini akan memeriksa paket yang datang dalam selang waktu 600 detik (10 menit) dan jika jumlah scan port mencapai 20, paket tersebut akan di-drop.
`-j DROP:` Menetapkan tindakan untuk menjatuhkan (DROP) paket yang sesuai dengan aturan di atas.

```
iptables -A INPUT -m recent --name portcheck --set -j ACCEPT
iptables -A FORWARD -m recent --name portcheck --set -j ACCEPT
```
`iptables -A INPUT:` Menambahkan aturan pada chain INPUT (penerimaan paket masuk).
`iptables -A FORWARD:` Menambahkan aturan pada chain FORWARD (penerusan paket).
`-m recent --name portcheck --set:` Menetapkan status paket menjadi "portcheck" (mencatat bahwa paket ini tidak terdeteksi sebagai scanning).
`-j ACCEPT:` Menetapkan tindakan untuk menerima (ACCEPT) paket yang sesuai dengan aturan di atas.

### Hasil

![55](https://github.com/yusnaaaaa/Jarkom-Modul-5-A06-2023/assets/114417418/95f67779-99f5-4db8-8aa6-feae03503207)

## Soal 10
Karena kepala suku ingin tau paket apa saja yang di-drop, maka di setiap node server dan router ditambahkan logging paket yang di-drop dengan standard syslog level. 

### Penyelesaian soal 10
Setup pada semua Node Router dan Server
```
iptables -A INPUT  -j LOG --log-level debug --log-prefix 'Dropped Packet' -m limit --limit 1/second --limit-burst 10
```
`-A INPUT:` Menambahkan aturan pada chain INPUT (penerimaan paket masuk).
`-j LOG:` Menetapkan tindakan untuk melakukan logging paket.
`--log-level debug:` Menentukan level log sebagai "debug."
`--log-prefix 'Dropped Packet':` Menetapkan awalan pesan log untuk paket yang di-drop sebagai "Dropped Packet."
`-m limit --limit 1/second --limit-burst 10:` Menggunakan modul limit untuk membatasi frekuensi logging. Aturan ini akan membatasi logging menjadi maksimal 1 pesan per detik dengan batasan 10 pesan jika melebihi batas tersebut.

### Hasil

![105](https://github.com/yusnaaaaa/Jarkom-Modul-5-A06-2023/assets/114417418/7deb178b-8d50-4af9-b02c-bd3b0f0c18e4)


