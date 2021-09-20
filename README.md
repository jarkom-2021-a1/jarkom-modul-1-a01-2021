# jarkom-modul-1-a01-2021

### 1
Nginx

### 2 
Gunakan filter http.authbasic

Akan muncul web-web yang menggunakan basic authentication method
Yaitu 568, 573, 2066

### 3
Lihat authorization pada nomor 2
kuncimenujulautan:tQKEJFbgNGC1NCZlWAOjhyCOm6o3xEbPkJhTciZN


### 4

Menggunakan filter mysql
Membuka isi dari mysql protocol yang berisi select

Paket yang mengandung perintah select adalah
3, 130, 183

### 5
Menggunakan filter mysql
Dan mencari yang query insert

“username” = “akakanomi”
“Password” = “pemisah4lautan”

### 6
Gunakan filter ftp
Terlihat pada paket 100 dan paket 104
User : secretuser
Pass : aku.pengen.pw.aja

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

### 11
src port 80

### 12
src port 21

### 13
dst port 443

### 14
dst host kemenag.go.id

### 15

