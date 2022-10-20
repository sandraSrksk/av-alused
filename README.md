# Arvutivõrgu alused
Võrgu identifikaatorid

# Hostinimi:
Iga võrgu seade on seotud unikaalse seadmega, mida nimetatakse hostinimeks.
Email, kasutajnimi@server 
kasutajanimi@ipaadress

# IP-aadress:
IP aadress on iga Internetis oleva seadme kordumatu identifikaator. IP-aadressi pikkus on 32 bitti. IPv6 aadress on 128 bitti.

## IPv6 on IP-protokolli uus versioon, mis on loodud eelmise versiooni (IPv4) probleemide lahendamiseks, kasutades aadressi pikkust 128 bitti, mitte 32.

## NAT
Kasutatakse privaatse IP-aadressiga hostidele juurdepääsu võimaldamiseks avalikku võrku.

## DHCP Server
annab võrgukonfi

## Unicast
Unicast-side toimub ühest võrgus olevast seadmest teise võrguseadmesse.

## Multicast
MultiCast-side toimub ühest võrgus olevast seadmest paljude, kuid mitte kõigi võrgus olevate seadmetega.

## Broadcast
Leviedastus toimub ühest võrguseadmest kõigi võrgus olevate seadmete vahel.

## Süsteemi privaatne IP-aadress , mida kasutatakse samas võrgus suhtlemiseks. Kasutades privaatset IP-andmeid või teavet saab saata või vastu võtta samas võrgus. 
## Süsteemi avalik IP-aadress on IP-aadress, mida kasutatakse väljaspool võrku suhtlemiseks.



# DNS-server:
DNS tähendab domeeninimede süsteemi. See on server, mis tõlgib URL-id või veebiaadressid nende vastavateks IP-aadressideks.

# MAC-aadress:
MAC kui füüsiline aadress, mis on iga hosti kordumatu identifikaator ja on seotud võrguliidese kaardiga (NIC). MAC-aadressi üldine pikkus on: 12-kohaline / 6 baiti / 48 bitti

# Port:
On kanal, mis võimaldab võrgu kasutajatel rakendusele andmeid saata või vastu võtta. Igal hostil võib töötada mitu rakendust. Kõik need rakendused tuvastatakse pordi numbri abil, milles need töötavad.

# Käsurea näited
- ping - Testib IP aadressi, saab vastu võtta taotlusi.
- Printf - On käsk stringide printimiseks. Prindib välja, mis sinna on pandud
- tcpdump  - Et näha TCP/IP-d ja muid pakette, mis edastatakse või võetakse vastu ühendatud võrgu kaudu.
- netstat	- Näitab TCP/IP ühenduse staatust
- sudo -annab käsklustele loa
- nc (NetCat) - TCP ühendused, portide kuulamine, IPv4 ja IPv6
- host - domeeninimede IP aadresside leidmiseks

## Harjutus 1
-	ip addr show eth0 - näitab esimese etherneti IP aadressi
    10: eth0@if11: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc noqueue state UP group default
        link/ether 02:42:ac:11:00:04 brd ff:ff:ff:ff:ff:ff link-netnsid 0
        inet 172.17.0.4/16 brd 172.17.255.255 scope global eth0
            valid_lft forever preferred_lft forever
-	ip route show - kirjeldab teid sihtkohtadesse
default via 172.17.0.1 dev eth0
172.17.0.0/16 dev eth0 proto kernel scope link src 172.17.0.4
172.18.0.0/16 dev docker0 proto kernel scope link src 172.18.0.1 linkdown
-	ping -c3 8.8.8.8 - seal on veebiaadress millega võimalik ühenduda
PING 8.8.8.8 (8.8.8.8) 56(84) bytes of data.
64 bytes from 8.8.8.8: icmp_seq=1 ttl=114 time=1.14 ms
64 bytes from 8.8.8.8: icmp_seq=2 ttl=114 time=0.319 ms
64 bytes from 8.8.8.8: icmp_seq=3 ttl=114 time=0.376 ms
3 packets transmitted, 3 received, 0% packet loss, time 2064ms
-	traceroute www.udacity.com - 
traceroute to www.udacity.com (104.18.41.189), 30 hops max, 60 byte packets
 1  172.17.0.1 (172.17.0.1)  0.054 ms  0.015 ms  0.016 ms
 2  * * *
 3  104.18.41.189 (104.18.41.189)  4.798 ms 141.101.65.12 (141.101.65.12)  5.144 ms 172.17.0.1 (172.17.0.1)  0.016 ms
-	host -t aaaa google.com - 
google.com has IPv6 address 2a00:1450:4013:c14::8b
google.com has IPv6 address 2a00:1450:4013:c14::65
google.com has IPv6 address 2a00:1450:4013:c14::64
google.com has IPv6 address 2a00:1450:4013:c14::66
-	mtr www.udacity.com - 
My traceroute  [v0.94]
cs-578716491323-default (172.17.0.4) -> www.udacity.com                                                     2022-10-20T17:27:47+0000
Keys:  Help   Display mode   Restart statistics   Order of fields   quit
-	host -t mx udacity.com - 
udacity.com mail is handled by 10 aspmx.l.google.com.
udacity.com mail is handled by 20 alt1.aspmx.l.google.com.



## Kõik maailma domeeninime tipud:
https://www.iana.org/domains/root/db

## DNS-ist
https://tparnpuu.webhosting.tptlive.ee/h5p/wp-admin/admin-ajax.php?action=h5p_embed&id=1

## Wireshark
https://www.wireshark.org/

## https://macaddress.io/mac-address-lookup/8L2oAK6YkE
 

