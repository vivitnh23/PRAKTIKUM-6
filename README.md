## Deskripsi Program Input Nilai Mahasiswa

Program ini dirancang untuk mengelola data nilai mahasiswa secara sederhana. Program ini memungkinkan pengguna untuk:

* Menambahkan data mahasiswa baru: Pengguna dapat memasukkan NIM, nama, nilai tugas, UTS, dan UAS. Program akan menghitung nilai akhir secara otomatis berdasarkan bobot yang telah ditentukan.
* Melihat daftar nilai: Program akan menampilkan semua data mahasiswa yang sudah tersimpan dalam format tabel yang mudah dibaca.
* Mengubah data mahasiswa: Pengguna dapat mengubah data mahasiswa yang sudah ada berdasarkan NIM.
* Menghapus data mahasiswa: Pengguna dapat menghapus data mahasiswa yang sudah tidak diperlukan.
* Mencari data mahasiswa: Pengguna dapat mencari data mahasiswa berdasarkan NIM.

## Flowchart 
![Flowchart](https://github.com/vivitnh23/PRAKTIKUM-6/blob/main/flowchart.drawio.png?raw=true)

## Kode Program 
``` python
data_mahasiswa = {}

def tampilkan_menu():
    print("\nProgram Input Nilai")
    print("=" * 50)
    print("[(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar]")
    pilihan = input("Pilih menu: ").lower()
    return pilihan

def tampilkan_data():
    print("\nDaftar Nilai")
    print("=" * 65)
    print("| NO |   NIM   |      NAMA      | TUGAS | UTS | UAS | AKHIR |")
    print("=" * 65)
    if not data_mahasiswa:
        print("|                       TIDAK ADA DATA                         |")
    else:
        for i, (nim, data) in enumerate(data_mahasiswa.items(), start=1):
            print(f"| {i:<2} | {nim:<7} | {data['nama']:<14} | {data['tugas']:<5} | {data['uts']:<3} | {data['uas']:<3} | {data['akhir']:<5.2f} |")
    print("=" * 65)

def tambah_data():
    nim = input("NIM: ")
    if nim in data_mahasiswa:
        print("NIM sudah ada. Gunakan opsi ubah data untuk mengganti.")
        return
    nama = input("Nama: ")
    tugas = float(input("Nilai Tugas: "))
    uts = float(input("Nilai UTS: "))
    uas = float(input("Nilai UAS: "))
    nilai_akhir = (tugas * 0.3) + (uts * 0.35) + (uas * 0.35)
    data_mahasiswa[nim] = {"nama": nama, "tugas": tugas, "uts": uts, "uas": uas, "akhir": nilai_akhir}
    print("Data berhasil ditambahkan.")

def ubah_data():
    nim = input("Masukkan NIM yang ingin diubah: ")
    if nim not in data_mahasiswa:
        print("NIM tidak ditemukan.")
        return
    print(f"Data saat ini: {data_mahasiswa[nim]}")
    nama = input("Masukkan Nama baru: ")
    tugas = float(input("Masukkan Nilai Tugas baru: "))
    uts = float(input("Masukkan Nilai UTS baru: "))
    uas = float(input("Masukkan Nilai UAS baru: "))
    nilai_akhir = (tugas * 0.3) + (uts * 0.35) + (uas * 0.35)
    data_mahasiswa[nim] = {"nama": nama, "tugas": tugas, "uts": uts, "uas": uas, "akhir": nilai_akhir}
    print("Data berhasil diubah.")

def hapus_data():
    nim = input("Masukkan NIM yang ingin dihapus: ")
    if nim in data_mahasiswa:
        del data_mahasiswa[nim]
        print("Data berhasil dihapus.")
    else:
        print("NIM tidak ditemukan.")

def cari_data():
    nim = input("Masukkan NIM yang ingin dicari: ")
    if nim in data_mahasiswa:
        data = data_mahasiswa[nim]
        print("\nData ditemukan:")
        print(f"NIM   : {nim}")
        print(f"Nama  : {data['nama']}")
        print(f"Tugas : {data['tugas']}")
        print(f"UTS   : {data['uts']}")
        print(f"UAS   : {data['uas']}")
        print(f"Akhir : {data['akhir']:.2f}")
    else:
        print("NIM tidak ditemukan.")

while True:
    pilihan = tampilkan_menu()
    if pilihan == "l":
        tampilkan_data()
    elif pilihan == "t":
        tambah_data()
    elif pilihan == "u":
        ubah_data()
    elif pilihan == "h":
        hapus_data()
    elif pilihan == "c":
        cari_data()
    elif pilihan == "k":
        print("Keluar dari program.")
        break
    else:
        print("Pilihan tidak valid. Silakan coba lagi.")

```

## Output Program 
````
Program Input Nilai
==================================================
[(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar]
Pilih menu:
Daftar Nilai
=================================================================
| NO |   NIM   |      NAMA      | TUGAS | UTS | UAS | AKHIR |
=================================================================
|                       TIDAK ADA DATA                         |
=================================================================

Program Input Nilai
==================================================
[(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar]
Pilih menu: T
NIM: 312410110
Nama: Vivit Nurul Hidayah
Nilai Tugas: 90
Nilai UTS: 95
Nilai UAS: 98
Data berhasil ditambahkan.

Program Input Nilai
==================================================
[(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar]
Pilih menu: T
NIM: 312410234
Nama: Jeon Jungkook 
Nilai Tugas: 90
Nilai UTS: 86
Nilai UAS: 90
Data berhasil ditambahkan.

Program Input Nilai
==================================================
[(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar]
Pilih menu: L

Daftar Nilai
=================================================================
| NO |   NIM   |      NAMA      | TUGAS | UTS | UAS | AKHIR |
=================================================================
| 1  | 312410110 | Vivit Nurul Hidayah | 90.0  | 95.0 | 98.0 | 94.55 |
| 2  | 312410234 | Jeon Jungkook  | 90.0  | 86.0 | 90.0 | 88.60 |
=================================================================

Program Input Nilai
==================================================
[(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar]
Pilih menu: K
Keluar dari program.
````


## Cara Kerja Program

Program ini bekerja dengan menggunakan struktur data dictionary dalam Python untuk menyimpan data mahasiswa. Setiap kunci dalam dictionary adalah NIM mahasiswa, dan nilainya adalah dictionary lain yang berisi informasi lengkap tentang mahasiswa tersebut (nama, nilai tugas, UTS, UAS, dan nilai akhir).

### Fungsi-fungsi Utama:

* tampilkan_menu(): Fungsi ini menampilkan menu pilihan kepada pengguna dan mengembalikan pilihan yang dipilih.
* tampilkan_data(): Fungsi ini menampilkan semua data mahasiswa yang tersimpan dalam format tabel.
* tambah_data(): Fungsi ini menambahkan data mahasiswa baru ke dalam dictionary.
* ubah_data(): Fungsi ini mengubah data mahasiswa yang sudah ada.
* hapus_data(): Fungsi ini menghapus data mahasiswa.
* cari_data(): Fungsi ini mencari data mahasiswa berdasarkan NIM.
