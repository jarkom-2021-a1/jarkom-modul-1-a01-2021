# jarkom-modul-1-a01-2021

# Anggota kelompok A1 :
- 05111940000083 Fajar Satria
- 05111940000124 Gerry Sihaj
- 05111940000130 Adrian

### 1 Sebutkan webserver yang digunakan pada "ichimarumaru.tech"!
Langkah - langkah :
- Menggunakan display filter ```http contains "ichimarumaru.tech"``` 
- Klik kanan pada paket dan pilih ```Follow``` kemudian klik ```TCP Stream```   
- Webserver yang digunakan nginx/1.18.0 ubuntu

![no1_filter](https://user-images.githubusercontent.com/65168221/134684782-fc654819-dc38-45e8-8be0-7a4070a4843d.png)
![no1_server](https://user-images.githubusercontent.com/65168221/134684792-4790d2c2-d24d-442f-a262-d69df7853cdb.png)


### 2 Temukan paket dari web-web yang menggunakan basic authentication method!
Langkah - langkah :
- Menggunakan display filter ```http.authbasic```
- Akan muncul web-web yang menggunakan basic authentication method (paket 568, 573, dan 2066)
- Dapat dilihat pada Authorization di bagian Hypertext Transfer Protocol bernilai basic

![No2](https://user-images.githubusercontent.com/65168221/134022072-7da7db5a-203f-4fe3-99bc-1d5ac05acea2.png)


### 3 Ikuti perintah di basic.ichimarumaru.tech! Username dan password bisa didapatkan dari file .pcapng!
Langkah - langkah :
- Lihat authorization pada nomor 2
- Username dapat dilihat pada credential di authorization
- "Username : kuncimenujulautan dan password : tQKEJFbgNGC1NCZlWAOjhyCOm6o3xEbPkJhTciZN

![No3](https://user-images.githubusercontent.com/65168221/134022966-0038e148-4127-4435-aa79-48cde39198a2.png)

Kemudian, kerjakan perintah yang dikerjakan di basic.ichimarumaru.tech yaitu menyebutkan urutan konfigurasi kabel T568A
![No3lanjutan](https://user-images.githubusercontent.com/65168221/134023713-05791726-666f-47c2-8e0c-d12e02301770.png)

Konfigurasi dari kabel T568A:
- putih hijau
- hijau
- putih orange
- biru
- putih biru
- orange
- putih coklat
- coklat


### 4 Temukan paket mysql yang mengandung perintah query select!
Langkah - langkah :
- Menggunakan display filter ```mysql.query matches "select"```
- Paket yang mengandung perintah select adalah 3, 130, 183

![no4](https://user-images.githubusercontent.com/65168221/134687220-51106ddf-3d6d-49dd-8c4e-499ddadd58aa.png)

Paket 3 :  
![No4Paket3](https://user-images.githubusercontent.com/65168221/134025144-92de06b9-f2b4-48e3-b6a8-b5f1bd8dfa21.png)

Paket 130 :  
![No4Paket 130](https://user-images.githubusercontent.com/65168221/134025156-f8731863-09dd-4d61-bfb0-8c75f3d4f7df.png)

Paket 183 :  
![No4Paket183](https://user-images.githubusercontent.com/65168221/134025216-7d7ae10b-4af2-40a1-af7a-063803ce8b3b.png)


### 5 Login ke portal.ichimarumaru.tech kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file .pcap!
Langkah - langkah :
- Menggunakan display filter ```mysql.query matches "insert"```
- Username dapat dilihat pada paket 30 dimana di dalam syntax insert terdapat username beserta password nya
- Username = akakanomi dan Password = pemisah4lautan

![no5](https://user-images.githubusercontent.com/65168221/134688017-4e5340a9-2d8f-46b2-9f98-afb5871aa19d.png)

Kemudian, kerjakan perintah yang dikerjakan di portal.ichimarumaru.tech yaitu menyebutkan urutan konfigurasi kabel T568B
![No5lanjutan](https://user-images.githubusercontent.com/65168221/134026551-dd62eecf-5cdd-4a13-89ce-973b825df82d.png)

Konfigurasi dari kabel T568B:
- putih orange
- orange
- putih hijau
- biru
- putih biru
- hijau
- putih coklat
- coklat


### 6 Cari username dan password ketika melakukan login ke FTP Server!
Langkah - langkah :
- Menggunakan display filter ```ftp.request.command == "USER" || ftp.request.command == "PASS"```
- User : secretuser dan Pass : aku.pengen.pw.aja

![no6](https://user-images.githubusercontent.com/65168221/134688906-b0299fcb-7de2-4d64-973c-abfddcc5c310.png)


### 7 Ada 500 file zip yang disimpan ke FTP Server dengan nama 0.zip, 1.zip, 2.zip, ..., 499.zip. Simpan dan Buka file pdf tersebut. (Hint = nama pdf-nya Real.pdf)
Langkah - langkah :
- Menggunakan display filter ```ftp-data contains "Real.pdf"``` 
- Klik kanan pada paket, lalu Follow TCP Stream, ubah show data menjadi RAW
- Lalu Save As file dengan nama 201.zip
- Unzip dan buka file nya maka akan tertera file Real.pdf

![no7](https://user-images.githubusercontent.com/65168221/134691161-3a4da802-6ca0-40e0-8f2d-a042977f2c14.png)

![no7raw](https://user-images.githubusercontent.com/65168221/134691353-5356e13b-9258-4346-a932-af04fa990659.png)

![no7akhir](https://user-images.githubusercontent.com/65168221/134691366-cd321246-0401-4222-afbf-46854993c0eb.png)


### 8 Cari paket yang menunjukan pengambilan file dari FTP tersebut!
Langkah - langkah :
- Menggunakan display filter ```ftp.request.command contains "RETR"```

![no8](https://user-images.githubusercontent.com/65168221/134692505-b1ca0667-b673-465e-8273-4fb648a5592b.png)


### 9 Dari paket-paket yang menuju FTP terdapat inidkasi penyimpanan beberapa file. Salah satunya adalah sebuah file berisi data rahasia dengan nama "secret.zip". Simpan dan buka file tersebut!
Langkah - langkah :
- Menggunakan display filter ```ftp-data.command contains "secret.zip"```
- Klik kanan pada paket, lalu Follow TCP Stream, ubah show data menjadi Raw
- Lalu Save As file dengan nama secret.zip
- Ketika akan membuka file, akan diminta password dan langkah untuk mencari password nya dapat dilihat pada soal no 10

![no9](https://user-images.githubusercontent.com/65168221/134693746-c0ccaa5b-1b01-4b82-9733-a52f23f698e1.png)

![no9raw](https://user-images.githubusercontent.com/65168221/134693880-1ded8420-498b-4442-ab75-270bedbbdc24.png)

![no9pass](https://user-images.githubusercontent.com/65168221/134694133-3c28a904-f476-4741-a892-293c41b294bf.png)



### 10 Selain itu terdapat "history.txt" yang kemungkinan berisi history bash server tersebut! Gunakan isi dari "history.txt" untuk menemukan password untuk membuka file rahasia yang ada di "secret.zip"!
Langkah - langkah :
- Menggunakan display filter ```ftp-data.command contains "history.txt"```
- Klik kanan pada paket, lalu Follow TCP Stream
- Terlihat command mengompress file Wanted.pdf dengan password dari file bukanapaapa.txt
- Coba lihat file bukanapaapa.txt dengan menggunakan display filter ```ftp-data.command contains "bukanapaapa.txt"```
- Klik kanan pada paket, lalu Follow TCP Stream
- Gunakan password “d1b1langbukanapaapajugagapercaya” untuk membuka file secret.zip

![no10history](https://user-images.githubusercontent.com/65168221/134694806-b4ed8e96-5b2d-4422-8bf3-65d94ad07d23.png)

![no10caripass](https://user-images.githubusercontent.com/65168221/134695022-e5ac7683-31d6-48aa-84d0-2c62f1061939.png)

![no10bukanapaapa](https://user-images.githubusercontent.com/65168221/134695436-345828b0-f14b-486d-9be7-412fe3d4823c.png)

![no10bukanapaapa](https://user-images.githubusercontent.com/65168221/134695581-2a5d2353-4231-4ef3-aedb-a3011547809c.png)

![image16](https://user-images.githubusercontent.com/65168221/134695652-1960d5c4-2c6f-4d53-be86-ff56790daa73.png)


### 11 Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!
Langkah - langkah :
- Menggunakan capture filter ```src port 80``` 

![No11](https://user-images.githubusercontent.com/65168221/134027841-0a47f1ff-2356-47da-b6a4-adaf771b2eba.png)


### 12 Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!
Langkah - langkah :
- Menggunakan capture filter ```src port 21 || dst port 21```
- Di sini kita memasukkan ftp://ftp.adobe.com pada File Explorer untuk melakukan testing
 
![No12](https://user-images.githubusercontent.com/65168221/134028698-c8b8d678-e881-40ec-a11c-c0bc4d3176ef.png)


### 13 Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!
Langkah - langkah :
- Menggunakan capture filter ```dst port 443```

![No13](https://user-images.githubusercontent.com/65168221/134028969-d168432d-3200-4717-a92a-2c7d0b741f84.png)


### 14 Filter sehingga wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id!
Langkah - langkah :
- Menggunakan capture filter ```dst host kemenag.go.id```

![No14](https://user-images.githubusercontent.com/65168221/134029287-51aeaecb-f995-44ed-b731-f6ca3b3c3a69.png)


### 15 Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
Langkah - langkah :
- Menggunakan capture filter ```src host 192.168.140.234```
- Untuk mendapatkan ip, gunakan ```ipconfig``` pada cmd dan ip terdapat pada bagian ```IPv4 Address```
- 192.168.140.234 merupakan ip address dari salah satu anggota kelompok kami

![No15](https://user-images.githubusercontent.com/65168221/134029930-52364718-f5d0-4f68-b099-af18ec3a3f11.png)

Kendala : 
- Kesulitan mencari paket mysql yang berisi perintah query select (no 4)
- Saat mencari username dan password untuk FTP awalnya masih manual (no 6)
- Bingung memahami soal karena diminta paket pengambilan file namun paket pengambilan file tidak ada (no 8)
- Bingung saat mencari ip dari milik kita sendiri (no 15)

Pembagian Tugas :
- No 1-5   Gerry Sihaj  (05111940000124)
- No 6-10  Fajar Satria (05111940000083)
- No 11-15 Adrian       (05111940000130)
