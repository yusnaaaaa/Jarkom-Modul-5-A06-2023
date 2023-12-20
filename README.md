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

## Soal 3
Kepala Suku North Area meminta kalian untuk membatasi DHCP dan DNS Server hanya dapat dilakukan ping oleh maksimal 3 device secara bersamaan, selebihnya akan di drop.

### Penyelesaian soal 3

## Soal 4
Lakukan pembatasan sehingga koneksi SSH pada Web Server hanya dapat dilakukan oleh masyarakat yang berada pada GrobeForest.

### Penyelesaian soal 4

## Soal 5
Selain itu, akses menuju WebServer hanya diperbolehkan saat jam kerja yaitu Senin-Jumat pada pukul 08.00-16.00.

### Penyelesaian soal 5

## Soal 6
Lalu, karena ternyata terdapat beberapa waktu di mana network administrator dari WebServer tidak bisa stand by, sehingga perlu ditambahkan rule bahwa akses pada hari Senin - Kamis pada jam 12.00 - 13.00 dilarang (istirahat maksi cuy) dan akses di hari Jumat pada jam 11.00 - 13.00 juga dilarang (maklum, Jumatan rek).

### Penyelesaian soal 6

## Soal 7
Karena terdapat 2 WebServer, kalian diminta agar setiap client yang mengakses Sein dengan Port 80 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan dan request dari client yang mengakses Stark dengan port 443 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan.

### Penyelesaian soal 7

## Soal 8
Karena berbeda koalisi politik, maka subnet dengan masyarakat yang berada pada Revolte dilarang keras mengakses WebServer hingga masa pencoblosan pemilu kepala suku 2024 berakhir. Masa pemilu (hingga pemungutan dan penghitungan suara selesai) kepala suku bersamaan dengan masa pemilu Presiden dan Wakil Presiden Indonesia 2024.

### Penyelesaian soal 8

## Soal 9
Sadar akan adanya potensial saling serang antar kubu politik, maka WebServer harus dapat secara otomatis memblokir  alamat IP yang melakukan scanning port dalam jumlah banyak (maksimal 20 scan port) di dalam selang waktu 10 menit. 
(clue: test dengan nmap)

### Penyelesaian soal 9

## Soal 10
Karena kepala suku ingin tau paket apa saja yang di-drop, maka di setiap node server dan router ditambahkan logging paket yang di-drop dengan standard syslog level. 

### Penyelesaian soal 10

