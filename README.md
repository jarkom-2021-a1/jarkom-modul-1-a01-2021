# jarkom-modul-1-a01-2021

### 1 Sebutkan webserver yang digunakan pada "ichimarumaru.tech"!
Langkah - langkah :
- Gunakan filter Host ichimarumaru.tech
- Filter http
- Webserver yang digunakan nginx/1.18.0 ubuntu

![No1](https://user-images.githubusercontent.com/65168221/134020964-a26793ff-a5dc-47e6-a4cf-1edd316fbb97.png)


### 2 Temukan paket dari web-web yang menggunakan basic authentication method!
Langkah - langkah :
- Gunakan filter http.authbasic
- Akan muncul web-web yang menggunakan basic authentication method (paket 568, 573, dan 2066)

![No2](https://user-images.githubusercontent.com/65168221/134022072-7da7db5a-203f-4fe3-99bc-1d5ac05acea2.png)

### 3 Ikuti perintah di basic.ichimarumaru.tech! Username dan password bisa didapatkan dari file .pcapng!
Langkah - langkah :
- Lihat authorization pada nomor 2
- Username dapat dilihat pada credential di authorization
- "Username : kuncimenujulautan dan password : tQKEJFbgNGC1NCZlWAOjhyCOm6o3xEbPkJhTciZN

![No3](https://user-images.githubusercontent.com/65168221/134022966-0038e148-4127-4435-aa79-48cde39198a2.png)

Kemudian, kerjakan perintah yang dikerjakan di basic.ichimarumaru.tech yaitu menyebutkan urutan konfigurasi kabel T568A
![No3lanjutan](https://user-images.githubusercontent.com/65168221/134023713-05791726-666f-47c2-8e0c-d12e02301770.png)


### 4 Temukan paket mysql yang mengandung perintah query select!
Langkah - langkah :
- Menggunakan filter mysql
- Paket mysql yang berisi perintah Select yaitu yang info nya berupa request query
- Paket yang mengandung perintah select adalah 3, 130, 183 (paket 30 tidak termasuk karena perintah nya Insert bukan Select)

Paket 3 :  
![No4Paket3](https://user-images.githubusercontent.com/65168221/134025144-92de06b9-f2b4-48e3-b6a8-b5f1bd8dfa21.png)

Paket 130 :  
![No4Paket 130](https://user-images.githubusercontent.com/65168221/134025156-f8731863-09dd-4d61-bfb0-8c75f3d4f7df.png)

Paket 183 :  
![No4Paket183](https://user-images.githubusercontent.com/65168221/134025216-7d7ae10b-4af2-40a1-af7a-063803ce8b3b.png)


### 5 Login ke portal.ichimarumaru.tech kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file .pcap!
Langkah - langkah :
- Menggunakan filter mysql
- Dan mencari yang query insert
- Username dapat dilihat pada paket 30 dimana di dalam syntax insert terdapat username beserta password nya
- Username = akakanomi dan Password = pemisah4lautan

![No5Paket30](https://user-images.githubusercontent.com/65168221/134026376-051fddad-203c-4105-8e94-bb162d59eff0.png)

Kemudian, kerjakan perintah yang dikerjakan di portal.ichimarumaru.tech yaitu menyebutkan urutan konfigurasi kabel T568B
![No5lanjutan](https://user-images.githubusercontent.com/65168221/134026551-dd62eecf-5cdd-4a13-89ce-973b825df82d.png)


### 6 Cari username dan password ketika melakukan login ke FTP Server!
Langkah - langkah :
- Gunakan filter ftp
- Terlihat pada paket 100 dan paket 104
- User : secretuser dan Pass : aku.pengen.pw.aja

![No6](https://user-images.githubusercontent.com/65168221/134026964-bdb9a3e3-c8a6-4df7-bd10-56ef914b38ce.png)


### 7
Gunakan filter ftp-data
Lalu sort berdasarkan length untuk mencari file yang berbeda diantara 500 zip tersebut

Terlihat paket yang mencurigakan terdapat pada packet 3075 dengan STOR file 201.zip
Gunakan filter “tcp.stream eq 128”
Klik kanan pada paket, lalu Follow TCP Stream, ubah show data menjadi RAW
Lalu Save As file dengan nama 201.zip

Buka file zip, akan tertera file Real.pdf


### 8
Gunakan filter ftp-data
Akan muncul paket paket pengambilan file


### 9
Pada packet 875,  terdapat file yang dikirimkan secret.zip
Gunakan filter tcp.stream eq 10
Klik kanan pada paket, lalu Follow TCP Stream, ubah show data menjadi Raw
Lalu Save As file dengan nama secret.zip

### 10

Coba lihat file history.txt dengan menggunakan filter tcp.stream eq 9
Klik kanan pada paket, lalu Follow TCP Stream

Terlihat command mengompress file Wanted.pdf dengan password dari file bukanapaapa.txt
Coba lihat file history.txt dengan menggunakan filter tcp.stream eq 11
Klik kanan pada paket, lalu Follow TCP Stream

Gunakan password “d1b1langbukanapaapajugagapercaya” untuk membuka file secret.zip

### 11 Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!
Langkah - langkah :
- filter menggunakan src port 80 
- src merupakan source kita mengambil paket dan dapat dilihat pada paket bahwa Src Port bernilai 80

![No11](https://user-images.githubusercontent.com/65168221/134027841-0a47f1ff-2356-47da-b6a4-adaf771b2eba.png)


### 12 Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!
Langkah - langkah :
- filter menggunakan src port 21 || dst port 21
- dst merupakan destination paket yang dituju
- Kita menggunakan || di sini karena mengandung port 21 berarti src atau dst port 21
- Di sini kita memasukkan ftp://ftp.adobe.com pada File Explorer untuk melakukan testing
 
![No12](https://user-images.githubusercontent.com/65168221/134028698-c8b8d678-e881-40ec-a11c-c0bc4d3176ef.png)

### 13 Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!
Langkah - langkah :
- filter menggunakan dst port 443
- Dapat dilihat pada paket bahwa Dst Port bernilai 443

![No13](https://user-images.githubusercontent.com/65168221/134028969-d168432d-3200-4717-a92a-2c7d0b741f84.png)


### 14 Filter sehingga wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id!
Langkah - langkah :
- filter menggunakan dst host kemenag.go.id

![No14](https://user-images.githubusercontent.com/65168221/134029287-51aeaecb-f995-44ed-b731-f6ca3b3c3a69.png)


### 15 Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
Langkah - langkah :
- filter menggunakan src host 192.168.140.234
- 192.168.140.234 merupakan ip address dari salah satu anggota kelompok kami

![No15](https://user-images.githubusercontent.com/65168221/134029930-52364718-f5d0-4f68-b099-af18ec3a3f11.png)


