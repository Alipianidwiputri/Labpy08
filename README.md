# Bahasa Pemograman Pertemuan 12

# Labpy08

# Diagram Class

![Screenshot 2024-12-05 131826](https://github.com/user-attachments/assets/42295bba-d0ef-4d96-866b-14d657b7c1ca)

# Flowchart

![Screenshot 2024-12-05 131910](https://github.com/user-attachments/assets/e75e5bb0-695b-4852-acd2-fdf4a3c8e400)

# Penjelasan code

Berikut adalah penjelasan dari kode program Python yang telah dibuat untuk mengelola data mahasiswa, termasuk penjelasan tentang setiap bagian dari kode tersebut:

1. Import dan Definisi Kelas

       def __init__(self):
        self.daftar_mahasiswa = []
- class Mahasiswa: Mendefinisikan kelas Mahasiswa yang akan digunakan untuk mengelola data mahasiswa.
- init: Merupakan metode konstruktor yang dipanggil saat objek dari kelas ini dibuat. Di sini, kita menginisialisasi atribut daftar_mahasiswa sebagai list kosong yang akan menyimpan data mahasiswa.

2. Method tambah

       self.daftar_mahasiswa.append({'nama': nama, 'nim': nim, 'nilai': nilai})
       print(f"Data mahasiswa {nama} (NIM: {nim}) berhasil ditambahkan.")
- tambah(self, nama, nim, nilai): Method ini digunakan untuk menambahkan data mahasiswa baru ke dalam daftar.
- self.daftar_mahasiswa.append(...): Menambahkan dictionary yang berisi nama, nim, dan nilai mahasiswa ke dalam list daftar_mahasiswa.
- print(...): Menampilkan pesan konfirmasi bahwa data mahasiswa telah berhasil ditambahkan.

3. Method tampilkan

       if not self.daftar_mahasiswa:
        print("Daftar mahasiswa kosong.")
        return
       print("Daftar Mahasiswa:")
       for index, mahasiswa in enumerate(self.daftar_mahasiswa, start=1):
        print(f"{index}. Nama: {mahasiswa['nama']}, NIM: {mahasiswa['nim']}, Nilai: {mahasiswa['nilai']}")
- tampilkan(self): Method ini digunakan untuk menampilkan semua data mahasiswa yang ada dalam daftar.
- if not self.daftar_mahasiswa:: Memeriksa apakah daftar mahasiswa kosong. Jika kosong, program akan menampilkan pesan dan keluar dari method.
- enumerate(...): Menggunakan fungsi enumerate untuk mendapatkan indeks dan data mahasiswa saat iterasi. Indeks dimulai dari 1.
- print(...): Menampilkan informasi mahasiswa dalam format yang terstruktur.

4. Method hapus

       for mahasiswa in self.daftar_mahasiswa:
        if mahasiswa['nama'] == nama:
            self.daftar_mahasiswa.remove(mahasiswa)
            print(f"Data mahasiswa {nama} berhasil dihapus.")
            return
       print(f"Data mahasiswa {nama} tidak ditemukan.")
- hapus(self, nama): Method ini digunakan untuk menghapus data mahasiswa berdasarkan nama.
- for mahasiswa in self.daftar_mahasiswa:: Melakukan iterasi melalui daftar mahasiswa.
- if mahasiswa['nama'] == nama:: Memeriksa apakah nama mahasiswa yang ingin dihapus ada dalam daftar.
- self.daftar_mahasiswa.remove(mahasiswa): Menghapus mahasiswa dari daftar jika ditemukan.
- print(...): Menampilkan pesan konfirmasi atau pesan bahwa mahasiswa tidak ditemukan.

5. Method ubah

       for mahasiswa in self.daftar_mahasiswa:
        if mahasiswa['nama'] == nama:
            mahasiswa['nim'] = nim_baru
            mahasiswa['nilai'] = nilai_baru
            print(f"Data mahasiswa {nama} berhasil diubah menjadi NIM {nim_baru} dan nilai {nilai_baru}.")
            return
       print(f"Data mahasiswa {nama} tidak ditemukan.")
- ubah(self, nama, nim_baru, nilai_baru): Method ini digunakan untuk mengubah data mahasiswa berdasarkan nama.
- if mahasiswa['nama'] == nama:: Memeriksa apakah nama mahasiswa yang ingin diubah ada dalam daftar.
- mahasiswa['nim'] = nim_baru dan mahasiswa['nilai'] = nilai_baru: Mengubah NIM dan nilai mahasiswa yang ditemukan.
- print(...): Menampilkan pesan konfirmasi atau pesan bahwa mahasiswa tidak ditemukan.

6. Menu Interaktif

       mhs = Mahasiswa()
    
       while True:
        print("\nMenu:")
        print("1. Tambah Mahasiswa")
        print("2. Tampilkan Mahasiswa")
        print("3. Ubah Mahasiswa")
        print("4. Hapus Mahasiswa")
        print("5. Keluar")
        
        pilihan = input("Pilih menu (1-5): ")
        
        if pilihan

   # Penjelasan Diagram class

   # Struktur  Class

   # 1. Kelas Mahasiswa

   Deskripsi

- Kelas ini adalah inti dari manajemen data mahasiswa, bertanggung jawab untuk mengelola seluruh operasi pada data mahasiswa.
- 
Atribut

1.     daftar_mahasiswa (private list):
Menyimpan kumpulan data mahasiswa
Bersifat privat untuk melindungi integritas data
Metode

2.     __init__():

Konstruktor kelas
Menginisialisasi list kosong untuk menyimpan data mahasiswa
tambah(nama, nim, nilai):

Menambahkan mahasiswa baru ke dalam daftar
Menerima parameter nama, NIM, dan nilai
Membuat entri baru dalam daftar mahasiswa
tampilkan():

Menampilkan seluruh data mahasiswa yang tersimpan
Menangani kasus daftar kosong
Menampilkan informasi setiap mahasiswa termasuk nama, NIM, dan nilai
hapus(nama):

Menghapus data mahasiswa berdasarkan nama
Mencari mahasiswa dengan nama tertentu
Menghapus entri jika ditemukan
Memberikan konfirmasi atau pesan kesalahan
ubah(nama, nim_baru, nilai_baru):

Mengubah data mahasiswa yang sudah ada
Mencari mahasiswa berdasarkan nama
Memperbarui NIM dan nilai
Memberikan konfirmasi perubahan
