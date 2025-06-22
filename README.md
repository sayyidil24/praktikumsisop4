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

## **c. Jebakan Troll (Berlanjut)**

Setelah membuat dua file tersebut, SunnyBolt dan Ryeku memintamu untuk membuat jebakan yang telah dirancang oleh mereka. SunnyBolt dan Ryeku yang merupakan kolega lama DainTontas dan tahu akan hal-hal memalukan yang dia pernah lakukan, akan menaruh aib-aib tersebut pada file `very_spicy_info.txt`. Apabila dibuka dengan menggunakan command `cat` oleh user selain DainTontas, akan memberikan output seperti berikut:

```
DainTontas' personal secret!!.txt
```

Untuk mengecoh DainTontas, apabila DainTontas membuka `very_spicy_info.txt`, isinya akan berupa seperti berikut:

```
Very spicy internal developer information: leaked roadmap.docx
```

## **d. Trap**

Suatu hari, DainTontas mengecek PC dia dan menemukan bahwa ada sebuah file baru, `very_spicy_info.txt`. Dia kemudian membukanya dan menemukan sebuah leak roadmap. Karena dia ingin menarik perhatian, dia akan mengupload file tersebut ke sosial media `Xitter` dimana _followernya_ dapat melihat dokumen yang bocor tersebut. Karena dia pernah melakukan hal ini sebelumnya, dia punya script bernama `upload.txt` yang dimana ketika dia melakukan `echo` berisi `upload` pada file tersebut, dia akan otomatis mengupload sebuah file ke akun `Xitter` miliknya.

Namun ini semua adalah rencana SunnyBolt dan Ryeku. Atas bantuanmu, mereka telah mengubah isi dari `upload.txt`. Apabila DainTontas melakukan upload dengan metode `echo` miliknya, maka dia dinyatakan telah "membocorkan" info leak tersebut. Setelah DainTontas membocorkan file tersebut, semua file berekstensi `.txt` akan selalu memunculkan sebuah ASCII Art dari kalimat

```
Fell for it again reward
```

Setelah seharian penuh mencoba untuk membetulkan PC dia, dia baru sadar bahwa file `very_spicy_info.txt` yang dia sebarkan melalui script uploadnya tersebut teryata berisikan aib-aib dia. Dia pun ditegur oleh SunnyBolt dan Ryeku, dan akhirnya dia pun tobat.

## **NOTES**

- `upload.txt` hanyalah berupa file kosong yang dipakai untuk trigger _behavior change_ dari `cat` milik DainTontas. Deskripsi di soal hanyalah sebagai _storytelling_ belaka.
- Trigger dari Trap akan bersifat `persist` bahkan ketika FUSE telah di-unmount ataupun ketika mesin dimatikan/direstart

---
