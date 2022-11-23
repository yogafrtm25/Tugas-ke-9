# Praktikum5
Nama : Yoga Pratama 

NIM : 312210042

Kelas : TI.22.A1

## DAFTAR ISI <br>
| No | Description | Link |
|-----|------|-----|
|1|Latihan|[Click Here](#latihan)|
|2|Nilai Mahasiswa|[Click Here](#nilai-mahasiswa)|
|3|Flowchart Nilai Mahasiswa |[Click Here](#flowchart-nilai-mahasiswa)|

## Latihan
Buat sebuah list sebanyak 5 elemen dengan nilai bebas

#### Akses list :
- Tampilkan elemen ke 3
- Ambil nilai elemen ke 2 sampai elemen ke 4
- Ambil elemen terakhir
#### Ubah elemen list :
- Ubah elemen ke 4 dengan nilai lainnya
- Ubah elemen ke 4 sampai dengan elemen terakhir
#### Tambah elemen list :
- Ambil 2 bagian dari list pertama (A) dan jadikan list ke 2 (B)
- Tambah list B dengan nilai string
- Tambah list B dengan 3 nilai
- Gabungkan list B dengan list A

#### Langkah-langkah :
1. Buat programnya terlebih dahulu seperti gambar di bawah ini

![Menginput nilai 5 elemen (1)](https://user-images.githubusercontent.com/115678171/203445766-790ff353-4f39-4e39-b20a-a753e741b92c.png)

![Menginput Nilai 5 elemen(2)](https://user-images.githubusercontent.com/115678171/203445856-14a360f5-14c0-4334-8c99-5ac968b1e9fc.png)

````
#Latihan List ( Yoga Pratama )

#Membuat sebuah list sebanyak 5 elemen dengan nilai bebas
a = [1, 4, 6, 8, 9]
print("List A =", a,)
# *Akses List
print("Elemen ke 3 adalah       :", a[2]) #Menampikan elemen 3
print("Elemen ke 2 - 4 adalah   :", a[1:4]) #Menampilkan elemen 2-4
print("Elemen terakhir adalah   :", a[4]) #Menampilkan elemen terakhir

# *Ubah Elemen List
a[3] = 7
print("Elemen 4 > 7             :", a) #Mengubah elemen 4
a[3:5] = [7, 10]
print("Elemen 4-5 > 7, 10       :", a,"\n") #Mengubah elemen 4-5

# *Tambah Elemen List
a = [1, 4, 6, 8, 9]
b = [3, 7, 10, 11, 20]
print("List A =", a)
print("List B =", b)

b.extend(a[1:3])
print("Ambil 2 elemen A jadi List B     :",b) #Mengambil 2 bagian A jadi B

b = [3, 7, 10, 11, 20]
b.append("14")
print("Tambah nilai string ke list B    :",b) #Menambah list B dengan nilai string

b = [3, 7, 10, 11, 20]
b.extend([25, 28, 30])
print("Menambah 3 nilai ke list B       :",b) #Menambah list B dengan 3 nilai

b = [3, 7, 10, 11, 20]
b = b + a
print("Menggabung List B dengan A       :",b) #Menggabungkan list B dan A

```
    
2. Hasil Run

![Run Menginput nilai 5 elemen](https://user-images.githubusercontent.com/115678171/203446301-9c83c044-6c45-4077-91e3-50b90cfa9acb.png)

## Nilai Mahasiswa
Buat program sederhana untuk menambahkan data kedalam sebuah list dengan rincian sebagai berikut :

- Program meminta memasukkan data sebanyak-banyaknya (gunakan perulangan)
- Tampilkan pertanyaan untuk menambah data (ya/tidak?), apabila jawaban   
"tidak", maka program akan menampilkan daftar datanya.
- Nilai Akhir diambil dari perhitungan 3 komponen nilai (tugas: 30%, uts: 35%, uas: 35%)
- Buat flowchart dan penjelasan programnya pada README.md.
- Commit dan push repository ke github.

#### Langkah-langkah :
1. Buat programnya terlebih dahulu seperti gambar di bawah ini

![Nilai mahasiswa ](https://user-images.githubusercontent.com/115678171/203446485-233d3cdd-e0a4-4258-bc74-e082de91af4c.png)

# Membuat Tugas Praktikum
data =[]
while True :
nama       = input    ("Nama        : ")
nim        = input    ("NIM         : ")
tugas      = int(input("Nilai Tugas : "))
uts        = int(input("Nilai UTS   : "))
uas        = int(input("Nilai UAS   : "))
nilaiakhir = float(tugas)*30/100+(uts)*35/100+(uas)*35/100
data.append([nama,nim,tugas,uts,uas,nilaiakhir])
lagi= input("Tambah data (ya/tidak)? ")
if lagi.lower() =="tidak":
 break


    print("=====================================================================================");
    print("|  No  |     Nama     |     NIM     |   Tugas   |   UTS   |   UAS   |  Nilai Akhir  |");
    print("=====================================================================================");
    i=0
    for x in data:
        i+=1
        print("|  {6:2}  |  {0:10}  |  {1:9}  |  {2:7}  |  {3:5}  | {4:6}  |  {5:11.2f}  |"\
              .format (x[0][:9] , x[1][:9],x[2],x[3],x[4],x[5], i))
    print("=====================================================================================");
    
2. Hasil Run

![Screenshot (168)](https://user-images.githubusercontent.com/115867244/202901652-176749d1-4596-4aaf-97e2-9089ef153fc8.png)


### Penjelasan Program :
1. Buatlah list berupa Nama, NIM, Nilai Tugas, Nilai UTS, Nilai UAS.
2. Lalu inputlah Nama, NIM, Nilai Tugas, Nilai UTS, Nilai UAS.
3. Lalu mencari nilai akhir dengan perhitungan nilai tugas 30%, nilai uts 35% dan uas 35% , dengan perintah float
4. Gunakan perintah append pada Nama, NIM, Nilai tugas, Nilai UTS, Nilai UAS untuk menambahkan 1 item ke elemen terakhir.
5. Jika ingin menambah list data ketik "ya" dan jika tidak ingin menambahkan list data ketik "tidak". Dengan perintah while jawab =="ya" dan if jawab =="tidak". Jawab input("Tambah data (ya/tidak)").
6. Gunakanlah perulangan for, dengan perintah for i in range(len(Nama)):. Fungsi "len" ialah untuk mengembalikan panjang (jumlah anggota) dari suatu objek.
7. Lalu cetak dengan perintah print
8. Selesai

### Flowchart Praktikum 5

![Gambar WhatsApp 2022-11-20 pukul 21 12 36](https://user-images.githubusercontent.com/115867244/202907083-e47e04a1-78a6-4e86-bba2-c64ae8b4ee04.jpg)

### Sekian, Terima kasih 
