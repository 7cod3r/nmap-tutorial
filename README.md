# nmap-tutorial
nmap challenge
Tek Sunucuyu veya  IP Adresi tarama
Tek bir IP adresi Tarama:

  $ nmap 192.168.1.1
Host Adı Tarama:

  $ nmap ozkantan.com
Ayrıntı Seviye artırın:

  $ nmap -v ozkantan.com
  $ nmap -vv ozkantan.com
## IP Adresleri Tarama
### Çoklu IP Adresleri Tarama:
```
nmap 192.168.1.1 192.168.1.2 192.168.1.3
```
```
nmap 192.168.1.1,2,3
```
Bir Alt Ağ Tarama:
```
nmap 192.168.1.0/24
```
```
nmap 192.168.1.*
```
### IP Adresleri (192.168.1.0 – 192.168.1.200) Aralığı tarama:
```
nmap 192.168.1.0-200
```
## Aktif Bilgisayarlar için Ağ Taraması
### Bir ağ üzerinde aktif Hosts tara:
```
nmap -sn 192.168.1.0/24
```
### Dosyadan Hosts Listesini tarama
### Tarama Dosyadan sağlar:
```
nmap -iL input.txt
```
 
### Nmap IP / Hosts / Ağları Dışındakini Tara
### Nmap taraması Hedefler hariç:
```
nmap 192.168.1.0/24 --exclude 192.168.1.1
```
```
nmap 192.168.1.0/24 --exclude 192.168.1.1 192.168.1.5
```
```
nmap 192.168.1.0/24 --exclude 192.168.1.1,2,3
```
Bir dosyadan  listesi hariç tutulursa:
```
nmap 192.168.1.0/24 --excludefile exclude.txt
```
## Belirli Bağlantı Noktaları için Tarama

### Tek port tara:
```
nmap -p 80 <HOST veya IP>
```
### Seçilen portları tara:
```
nmap -p 80,443 <HOST veya IP>
```
### Port aralığı tara:
```
nmap -p 80-1000 <HOST veya IP>
```
### Tüm portları tara:
```
nmap -p "*" <HOST veya IP>
```
### En çok Kullanılan portları tara:
```
nmap --top-ports 10 <HOST veya IP>
```
