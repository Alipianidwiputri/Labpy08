# Bahasa Pemograman Pertemuan 12

# Labpy08

# Diagram Class

![Screenshot 2024-12-05 131826](https://github.com/user-attachments/assets/42295bba-d0ef-4d96-866b-14d657b7c1ca)

# Flowchart

![Screenshot 2024-12-05 131910](https://github.com/user-attachments/assets/e75e5bb0-695b-4852-acd2-fdf4a3c8e400)

# Penjelasan code

Berikut adalah penjelasan dari kode program Python yang telah dibuat untuk mengelola data mahasiswa, termasuk penjelasan tentang setiap bagian dari kode tersebut:

# 1. Class Mahasiswa
```
def __init__(self):
    self.daftar_mahasiswa = []
```
- Ini adalah constructor class yang menginisialisasi list kosong untuk menyimpan data mahasiswa
- Menggunakan list of dictionaries untuk menyimpan data setiap mahasiswa

# 2. Metode Tambah
```
def tambah(self, nama, nim, nilai):
    # Validasi input
    if not isinstance(nim, int) or not isinstance(nilai, int):
        print("Error: NIM dan nilai harus berupa angka.")
        return
    if nilai < 0 or nilai > 100:
        print("Error: Nilai harus berada antara 0-100.")
        return
```
- Memeriksa apakah NIM dan nilai berupa angka menggunakan isinstance()
- Memvalidasi nilai harus dalam rentang 0-100
- Memeriksa apakah NIM sudah ada untuk mencegah duplikasi
- Jika semua validasi berhasil, data mahasiswa ditambahkan ke list

# 3. Metode Tampilkan
```
def tampilkan(self):
    if not self.daftar_mahasiswa:
        print("Daftar mahasiswa kosong.")
        return
        
    print("\nDaftar Mahasiswa:")
    print("-" * 50)
    print(f"{'No':3} | {'Nama':15} | {'NIM':10} | {'Nilai':5} | {'Status':8}")
```
- Memeriksa apakah daftar kosong
- Menampilkan data dalam format tabel dengan header
- Menghitung dan menampilkan statistik:
  - Rata-rata nilai
  - Jumlah mahasiswa yang lulus (nilai ≥ 60)
  - Jumlah mahasiswa yang gagal

# 4. Metode Hapus
```
def hapus(self, nama):
    before_length = len(self.daftar_mahasiswa)
    self.daftar_mahasiswa = [m for m in self.daftar_mahasiswa if m['nama'].lower() != nama.lower()]
```
- Menggunakan list comprehension untuk membuat list baru tanpa mahasiswa yang dihapus
- Membandingkan panjang list sebelum dan sesudah untuk menentukan apakah penghapusan berhasil
- Pencarian nama bersifat case-insensitive (tidak sensitif huruf besar/kecil)

# 5. Metode Ubah
```
def ubah(self, nama, nim_baru, nilai_baru):
    # Validasi input
    if not isinstance(nim_baru, int) or not isinstance(nilai_baru, int):
        print("Error: NIM dan nilai harus berupa angka.")
        return
```
- Melakukan validasi input seperti pada metode tambah
- Memeriksa apakah NIM baru sudah digunakan oleh mahasiswa lain
- Mencari mahasiswa berdasarkan nama (case-insensitive)
- Mengupdate data jika ditemukan

# 6. Fungsi Main
```
def main():
    mhs = Mahasiswa()
    
    while True:
        try:
            print("\nMenu Manajemen Data Mahasiswa:")
            # ... menu options ...
```
- Membuat instance dari class Mahasiswa
- Menampilkan menu dalam loop while
- Menggunakan try-except untuk menangani error:
  - ValueError untuk input yang tidak valid
  - KeyboardInterrupt untuk menghentikan program (Ctrl+C)
  - Exception umum untuk error lainnya

# 7. Fitur Keamanan dan Error Handling:
- Validasi input untuk mencegah data yang tidak valid
- Pencegahan duplikasi NIM
- Penanganan kesalahan untuk input yang tidak sesuai
- Konfirmasi operasi berhasil atau gagal
- Case-insensitive search untuk kemudahan penggunaan

# 8. Fitur Tambahan:
- Status kelulusan otomatis (Lulus/Gagal)
- Statistik ringkasan (rata-rata, jumlah lulus/gagal)
- Formatting tabel untuk tampilan yang lebih rapi
- Pesan error yang informatif
- Validasi rentang nilai (0-100)

# 9. Best Practices yang Diterapkan:
- Kode terstruktur dan modular
- Validasi input yang ketat
- Error handling yang komprehensif
- Penamaan variabel yang jelas
- Komentar untuk menjelaskan fungsi kode
- Pemisahan logika program ke dalam fungsi-fungsi

   # Penjelasan Diagram class

   # Struktur  Class

   # 1. Kelas Mahasiswa

   Deskripsi

- Kelas ini adalah inti dari manajemen data mahasiswa, bertanggung jawab untuk mengelola seluruh operasi pada data mahasiswa.
- 
Atribut

-      daftar_mahasiswa (private list):
Menyimpan kumpulan data mahasiswa
Bersifat privat untuk melindungi integritas data

**Metode**

1.     __init__():

- Konstruktor kelas
- Menginisialisasi list kosong untuk menyimpan data mahasiswa
2.     tambah(nama, nim, nilai):

- Menambahkan mahasiswa baru ke dalam daftar
- Menerima parameter nama, NIM, dan nilai
- Membuat entri baru dalam daftar mahasiswa

3.     tampilkan():

- Menampilkan seluruh data mahasiswa yang tersimpan
- Menangani kasus daftar kosong
- Menampilkan informasi setiap mahasiswa termasuk nama, NIM, dan nilai

4.     hapus(nama):

- Menghapus data mahasiswa berdasarkan nama
- Mencari mahasiswa dengan nama tertentu
- Menghapus entri jika ditemukan
- Memberikan konfirmasi atau pesan kesalahan

5.     ubah(nama, nim_baru, nilai_baru):

- Mengubah data mahasiswa yang sudah ada
- Mencari mahasiswa berdasarkan nama
- Memperbarui NIM dan nilai
- Memberikan konfirmasi perubahan

# 2. Kelas DataMahasiswa

**Deskripsi**

- Kelas ini merupakan struktur data untuk menyimpan informasi individual setiap mahasiswa.

**Atribut**

- nama (string): Nama lengkap mahasiswa
- nim (integer): Nomor Induk Mahasiswa
- nilai (integer): Nilai akademik mahasiswa

# 3. Kelas Main
**Deskripsi**

- Kelas yang bertanggung jawab untuk menjalankan program dan berinteraksi dengan pengguna.

**Metode**

1.     main():

- Fungsi utama untuk menjalankan program
- Membuat instance kelas Mahasiswa
- Memulai loop utama program

2.     tampilkan_menu():

- Menampilkan pilihan menu kepada pengguna
- Memudahkan interaksi dan navigasi program

3.     pilih_menu():

- Memproses pilihan menu yang dipilih pengguna
- Memanggil metode yang sesuai dari kelas Mahasiswa

# Hubungan Antar Kelas

**Komposisi (Mahasiswa -- 0.. DataMahasiswa)**

- Kelas Mahasiswa mengandung beberapa objek DataMahasiswa
- Hubungan komposisi berarti objek DataMahasiswa tidak dapat eksis tanpa Mahasiswa
- Satu objek Mahasiswa dapat memiliki 0 atau lebih objek DataMahasiswa

**Asosiasi (Main ..> Mahasiswa)**

- Kelas Main menggunakan (uses) kelas Mahasiswa
- Main bergantung pada fungsionalitas Mahasiswa untuk menjalankan program
