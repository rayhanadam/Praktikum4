# Struktur kondisi dan Perulangan
## Perulangan
### Latihan 1
Masukan kode berikut
```
# melakukan perulangan dari 0 sampai 10
for i in range(0, 10):
    # menampilkan variable i , (" " * 3) Artinya menambahkan spasi tiga kali lalu end => yaitu memulai baris baru setelah nilai terakhir
    print(i, " " * 3, end='')

    # melakukan perulangan dari 1 sampai 10
    for j in range(1, 10):
        # menampilkan output j + i , (" " * 3) Artinya menambahkan spasi tiga kali lalu end => yaitu memulai baris baru setelah nilai terakhir
        print(j+i, " " * 3, end='')
    print()
```
![Screenshot_20221109_231523](https://user-images.githubusercontent.com/115473812/200894991-39282369-b6bb-4286-95f2-4b3112a73ffa.png)
Hasil output
![Screenshot_20221109_231541](https://user-images.githubusercontent.com/115473812/200895332-c6fdb2e6-972a-4363-81d8-4c2cfb8e7b3c.png)

### Latihan 2
Masukan kode berikut
```
# import module random untuk mengenerate angka acak 0.3222...dst
from random import random

# variable jumlahNilai menampung input masukan lalu diconvert ke integer
jumlahNilai = int(input('Masukan jumlah nilai yang ingin dicari : '))

# variable nilaiRandom & kurangDariNolKomaLima berupa array/list untuk menyimpan data yang diperlukan nanti.
nilaiRandom = []
kurangDariNolKomaLima = []

# looping data berdasarkan jumlahNilai,
for i in range(0, jumlahNilai):
    # variable n = menyimpan angka random contoh: 0.988375998263476
    n = random()

    # menambahkan n ke variable nilaiRandom
    # fungsi append() untuk menambahkan data ke dalam variable yang type datanya berupa array/list
    nilaiRandom.append(n)

    # apakah n < dari 0.5 ? jika iya tampilkan lalu break dan memulai ke angka random selanjutnya
    while n < 0.5:

        # menambahkan n jika kurang dari 0.5 ke variable kurangDariNolKomaLima
        kurangDariNolKomaLima.append(n)

        # menampilkan output n
        print("data ke -", str(i+1), " => ", n)
        break

print()
# menampilkan output keseluruhan nilai random
print("Berikut keseluruhan nilai Random dari total ", jumlahNilai,
        "yaitu ", nilaiRandom)

print()
# menampilkan output keseluruhan nilai n < 0.5
print("Berikut nilai yang kurang dari 0.5 berjumlah ", len(kurangDariNolKomaLima),
        "yaitu ", kurangDariNolKomaLima)
```
![Screenshot_20221109_231833](https://user-images.githubusercontent.com/115473812/200896015-2a6ad9a0-5172-4421-9afd-93ce9d94fd4f.png)<br>
Hasil Output
![Screenshot_20221109_231930](https://user-images.githubusercontent.com/115473812/200896292-0612faa2-775f-48aa-9907-ab5c7ea1261b.png)

## Struktur Kondisi
### Latihan 1
Masukan kode berikut
```
# menerima input yang diketik dan menyimpannya didalam variable
bilanganSatu=input("Masukan bilangan Pertama : ")
bilanganKedua = input("Masukan bilangan Kedua : ")

# mengkonversi input string ke integer karena method input() selalu mengembalikan type data string
bilanganSatu = int(bilanganSatu)
bilanganKedua = int(bilanganKedua)

# mengecek untuk menentukan bilangan terbesar dari kedua bilangan
if bilanganSatu > bilanganKedua:
     print("Bilangan ", bilanganSatu, "lebih besar dari bilangan", bilanganKedua)
else:
     print("Bilangan ", bilanganKedua, "lebih besar dari bilangan", bilanganSatu)
```
![Screenshot_20221110_001653](https://user-images.githubusercontent.com/115473812/200897282-224403fd-e646-4b46-95f4-b4b54821fa73.png)<br>
Hasil Output
![Screenshot_20221110_001704](https://user-images.githubusercontent.com/115473812/200897434-790dbec6-1dd9-4b8a-8cba-9fef7ded90ff.png)


### Latihan 2
Masukan kode berikut
```
# variable angka untuk menampung jumlah angka yang diinputkan berupa array/list
angka = []
# variable bilangan untuk menentukan jumlah bilangan yang diinginkan
bilangan = input("Masukan jumlah bilangan yang diinginkan : ")
# mengkonversi input string ke integer karena method input() selalu mengembalikan type data string
bilangan = int(bilangan)

print("Program mengurutkan data ")

# melakukan perulangan berdasarkan jumlah dari variable bilangan

for i in range(0, bilangan):
# melakukan perulangan  input sampai jumlah dari variable bilangan yang sudah ditentukan
# misal bilangannya  sama dengan 4 maka akan dimunculkan input 4 kali lalu disimpan di variable => data

    data= int(input("Masukan Bilangan ke-" + str(i+1) + " : "))
# menambahkan isi dari variable data ke variable angka yang type datanya berupa array
# contoh input pertama [3] => input ke-dua [3,5] => input ke-tiga [3,5,2] => input ke-empat[3,5,2,9] dan seterusnya sesuai jumlah variable bilangan
    angka.append(data)

# menampilkan hasil program
# method sorted() berfungsi untuk mengurutkan nilai dari terkecil ke terbesar,
print("Bilangan yang sudah diurutkan dari terkecil ke terbesar", sorted(angka))
```
![Screenshot_20221110_002218](https://user-images.githubusercontent.com/115473812/200898358-9f0c4705-190c-4265-84a1-b8a27399748c.png)

Hasil output
![Screenshot_20221110_002228](https://user-images.githubusercontent.com/115473812/200898430-8b567114-43d6-4e2b-803b-7e4f5d0f1fcb.png)
