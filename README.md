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

##### Atur Konfigurasi DHCP RELAY

## Soal 1
### Penyelesaian soal 1
## Soal 2
### Penyelesaian soal 2
## Soal 3
### Penyelesaian soal 3
## Soal 4
### Penyelesaian soal 4
## Soal 4
### Penyelesaian soal 4
## Soal 5
### Penyelesaian soal 5
## Soal 6
### Penyelesaian soal 6
## Soal 7
### Penyelesaian soal 7
## Soal 8
### Penyelesaian soal 8
## Soal 9
### Penyelesaian soal 9
## Soal 10
### Penyelesaian soal 10
