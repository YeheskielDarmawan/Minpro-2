Nama    : Yeheskiel Darmawan
Nim     : 2509116027
Jurusan : Sistem Informasi

Baik, saya akan jelaskan apas aja yang di coding

1. Judul
Program Pencatatan Data Mata Uang Dunia dengan Sistem Login dan Hak Akses (Manager dan Karyawan).

2. Tujuan
1. Membuat aplikasi sederhana untuk mencatat dan mengelola data kurs mata uang dunia.
2. Menerapkan konsep CRUD (Create, Read, Update, Delete) pada data mata uang.
3. Menerapkan sistem login dengan role-based access (Manager dan Karyawan).
4. Melakukan error handling untuk mengantisipasi input yang salah.

3. Dasar Teori
CRUD adalah operasi dasar dalam pengolahan data, yaitu Create (menambah), Read (membaca/menampilkan), Update (mengubah), dan Delete (menghapus).
Role-based access control (RBAC) adalah mekanisme keamanan di mana setiap user diberikan hak akses sesuai dengan perannya.
Error handling dalam Python dilakukan dengan try-except, untuk mencegah program berhenti ketika terjadi kesalahan input.

4. Analisis Program
4.1 Data User
users = {
    "manager": {"password": "1234", "role": "manager"},
    "karyawan": {"password": "1111", "role": "karyawan"}
}
Manager: username = manager, password = 1234.
Karyawan: username = karyawan, password = 1111.

4.2 Data Mata Uang
currencies = {
    "USD": 1.0,
    "EUR": 0.92,
    "GBP": 0.80,
    "JPY": 147.75,
    "IDR": 15648.38,
}

Berisi kurs beberapa mata uang terhadap USD.

4.3 Fungsi CRUD
Create: Menambah data kurs baru.
Read: Menampilkan semua data kurs.
Update: Mengubah nilai kurs yang sudah ada.
Delete: Menghapus data kurs.

4.4 Menu Program
Menu Manager:
1. Tambah Data
2. Lihat Data
3. Update Data
4. Hapus Data
5. Logout
Menu Karyawan:
1. Lihat Data
2. Logout
   
4.5 Sistem Login
User memasukkan username dan password.
Jika benar → diarahkan ke menu sesuai role.
Jika salah → muncul pesan error.

5. Flow Program (Alur Kerja)
1. Program dimulai → menampilkan menu login.
2. User memasukkan username dan password.
3. Jika login berhasil:
Jika Manager → bisa melakukan semua operasi CRUD.
Jika Karyawan → hanya bisa melihat data.
4. Jika login gagal → tampil pesan error, kembali ke login.
5. User bisa logout dan login kembali dengan akun lain
6. Kesimpulan
Program berhasil menerapkan sistem login dengan role manager dan karyawan.
Manager dapat mengelola data (CRUD), sedangkan Karyawan hanya dapat melihat data.
Penggunaan CRUD dan error handling membuat program lebih terstruktur dan aman dari kesalahan input.

FLOWCHART
<img width="1024" height="1536" alt="Diagram Manajemen Sistem Mata Uang" src="https://github.com/user-attachments/assets/3819de8c-9dd7-4b54-9988-f3eeb4cb3368" />

pthon
<img width="1920" height="1080" alt="Screenshot (37)" src="https://github.com/user-attachments/assets/50f8c0b8-809c-4106-b3ce-d786d211fbc3" />
<img width="1920" height="1080" alt="Screenshot (38)" src="https://github.com/user-attachments/assets/6719434b-2887-47f0-8124-d1cea7e076ef" />
<img width="1920" height="1080" alt="Screenshot (39)" src="https://github.com/user-attachments/assets/01f75810-3250-4ddf-b4f4-c189dcf0fc07" />
<img width="1920" height="1080" alt="Screenshot (40)" src="https://github.com/user-attachments/assets/6f5f819c-eab8-4c46-8982-380c8fb4dba6" />
<img width="1920" height="1080" alt="Screenshot (41)" src="https://github.com/user-attachments/assets/dfcaec51-5e39-4e9f-ae85-9364f29cfa0c" />

output diterminal
Penjelasan Output di Terminal Berdasarkan Role
🔹 1. Saat Program Pertama Kali Dijalankan

Output identitas selalu muncul lebih dulu:

Nama    : Yeheskiel Darmawan
Nim     : 2509116027
Prodi   : Sistem Informasi


Kemudian masuk ke menu login:

=== LOGIN SISTEM ===
Username: 
Password: 

🔹 2. Jika Login sebagai Manager

Jika username = manager dan password = 1234:

Login berhasil! Selamat datang, manager.


Program menampilkan Menu Manager:

=== MENU MANAGER ===
1. Tambah Data
2. Lihat Data
3. Update Data
4. Hapus Data
5. Logout
Pilih menu (1-5): 


Contoh output saat lihat data:

=== Daftar Kurs Mata Uang ===
USD : 1.0
EUR : 0.92
GBP : 0.8
JPY : 147.75
IDR : 15648.38
...


Contoh output saat tambah data berhasil:

Masukkan kode mata uang: PHP
Masukkan nilai kurs: 58.5
Data berhasil ditambahkan.


Contoh output saat update data berhasil:

Masukkan kode mata uang yang ingin diupdate: IDR
Masukkan nilai kurs baru: 15600
Data berhasil diperbarui.


Contoh output saat hapus data berhasil:

Masukkan kode mata uang yang ingin dihapus: JPY
Data berhasil dihapus.


Jika logout:

Logout berhasil.

🔹 3. Jika Login sebagai Karyawan

Jika username = karyawan dan password = 1111:

Login berhasil! Selamat datang, karyawan.


Program menampilkan Menu Karyawan:

=== MENU KARYAWAN ===
1. Lihat Data
2. Logout
Pilih menu (1-2): 


Jika pilih lihat data, hasilnya sama seperti Manager, contoh:

=== Daftar Kurs Mata Uang ===
USD : 1.0
EUR : 0.92
GBP : 0.8
JPY : 147.75
IDR : 15648.38
...


Jika logout:

Logout berhasil.

✨ Perbedaan Utama Output

Manager → bisa menambah, melihat, mengupdate, dan menghapus data (CRUD).

Karyawan → hanya bisa melihat data dan logout.

Mau saya buatkan perbandin


<img width="1920" height="1080" alt="Screenshot (42)" src="https://github.com/user-attachments/assets/90104887-f8bf-49b9-896a-ea2875f23762" />
<img width="1920" height="1080" alt="Screenshot (43)" src="https://github.com/user-attachments/assets/aa3fb36e-620f-4b31-9d3a-53796a068028" />

