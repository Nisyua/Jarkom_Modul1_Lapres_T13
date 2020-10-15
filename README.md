# Jarkom_Modul1_Lapres_T13

### Disusun oleh :
- Anis Saidatur Rochma          [05311840000002]
- Desya Ananda Puspita Dewi     [05311840000046]

## A. Display Filter

### No. 1 
Sebutkan webserver yang digunakan pada ***"testing.mekanis.me"!***

```
http.host==testing.mekanisme.me
```
![](/img/1.png)

lalu klik kanan, pilih **TCP STREAM**

![](/img/1b.png)

### No. 2 
Simpan gambar **"Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"**!

**Penyelesaian**

Filter expression yang digunakan : 
```
HTTP
```
Lalu , `export objects berupa HTTP`

![](/img/2.png)

setelah itu text filter dengan kata "sukabumi", dan `Save`

![](/img/sukabumi.png)
![](/img/Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg)

### No. 3 
Cari username dan password ketika login di "ppid.dpr.go.id"!

```
http.request.method==POST
```
![](/img/3.png)

lalu , klik ```tcp stream``` , kemudian cari ***username*** dan ***password***

![](/img/3l.png)

### No. 4
Temukan paket dari **web-web** yang menggunakan **basic authentication** method!

```http.authbasic```

![](/img/4.png)

### No. 5
Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!

```http.host==aku.pengen.pw```

Lalu buka bagian Authorization (bawah) dan ada *credentials*

![](/img/5.png)

Lalu ikuti sesuai dengan perintah 

![](/img/5a.png)

### No. 6
Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file ***"Open This.pdf"*** di ***Answer.zip.*** Untuk mendapatkan password zipnya, temukan dalam file ***zipkey.txt*** (passwordnya adalah isi dari file txt tersebut).

Cari dengan mengggunakan filter expression
```
ftp-data
```
Kemudian `ctrl+F` dan cari dengan kata kunci _answer_ untuk menemukan file ***Answer.zip***. Lalu cari filenya dan save as menjadi zip

![](/img/6-1.png)
![](/img/6-2.png)

Lalu lakukan pencarian dengan kata kunci _zipkey_ untuk menemukan file ***zipkey.txt***

![](/img/6-3.png)

Setelah itu, didapatkan file pdf di dalam ***Answer.zip*** dan password zipnya di dalam file ***zipkey.txt***

![](/img/answer.png)
![](/img/zipkey.png)

Saat file berhasil dibuka, akan menampilkan isi dari file ___Open This.pdf*___

![](/img/6-5.png)

### No. 7 
Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut.
Your Super Mega Ultra Rare Hint = nama pdf-nya ***"Yes.pdf"***

### No. 8 
Cari objek apa saja yang didownload ***(RETR)*** dari koneksi FTP dengan Microsoft FTP Service!

Cari IP dari Microsoft FTP Sevice dengan menggunakan
```
ftp contains "Microsoft"
```

![](/img/8-1.png)

Kemudian cari objek yang didownload dengan menggunakan 
```
ftp.request.command contains "RETR" && ip.dst ==198.246.117.106
```

![](/img/8-2.png)

### No. 9
Cari username dan password ketika login FTP pada localhost!

```
ftp.request.command==USER || ftp.request.command==PASS
```

![](/img/9.png)

### No. 10 
Cari file .pdf di wireshark lalu download dan buka file tersebut!
    ***clue: "25 50 44 46"*** 

**Penyelesaian**

` ctrl + F ` dan cari data dengan menggunakan hex value `25 50 44 46`

![](/img/10.1.png)

Setelah menemukan hex value nya, klik kanan dan TCP Follow. Kemudian save as dalam bentuk Raw agar dapat membaca file .pdf

![](/img/10-3.png)
![](/img/10-2.png)

file .pdf berhasil ter-unduh dan dapat dilihat isi dari .pdf tersebut

![](/img/10.4.png)

## B. Capture Filter
11. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!
12. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!
13. Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!
14. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
15. Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!

Capture file dengan ```dst monta.if.its.ac.id```

![](/img/15a.png)

