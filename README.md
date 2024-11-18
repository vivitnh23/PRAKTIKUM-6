## Deskripsi Program Input Nilai Mahasiswa

Program ini dirancang untuk mengelola data nilai mahasiswa secara sederhana. Program ini memungkinkan pengguna untuk:

* Menambahkan data mahasiswa baru: Pengguna dapat memasukkan NIM, nama, nilai tugas, UTS, dan UAS. Program akan menghitung nilai akhir secara otomatis berdasarkan bobot yang telah ditentukan.
* Melihat daftar nilai: Program akan menampilkan semua data mahasiswa yang sudah tersimpan dalam format tabel yang mudah dibaca.
* Mengubah data mahasiswa: Pengguna dapat mengubah data mahasiswa yang sudah ada berdasarkan NIM.
* Menghapus data mahasiswa: Pengguna dapat menghapus data mahasiswa yang sudah tidak diperlukan.
* Mencari data mahasiswa: Pengguna dapat mencari data mahasiswa berdasarkan NIM.

## Flowchart 
![Flowchart](

## Cara Kerja Program

Program ini bekerja dengan menggunakan struktur data dictionary dalam Python untuk menyimpan data mahasiswa. Setiap kunci dalam dictionary adalah NIM mahasiswa, dan nilainya adalah dictionary lain yang berisi informasi lengkap tentang mahasiswa tersebut (nama, nilai tugas, UTS, UAS, dan nilai akhir).

### Fungsi-fungsi Utama:

* tampilkan_menu(): Fungsi ini menampilkan menu pilihan kepada pengguna dan mengembalikan pilihan yang dipilih.
* tampilkan_data(): Fungsi ini menampilkan semua data mahasiswa yang tersimpan dalam format tabel.
* tambah_data(): Fungsi ini menambahkan data mahasiswa baru ke dalam dictionary.
* ubah_data(): Fungsi ini mengubah data mahasiswa yang sudah ada.
* hapus_data(): Fungsi ini menghapus data mahasiswa.
* cari_data(): Fungsi ini mencari data mahasiswa berdasarkan NIM.

### Alur Kerja Umum:

1. Program memulai dengan mendefinisikan dictionary kosong data_mahasiswa untuk menyimpan data.
2. Program memasuki loop while True yang akan terus berjalan hingga pengguna memilih opsi "keluar".
3. Pada setiap iterasi loop, program menampilkan menu pilihan.
4. Pengguna memilih salah satu opsi yang tersedia.
5. Program akan menjalankan fungsi yang sesuai dengan pilihan pengguna.
6. Proses ini berulang hingga pengguna memilih opsi "keluar".

## Peningkatan yang Mungkin Dilakukan

* Validasi input: Program dapat dilengkapi dengan validasi input untuk memastikan data yang dimasukkan oleh pengguna valid (misalnya, NIM harus berupa angka, nilai harus berupa angka di antara 0 dan 100).
* Penyimpanan data: Data mahasiswa dapat disimpan ke dalam file (misalnya, CSV atau JSON) agar data tidak hilang ketika program dijalankan ulang.
* Pencarian yang lebih canggih: Program dapat dilengkapi dengan fitur pencarian yang lebih canggih, misalnya mencari berdasarkan rentang nilai atau nama mahasiswa.
* Antarmuka pengguna: Program dapat dilengkapi dengan antarmuka pengguna yang lebih menarik dan user-friendly, misalnya menggunakan library seperti Tkinter.
* Fitur tambahan: Program dapat dilengkapi dengan fitur tambahan seperti menghitung rata-rata nilai, mencari nilai tertinggi dan terendah, atau membuat grafik distribusi nilai.
