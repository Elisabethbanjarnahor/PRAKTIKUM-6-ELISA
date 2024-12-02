NAMA : ELISABETH ERNI BANJARNAHOR
NIM : 312410525
KLS : TI 24 A5


## ALGORITMA ##


1. Inisialisasi kamus `mahasiswa untuk menyimpan data mahasiswa.

2. Definisikan fungsi 'tambah_mahasiswa()`, `tampilkan_semua()`, `hapus_mahasiswa()', dan `ubah_nilai()`.

3. Masuki loop 'while True' untuk menampilkan menu interaktif dan menerima input pilihan dari pengguna.

4. Berdasarkan pilihan pengguna, panggil fungsi yang sesuai.

5. Jika pengguna memilih untuk keluar, hentikan loop 'while' dan akhiri program.


## FLOWCHART PROGRAM ##
![WhatsApp Image 2024-12-02 at 18 22 33_1e6e9e7c](https://github.com/user-attachments/assets/502119e1-09ab-40eb-bf29-9b7241d1ef9b)



## CODINGAN PROGRAM ##
```ruby
mahasiswa = {}  # Kamus untuk menyimpan data mahasiswa

def tambah_mahasiswa():
    nama = input("Masukkan nama mahasiswa: ")
    nilai = float(input("Masukkan nilai mahasiswa: "))
    mahasiswa[nama] = nilai
    print("Data mahasiswa berhasil ditambahkan.")

def tampilkan_semua():
    if not mahasiswa:
        print("Tidak ada data mahasiswa.")
    else:
        print("Data Mahasiswa:")
        for nama, nilai in mahasiswa.items():
            print(f"{nama}: {nilai}")

def hapus_mahasiswa():
    nama = input("Masukkan nama mahasiswa yang ingin dihapus: ")
    if nama in mahasiswa:
        del mahasiswa[nama]
        print("Data mahasiswa berhasil dihapus.")
    else:
        print("Data mahasiswa tidak ditemukan.")

def ubah_nilai():
    nama = input("Masukkan nama mahasiswa yang ingin diubah nilainya: ")
    if nama in mahasiswa:
        nilai_baru = float(input("Masukkan nilai baru: "))
        mahasiswa[nama] = nilai_baru
        print("Nilai mahasiswa berhasil diubah.")
    else:
        print("Data mahasiswa tidak ditemukan.")

while True:
    print("\nMenu:")
    print("1. Tambah data mahasiswa")
    print("2. Tampilkan semua data mahasiswa")
    print("3. Hapus data mahasiswa")
    print("4. Ubah nilai mahasiswa")
    print("5. Keluar")

    pilihan = input("Pilih menu: ")

    if pilihan == '1':
        tambah_mahasiswa()
    elif pilihan == '2':
        tampilkan_semua()
    elif pilihan == '3':
        hapus_mahasiswa()
    elif pilihan == '4':
        ubah_nilai()
    elif pilihan == '5':
        break
    else:
        print("Pilihan tidak valid.")
```
Penjelasan codingan :
1. **Deklarasi Kamus 'mahasiswa`:** python mahasiswa = {} # Kamus untuk menyimpan data mahasiswa
Kode ini mendeklarasikan kamus kosong bernama 'mahasiswa yang akan digunakan untuk menyimpan data mahasiswa. Kamus ini akan menyimpan pasangan kunci-nilai, di mana kunci adalah nama mahasiswa dan nilai adalah nilai mahasiswa.
2. **Fungsi `tambah_mahasiswa()':**
python def tambah_mahasiswa(): nama = input("Masukkan nama mahasiswa: ") nilai = float(input("Masukkan nilai mahasiswa: ")) mahasiswa [nama] = nilai print("Data mahasiswa berhasil ditambahkan.")
Fungsi ini meminta input nama dan nilai mahasiswa dari pengguna, kemudian menyimpannya ke dalam kamus `mahasiswa`. * `nama = input("Masukkan nama mahasiswa: ")'` : Meminta input nama mahasiswa dari pengguna. * `nilai = float(input("Masukkan nilai mahasiswa: ")): Meminta input nilai mahasiswa dari
pengguna dan mengubahnya menjadi tipe data float.
* `mahasiswa[nama] = nilai`: Menambahkan pasangan kunci-nilai ke dalam kamus `mahasiswa, dengan nama mahasiswa sebagai kunci dan nilai mahasiswa sebagai nilai. * `print("Data mahasiswa berhasil ditambahkan.")` : Menampilkan pesan konfirmasi bahwa data mahasiswa berhasil ditambahkan.
3. **Fungsi 'tampilkan_semua()`:** python
def tampilkan_semua(): if not mahasiswa: print("Tidak ada data mahasiswa.") else: print("Data Mahasiswa:") for nama, nilai in mahasiswa.items(): print(f"{nama): {nilai}")
Fungsi ini menampilkan semua data mahasiswa yang tersimpan dalam kamus 'mahasiswa`.
* `if not mahasiswa:': Memeriksa apakah kamus `mahasiswa kosong. Jika kosong, maka tidak ada data mahasiswa yang akan ditampilkan. * `print("Tidak ada data mahasiswa.")` :
Menampilkan pesan jika tidak ada data mahasiswa.
* `else:`: Jika kamus 'mahasiswa` tidak kosong, maka program akan menampilkan data mahasiswa.

* `print("Data Mahasiswa:")`: Menampilkan judul "Data Mahasiswa:".

* `for nama, nilai in mahasiswa.items():`: Melakukan iterasi melalui semua pasangan kunci- nilai dalam kamus 'mahasiswa`.

* `print(f"{nama}: (nilai}")`: Menampilkan nama mahasiswa dan nilainya.
4. **Fungsi 'hapus_mahasiswa()*:** python
def hapus_mahasiswa(): nama = input("Masukkan nama mahasiswa yang ingin dihapus: ") if nama in mahasiswa: del mahasiswa[nama] print("Data mahasiswa berhasil dihapus.")
else: print("Data mahasiswa tidak ditemukan.")
Fungsi ini meminta input nama mahasiswa yang ingin dihapus, kemudian menghapusnya dari kamus `mahasiswa`.

* `nama = input("Masukkan nama mahasiswayang ingin dihapus: ")`: Meminta input nama mahasiswa yang ingin dihapus dari pengguna.

* `if nama in mahasiswa:`: Memeriksa apakah nama mahasiswa yang ingin dihapus ada dalam kamus 'mahasiswa`.

* `del mahasiswa [nama]': Menghapus pasangan kunci-nilai dengan nama mahasiswa yang diberikan dari kamus `mahasiswa`.

* `print("Data mahasiswa berhasil dihapus.")` Menampilkan pesan konfirmasi bahwa data mahasiswa berhasil dihapus.

* `else:: Jika nama mahasiswa tidak ditemukan dalam kamus `mahasiswa', maka program akan menampilkan pesan bahwa data mahasiswa tidak ditemukan.

* `print("Data mahasiswa tidak ditemukan.")` : Menampilkan pesan jika data mahasiswa tidak ditemukan.
5. **Fungsi 'ubah_nilai()*:**
python def ubah_nilai(): nama = input("Masukkan nama mahasiswa yang ingin diubah nilainya: ") if nama in mahasiswa: nilai_baru = float(input("Masukkan nilai baru: ")) mahasiswa[nama] = nilai_baru
print("Nilai mahasiswa berhasil diubah.")
else:
print("Data mahasiswa tidak ditemukan.")

Fungsi ini meminta input nama mahasiswa yang ingin diubah nilainya, kemudian meminta input nilai baru dan mengupdate nilai mahasiswa tersebut dalam kamus `mahasiswa`.

* `nama = input("Masukkan nama mahasiswa yang ingin diubah nilainya: ")`: Meminta input nama mahasiswa yang ingin diubah nilainya dari pengguna.

* `if nama in mahasiswa:`: Memeriksa apakah nama mahasiswa yang ingin diubah nilainya ada dalam kamus 'mahasiswa`.

* `nilai_baru = float(input("Masukkan nilai baru: "))': Meminta input nilai baru dari pengguna dan mengubahnya menjadi tipe data float.

* `mahasiswa[nama] = nilai_baru`: Mengupdate nilai mahasiswa dengan nama yang diberikan dengan nilai baru.

* `print("Nilai mahasiswa berhasil diubah.")` : Menampilkan pesan konfirmasi bahwa nilai mahasiswa berhasil diubah.

* `else:: Jika nama mahasiswa tidak ditemukan dalam kamus 'mahasiswa, maka program akan menampilkan pesan bahwa data mahasiswa tidakditemukan.

* `print("Data mahasiswa tidak ditemukan.")` : Menampilkan pesan jika data mahasiswa tidak ditemukan.
6. **Loop 'while True:**

python

while True:

print("

Menu:")

print("1. Tambah data mahasiswa")

print("2. Tampilkan semua data mahasiswa")

print("3. Hapus data mahasiswa")

print("4. Ubah nilai mahasiswa")

print("5. Keluar")

pilihan = input("Pilih menu: ")

if pilihan == '1':

tambah_mahasiswa()

elif pilihan == '2':

tampilkan_semua()

elif pilihan == '3':

hapus_mahasiswa()

elif pilihan == '4':

ubah_nilai()

elif pilihan == '5':
break

else:

print("Pilihan tidak valid.")

Kode ini merupakan loop utama program yang akan terus berjalan hingga pengguna memilih untuk keluar. Di dalam loop, program menampilkan menu interaktif yang berisi pilihan untuk menambahkan, menampilkan, menghapus, mengubah data mahasiswa, dan keluar.

* `print("

Menu:"): Menampilkan judul "Menu:".

* `print("1. Tambah data mahasiswa")` :

Menampilkan pilihan 1 untuk menambahkan data mahasiswa.

* `print("2. Tampilkan semua data mahasiswa")' : Menampilkan pilihan 2 untuk menampilkan semua data mahasiswa.

* `print("3. Hapus data mahasiswa")`: Menampilkan pilihan 3 untuk menghapus data mahasiswa.

* `print("4. Ubah nilai mahasiswa")`: Menampilkan pilihan 4 untuk mengubah nilai mahasiswa.

* `print("5. Keluar")': Menampilkan pilihan 5 untuk keluar dari program.

* `pilihan = input("Pilih menu: ")': Meminta input pilihan dari pengguna.

* `if pilihan == '1':': Jika pengguna memilih pilihan 1, maka program akan memanggil fungsi tambah_mahasiswa()`.

* `elif pilihan == '2':': Jika pengguna memilih pilihan 2, maka program akan memanggil fungsi tampilkan_semua()`.

* `elif pilihan == '3':': Jika pengguna memilih pilihan 3, maka program akan memanggil fungsi hapus_mahasiswa()`.

* `elif pilihan == '4':': Jika pengguna memilih pilihan 4, maka program akan memanggil fungsi `ubah_nilai()`.

* `elif pilihan == '5':': Jika pengguna memilih pilihan 5, maka program akan keluar dari loop `while' dan program akan berakhir.

* `else:`: Jika pengguna memilih pilihan yang tidak valid, maka program akan menampilkan pesan "Pilihan tidak valid.".

## HASIL CODINGAN ##

★★SEKIAN DAN TERIMA KASIH★★
