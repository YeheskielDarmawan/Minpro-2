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


<img width="1024" height="1536" alt="Diagram Manajemen Sistem Mata Uang" src="https://github.com/user-attachments/assets/3819de8c-9dd7-4b54-9988-f3eeb4cb3368" />


<img width="1920" height="1080" alt="Screenshot (41)" src="https://github.com/user-attachments/assets/fdac9a42-0973-4373-8123-d3a886095366" />
