# Tugas Praktikum 3

## Latihan 1
### Menampilkan Bilangan Acak Yang Lebih Kecil Dari 0.5
Untuk menampilkan bilangan acak yang lebih kecil dari 0.5 dibutuhkan code seperti berikut:
```python
num = int(input("masukkan bilangan n: "))
jumlah = num+1
start = 1
stop = jumlah
step = 1
for i in range(start, stop, step):
    from random import random
    a = random()
    print("data ke:", i, "=>", (a))
```
(1). Pertama kita akan membuat perintah "num = int(input("masukkan bilangan: "))" untuk memasukkan nilai n yang diinginkan.

(2). Kedua adalah memasukkan variable dibawah, untuk menentukan jumlah data yang akan kita cari.
- jumlah = num+1
- start = 1
- stop = jumlah
- step = 1

(3). Ketiga adalah memasukkan perintah "for i in range(start, stop, step)", untuk memulai dan mengakhiri looping sesuai input start, stop dan step yang sudah kita masukkan tadi di langkah kedua. 

(4). Keempat adalah memasukkan perintah "from random import random", agar bilangan yang ditampilkan adalah acak

(5). Masukkan perintah "a = random()" sebagai variable untuk menampilkan bilangan acaknya

(6). Terakhir adalah masukkan perintah "print("data ke:", i, "=>", (a)), untuk menampilkan hasil dari semua syntax yang sudah kita masukkan sebelumnya.

Berikut hasil eksekusi program diatas :
![ayam1](https://user-images.githubusercontent.com/56240134/68080625-e6c47c80-fe31-11e9-9685-b70f5610c9cb.png)
 
## Latihan2
### Menampilkan Bilangan Terbesar Dari N, Masukkan Bilangan 0 Untuk Berhenti
Untuk melakukan hal seperti judul diatas kita harus memasukkan code sebagai berikut : 
```python
a = int()
b = int()

while a >= 0: 
    a = int(input("Masukkan bilangan: "))
    if a == 0:
        break
    if a > b:
        b = a
print("Bilangan terbesar adalah", b)
```
1. Masukkan perintah " a = int() dan b = int()" untuk menyatakan bilangan bulat, nilai variable belum dimasukkan.

2. Lalu kita akan menggunakan statement while dan if : 
- while a >= 0: 
    - a = int(input("Masukkan bilangan: "))
- if a == 0:
    - break
- if a > b:
    - b = a
- print("Bilangan terbesar adalah", b)
> Keterangan : Ketika nilai a lebih dari 0, maka tampilkan input "masukkan bilangan: ". Ketika nilai a sama dengan 0 maka berenti menampilkan input "masukkan bilangan". Lalu a > b, b = a, akan mengambil nilai a terbesar untuk variable b. 

Hasil Eksekusi Program : 
![ayam2](https://user-images.githubusercontent.com/56240134/68085478-1ac09180-fe74-11e9-861f-5eba236e72f9.png)

## Latihan3
### Menghitung Total Keuntungan 
Jadi di latihan3 ini kita akan menghitung total keuntungan dari soal berikut : 
Seorang pengusaha menginvestasikan uangnya untuk memulai usaha dengan modal 100 juta, pada bulan 1 dan 2 belum menghasilkan laba. bulan ketiga mendapatkan laba sebesar 1%, dan pada bulan ke 5 pendapatan laba meningkat ke 5%, lalu pada bulan ke 8 mengalami penurunan sebesar 2%, sehingga laba menjadi 3%. Hitunglah keuntungan selama 8 bulan berjalannya usaha.

Nah untuk menghitung keuntungan usaha tersebut kira-kira beginilah codingnya : 
```python
modal = 100000000
laba = 0
untung = 0

for i in range (1, 9):
    if (i < 3):
        laba = 0
        untung = untung + laba
    elif (i < 5):
        laba = modal*1/100
        untung = untung + laba
    elif (i < 8):
        laba = modal*5/100
        untung = untung + laba
    else:
        laba = modal*2/100
        untung = untung + laba
    print("Laba bulan ke", i, "Sebesar:", laba)
print("Total laba adalah      :", untung)
```

1. Pertama kita akan memasukkan nilai ke variable "modal, laba dan untung", besar nilai dapat dilihat dalam code diatas.

2. Lalu kita akan menggunakan statement for dan if :
- for i in range (1, 9):
- if (i < 3):
    - laba = 0
    - untung = untung + laba
- elif (i < 5):
    - laba = modal*1/100
    - untung = untung + laba
- elif (i < 8):
    - laba = modal*5/100
    - untung = untung + laba
- else:
    - laba = modal*2/100
    - untung = untung + laba
    print("Laba bulan ke", i, "Sebesar:", laba)
print("Total laba adalah      :", untung)

> Keterangan : 
>- for i in range(1, 9) untuk menampilkan deret integer dari angka 1 sampai 8 (tidak sampai 9 karena basis index dari range dimulai dari 0).
>- lalu ada  "if (i < 3):", "- laba = 0" dan "- untung = untung + laba" yaitu jika i kurang dari 3 maka labanya = 0 (sesuai soalnya) dan kita akan memasukkan variable "untung = untung + laba" untuk menghitung jumlah keuntungan selama 8 bulan nanti.
>- lalu ada "- elif (i < 5):", "- laba = modal*1/100" dan "- untung = untung + laba". Disini laba ditulis "laba = modal*1/100". Maksudnya yaitu jumlah labanya berasal dari jumlah modal dikali 1 lalu dibagi 100 atau bisa disebut (1%) seperti tertera disoal.
>- lalu masih ada statement "elif (i < 8):" dan statement "else:" yang maksudnya pun sama seperti diatas, jadi saya tidak akan menjelaskannya kembali.
>- lalu ada perintah : print("Laba bulan ke", i, "Sebesar:", laba). Dengan perintah ini system akan menampilkan tulisan "Laba bulan ke" dilanjut dengan variable i dan tulisan "Sebesar" dilanjut dengan variable laba.
>- terakhir ada perintah : print("Total laba adalah      :", untung). Dengan perintah ini system akan menampilkan tulisan "Total laba adalah: " diikuti oleh variable untung yang sudah kita masukkan tadi.

Hasil Eksekusi Program
![ayam2](https://user-images.githubusercontent.com/56240134/68086155-47c47280-fe7b-11e9-9b47-8669319ea53c.png)
