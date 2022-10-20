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
If you run ping -c3 8.8.8.8  and get the output, 3 packets transmitted, 3 received, 0% packet loss, which of these conclusions seem reasonable?
Your computer has interne access 
The computer at 8.8.8.8 is up and running - (sest saan sõnumeid sealt)
Your ISP knows how to send traffic towards Google.  (Google server on sellel aadressil.)

## Harjutus 2
So what happens if on your Linux machine you run this command, printf 'HEAD / HTTP/1.1\r\nHost: en.wikipedia.org\r\n\r\n' | nc en.wikipedia.org 80
Saame tagasi ifot Wikipedia serverilt

## Harjutus 3
What web servers does Google use? - gws (Google Web Server)
printf 'HEAD / HTTP/1.1\r\nHost: www.google.com\r\n\r\n' | nc www.google.com 80
HTTP/1.1 200 OK
date -"-
Server: gws

## Harjutus 4
How would you get nc on port 3456?
käsuga: nc -l 3456 

## Harjutus 5
With 2 terminals SSHed into yur Linux box, on one of them, set an nc process listening on a port. Pick whatever port number 4356.  And in the other terminal, connect to it with nc localhost 3456. Figure out how to disconnect them without just closing the SHH session
Ctr D ütleb ühele nc välju ja teine väljub, kui üks o ühenduse lõpetanud

## Harjutus 6 
Using netcat - fnd out what is the highest port that you can listen on:
Tava kasutaja saab kuulata 1024 - 65535 porti vahemikus
Kasutades näiteks sudo käsku oleks võimalik kuulata kõige madalamalt 1

## Harjutus 7
Milline programm kuulab?
Kasutansudo lsof -i . see, kus on kirjas LISTEN


## Kõik maailma domeeninime tipud:
https://www.iana.org/domains/root/db

## DNS-ist
https://tparnpuu.webhosting.tptlive.ee/h5p/wp-admin/admin-ajax.php?action=h5p_embed&id=1

## Wireshark
https://www.wireshark.org/

## https://macaddress.io/mac-address-lookup/8L2oAK6YkE
 

