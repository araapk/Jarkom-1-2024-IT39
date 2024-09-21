# Laporan Resmi Praktikum Jarkom Modul 1 2024

---
### Anggota Kelompok
- Rafika Az Zahra Kusumastuti  (5027231050)
- Johanes Edward Nathanael     (5027231067)

# Daftar Isi
- [Advance-Sanity-Check](#advance-sanity-check)
- [Illegal-Breakthrough](#illegal-breakthrough)
- [FTP-Login](#ftp-login)
- [Surprise](#surprise)
- [Corporate-Breach](#corporate-breach)
- [Pegawai-Negeri-Sebelah](#pegawai-negeri-sebelah)
- [EZ](#ez)
- [Rizzset](#rizzset)
- [Malacious-Code](#malacious-code)
- [Stegography](#stegography)


## Advance Sanity Check
### Deskripsi
Yang sederhana dulu aja.

### Flag
JarkomIT{8uK4n_S4n1ty_b1a5A_xcTcEi7kvH6fLCItLIZzNzBZZSu5b4OTIjRxoQ2UzzgIr6eWNHIwkIKK}

### Penjelasan
1.Masuk ke nc yang ada di soal nc 10.15.42.60 47000 & download pcapng dari soal

2.Lakukan Filtering berupa TCP dan follow streamnya 

3.Data berupa username pengirim dan juga filenya akan ketemu

4.Untuk mendapatkan pesan rahasia, ikuti petunjuk, lalu dapatkan kode dari ppt peraturan. 

5.Lakukan Decode dari Base64 ke Text


### Dokumentasi Pengerjaan
![image](https://github.com/user-attachments/assets/6accfd4f-0184-4b15-b943-2e9d78e911c7)
![image](https://github.com/user-attachments/assets/b05d5792-bcac-4cba-b826-e607751a0614)


## Illegal Breakthrough
### Deskripsi
Seorang full-stack developer bernama kevin sedang membuat sebuah web yang memiliki login page. Tetapi karena ia hanya digaji rendah, ia lupa untuk mengamankan web yang ia buat. Bantulah kevin untuk tracing dari jejak yang ditinggalkan oleh attacker.

### Flag
JarkomIT{d34th_fr0m_th3_sky_MXmnLDXXbYhSLr4OWxS2XQaYdH1ZiQ2blHsJEajlBeYADkX01Vm3WW1}

### Penjelasan
Langkah-langkah menemukan flag :
1. Masuk ke nc yang ada di soal `nc 10.15.42.60 47000`
2. Temukan IP address dari korban dengan cara mencari di `destination` pada wireshark
3. Temukan port yang digunakan sebagai webserver dengan cara `follow` pada ip addresnya, `open with http atau lainnya`, dan temukan portnya di hostnya
4. Temukan dimana endpoint yang terdapat login denan cara mencari di `info`
5. Temukan tools apa yang digunakan oleh attacker dengan cara `follow` pada ip addresnya
6. Temukan kredensial apa yang berhasil digunakan oleh attacker untuk login dengan cara `follow` pada ip addresnya kemudian temukan user dan passwordnya
7. Setelah menemukan semuanya akan muncul flagnya dan masukkan pada soal

### Dokumentasi Pengerjaan
![Screenshot_2024-09-18_13_10_51](https://github.com/user-attachments/assets/9a6afeb8-adc0-4ffb-a178-2e9e27b8017e)
![Screenshot_2024-09-18_13_11_19](https://github.com/user-attachments/assets/a0caec0b-6ec8-4361-b63c-98b37ef93a09)
![Screenshot_2024-09-18_13_11_37](https://github.com/user-attachments/assets/d0e277a1-94bb-4980-babb-3b6ba8d2b491)


## FTP Login
### Deskripsi
Seseorang menemukan sebuah celah dalam sebuah server. Ia mencoba untuk melakukan brute force login dan ia berhasil masuk. Lakukan pemeriksaan untuk melihat apa yang dilakukan oleh orang tersebut!

### Flag
JarkomIT{n0t_s0_s3cur3_ftp_Z6debjHQHNU2uOmUZvNqtt2QmL0KE2XZDY81Hkj30cLkOcDu30uhG1N}

### Penjelasan
Langkah-langkah menemukan flag :
1. Masuk ke nc yang ada di soal `nc 10.15.42.60 49000`
2. Temukan username yang berhasil digunakan untuk FTP login dengan cara mencari di `info`
3. Temukan password yang berhasil digunakan untuk FTP login dengan cara mencari di `info`
4. Setelah menemukan semuanya akan muncul flagnya dan masukkan pada soal

### Dokumentasi Pengerjaan
![Screenshot_2024-09-18_13_31_28](https://github.com/user-attachments/assets/941d8742-a782-402d-83a3-58ab8dea58b7)
![Screenshot_2024-09-18_13_31_52](https://github.com/user-attachments/assets/3e6654a1-8914-4369-96e3-59a2529bf1ee)



## Surprise
### Deskripsi
Setelah mengetahui apa yang diketahui pada challenge sebelumnya, sekarang lakukan analisis untuk mengetahui apa yang sebenarnya terjadi.
File sama seperti FTP Login.

### Flag
JarkomIT{l1ttl3_m0us3_1n_th3_h0us3_tSvczBH3CSN1umnRG7wxlQaxwG05z50eT7nZYnGy5x5eYbYW8VKITCHU} 

### Penjelasan
Langkah-langkah menemukan flag :
1. Masuk ke nc yang ada di soal `nc 10.15.42.60 48500`
2. Temukan service yang digunakan pada FTP server dengan cara mencari di `info`
3. Temukan nama file yang dikirim oleh attacker dengan cara mencari di `info`
4. Temukan pesan rahasia yang ditinggalkan oleh attacker dengan cara `follow` pada usernya, kemudian copy vector chipPartsnya dan convert ke text. Lalu, copy text ke terminal
5. Setelah menemukan semuanya akan muncul flagnya dan masukkan pada soal

### Dokumentasi Pengerjaan
![Screenshot_2024-09-18_13_33_23](https://github.com/user-attachments/assets/81b28609-e33c-40ab-acb9-e0ad9cd6061c)
![Screenshot_2024-09-18_13_33_39](https://github.com/user-attachments/assets/9b411e48-0c5c-42d0-a530-d2ae551011e2)


## Corporate Breach
### Deskripsi
Sebuah perusahaan IT support mendapatkan serangan oleh orang tidak dikenal. Bantulah perusahaan tersebut untuk melacak jejak yang ditinggalkan oleh attacker.

### Flag
JarkomIT{supp0rt_k0k_l3m4h_bg_spWRE3LkMxyzoWMMVAlNt7saeG6mdRvzEbWx7asAXh6U0efY4zEDG6}


### Penjelasan
1. Masuk ke nc yang ada di soal nc nc nc nc nc 10.15.42.60 51000 & download pcapng
2. Follow Stream TCP 
3. Lakukan Analisa
4. Masukkan Jawabannya ke pertanyaan


### Dokumentasi Pengerjaan
![image](https://github.com/user-attachments/assets/b21f83e4-2ad8-46f8-a387-3c634f2c05cf)


## Pegawai Negeri Sebelah
### Deskripsi
Kamu seorang data analisis diminta untuk memastikan ulang data-data dari beberapa pegawai

### Flag
JarkomIT{Tum8eN_p45SnYa_Ku4t_B1aS4Nya_3XQr3NnkfxlNQTXU6uq4FugJzL3rB7dh5vn8ICmZ6uB6BEiDMRKbM4h}


### Penjelasan
1.Masuk ke nc yang ada di soal nc nc 10.15.42.60 53000 & download pcapng dari soal
2.Lakukan Filtering berupa TCP dan follow streamnya
3. Analisa hasilnya dan masukkan jawaban ke pertanyaan


### Dokumentasi Pengerjaan
![image](https://github.com/user-attachments/assets/e3c441ac-31bb-49b4-bce7-662c787579c3)
![image](https://github.com/user-attachments/assets/263ae228-43e1-42fa-ad48-aecfb5cd8e7a)


## EZ
### Deskripsi
Aku sedang mencoba bikin chat service tapi kayanya pesannya bisa di sniffing deh? coba temukan pesannya.

### Flag
JarkomIT{BiAr_aman_Pake_sSh_WYCakZDMgW0JHjiO22BaCoYc03z54cKDZEScFSk5821Wm4ehhyy6EZ}


### Penjelasan
1.Masuk ke nc yang ada di soal nc nc nc 10.15.42.60 54000 & download pcapng dari soal
2.Lakukan Filtering berupa TCP dan follow streamnya
3.Analisa Hasilnya dan masukkan jawaban ke pertanyaanya


### Dokumentasi Pengerjaan
![image](https://github.com/user-attachments/assets/0a4fa041-6735-48c1-8c8d-745321bd67ed)
![image](https://github.com/user-attachments/assets/e6532cae-506f-4f6a-aade-2adcd974ad50)


## Rizzset
### Deskripsi
Aku sedang bereksperimen dengan suatu tools, kamu juga bisa menggunakannya untuk menjawab soal ini

### Flag
JarkomIT{Dn5_C0rR34t10n_n8hjYobGqKiPEhMTB3eeSGgeIr1zZPQRNUbU2unoKhb42NNwj4XcEh1T5}

### Penjelasan
Langkah-langkah menemukan flag :
1. Masuk ke nc yang ada di soal `nc 10.15.42.60 59500`
2. Cari di google cara install jarm
   - Clone github jarm di terminal
   - Pindah ke folder `jarm`
   - Install requirementsnya menggunakan command `pip install -r requirements.txt`
   - Run jarmnya agar dapat jarm webnya menggunakan command `python3 jarm.py -v webnya`, lalu copy jarmnya
   - Keluar dari folder
3. Masuk ke nc lagi
4. Temukan nama domain dari dns query pada log dengan cara mencari di `info`
5. Temukan IP dari domain dengan cara mencari di `source`
6. Masukkan jarm yang telah di dapat tadi
7. Setelah menemukan semuanya akan muncul flagnya dan masukkan pada soal

### Dokumentasi Pengerjaan
![Screenshot_2024-09-18_14_27_41](https://github.com/user-attachments/assets/733d276f-1803-4bbc-bb72-da660b259ad1)
![Screenshot_2024-09-18_14_28_03](https://github.com/user-attachments/assets/f9b7b309-3d4f-4467-9e26-0f8dc8e5cb86)
![Screenshot_2024-09-18_14_28_16](https://github.com/user-attachments/assets/4157acc9-c1e8-45a4-a0fa-cdf23681e257)
![Screenshot_2024-09-18_14_28_33](https://github.com/user-attachments/assets/4575af59-a978-49ba-82a3-ffa3317d79b9)
![Screenshot_2024-09-18_14_28_38](https://github.com/user-attachments/assets/f4867a8b-94e4-48ac-a8e9-3e8cdb900882)

## Malacious Code
### Deskripsi
Ternyata sang attacker dengan sengaja meninggalkan sesuatu untuk dibaca oleh kamu. Lihat pesan apa yang ditinggalkan attacker.
File sama seperti Corporate Breach.

### Flag
JarkomIT{s3cr3t_m3ss4ge_fr0m_4uth0r_F4p5OLXhaQmgLi4683d05j20LC0In5zP7zTZkdjGgotoT3En5Cb4L0R}


### Penjelasan
1. Masuk ke nc yang ada di soal nc nc nc nc nc 10.15.42.60 51000 & download pcapng
2. Follow Stream TCP 
3. Lakukan Analisa
4. Masukkan Jawabannya ke pertanyaan


### Dokumentasi Pengerjaan
![image](https://github.com/user-attachments/assets/57ae35a1-8546-4db5-925b-ab1ae8286bee)


## Stegography
### Deskripsi
Seekor stegosaurus berusaha menyimpan pesan di dalam beberapa gambar apakah kamu bisa memperoleh dan menyusunnya?

### Flag
JarkomIT{S3LaM4t_p4rA_PahL4WaN_DqhNt9l1cf224DkvLr6IzqldHP5sh19ZEiYuSuvJoF2YxaBUGWKKPhC5}


### Penjelasan
1. Masuk ke nc yang ada di soal nc nc nc nc 10.15.42.60 58000 & download pcapng serta zip dari soal
2. Lakukan Extract pada file untuk membuka file code berupa reversed.py
3. Lakukan Edit pada Python Code agar bisa menerima argv
4. Lakukan Extract FTP-Data berupa 13 Image yang sudah Steganografi
5. Jalankan Kode Python dengan memasukan syntax imagenya juga ke semua kodenya
6. Masukkan jawabannya ke pertanyaannya


### Dokumentasi Pengerjaan
![image](https://github.com/user-attachments/assets/abddb359-960f-4557-9275-d1d17f535cf1)
![image](https://github.com/user-attachments/assets/2614b4df-30e4-4a34-82af-dea1eee6d36d)
![image](https://github.com/user-attachments/assets/7672873d-c055-4824-9c51-b4db7f901bb4)
![image](https://github.com/user-attachments/assets/58702d1a-519e-4dd1-9f0b-5e9718b7e2cc)
![image](https://github.com/user-attachments/assets/aceee1bc-dbbc-46b1-bba4-46b1d3e5fae5)



