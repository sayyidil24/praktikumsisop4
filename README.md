# praktikumsisop4

# **Drama Troll**

Dalam sebuah perusahaan penuh drama fandom, seorang karyawan bernama DainTontas telah menyinggung komunitas Gensh _ n, Z _ Z, dan Wut \* ering secara bersamaan. Akibatnya, dua rekan kerjanya, SunnyBolt dan Ryeku, merancang sebuah troll dengan gaya khas: membuat filesystem jebakan menggunakan FUSE.

Mereka membutuhkan bantuanmu, ahli Sistem Operasi, untuk menciptakan filesystem kustom yang bisa mengecoh DainTontas, langsung dari terminal yang dia cintai.

## **a. Pembuatan User**

Buat 3 user di sistem sebagai berikut yang merepresentasikan aktor-aktor yang terlibat dalam _trolling_ kali ini, yaitu:

- DainTontas
- SunnyBolt
- Ryeku

Gunakan `useradd` dan `passwd` untuk membuat akun lokal. User ini akan digunakan untuk mengakses filesystem FUSE yang kamu buat.a

![image](https://github.com/user-attachments/assets/e16d7fc3-c796-4a1e-ae63-f463347b8116)

Penjelasan code diatas untuk membuat 3 user yang sesuai diperintahkan soal dan membuat password dengan menggunakan useradd dan passwd dan untuk mengecek apakah code tersebut jalan dengan menggunakan 
getent passwd DainTontas SunnyBolt Ryeku
yang nanti akan keluar seluruh user yang telah kita buat di atas

![image](https://github.com/user-attachments/assets/1c10bf37-67e5-4b26-bbe1-fb9d5717da6b)



## **b. Jebakan Troll**

Untuk menjebak DainTontas, kamu harus menciptakan sebuah filesystem FUSE yang dipasang di `/mnt/troll`. Di dalamnya, hanya akan ada dua file yang tampak sederhana:

- `very_spicy_info.txt` - umpan utama.
- `upload.txt` - tempat DainTontas akan "secara tidak sadar" memicu jebakan.

jawaban
disini dikarenakan eror lalu ternyata solusi nya menggunakan virtual environment baru dan cara mengaktifkan nya memakai source ~/venv-troll/bin/activate lalu membuat file dan direktori trollfs
dan disini menggunakan python jadi mendownload library nya dahulu jika sudah maka kita membuat file dan isinya berupa python
![image](https://github.com/user-attachments/assets/a05ef23f-3849-437a-b273-66bbc1e9659e)
code diatas untuk membuat jebakan yang akan di mount ke /mnt/troll dan menampilkan 2 file palsu


