print('-----------------------------')
print('Nama    :Yeheskiel Darmawan  ')
print('Nim     :2509116027          ')
print('Prodi   :Sistem Informasi    ')
print('-----------------------------')

# =============================
# Program Pencatatan Data Mata Uang Dunia
# Dengan Sistem Login & Role (Manager / Karyawan)
# Fitur: CRUD + Error Handling
# =============================

# Data user (username, password, role)
users = {
    "manager": {"password": "1234", "role": "manager"},
    "karyawan": {"password": "1111", "role": "karyawan"}
}

# Data mata uang dunia
currencies = {
    "USD": 1.0,        # Dolar Amerika
    "EUR": 0.92,       # Euro
    "GBP": 0.80,       # Poundsterling
    "JPY": 147.75,     # Yen Jepang
    "AUD": 1.50,       # Dolar Australia
    "CAD": 1.38,       # Dolar Kanada
    "SGD": 1.28,       # Dolar Singapura
    "CHF": 0.89,       # Franc Swiss
    "CNY": 7.12,       # Yuan Tiongkok
    "INR": 83.70,      # Rupee India
    "IDR": 16458.38,   # Rupiah Indonesia
    "MYR": 4.20,       # Ringgit Malaysia
    "THB": 35.50,      # Baht Thailand
    "KRW": 1305.0,     # Won Korea Selatan
    "ZAR": 19.60       # Rand Afrika Selatan
}


# =============================
# Fungsi CRUD
# =============================
def create():
    try:
        code = input("Masukkan kode mata uang (contoh: USD, IDR): ").upper()
        if code in currencies:
            print(f"{code} sudah ada dalam data.")
            return
        value = float(input(f"Masukkan nilai kurs {code}: "))
        currencies[code] = value
        print(f"Data {code} berhasil ditambahkan.")
    except ValueError:
        print("Input harus berupa angka untuk nilai kurs!")


def read():
    if not currencies:
        print("Belum ada data mata uang.")
        return

    print("\n=== Data Mata Uang Dunia ===")
    print(f"{'Kode':<8}{'Nilai Kurs (vs USD)':>20}")
    print("-" * 28)
    for code, value in sorted(currencies.items()):
        print(f"{code:<8}{value:>20}")


def update():
    code = input("Masukkan kode mata uang yang ingin diupdate: ").upper()
    if code in currencies:
        try:
            new_value = float(input(f"Masukkan nilai kurs baru untuk {code}: "))
            currencies[code] = new_value
            print(f"Data {code} berhasil diperbarui.")
        except ValueError:
            print("Input harus berupa angka!")
    else:
        print(f"{code} tidak ditemukan.")


def delete():
    code = input("Masukkan kode mata uang yang ingin dihapus: ").upper()
    if code in currencies:
        del currencies[code]
        print(f"Data {code} berhasil dihapus.")
    else:
        print(f"{code} tidak ditemukan.")


# =============================
# Menu Manager & Karyawan
# =============================
def menu_manager():
    while True:
        print("\n=== MENU MANAGER ===")
        print("1. Tambah Data (Create)")
        print("2. Lihat Data (Read)")
        print("3. Update Data")
        print("4. Hapus Data")
        print("5. Logout")

        pilihan = input("Pilih menu (1-5): ")

        if pilihan == "1":
            create()
        elif pilihan == "2":
            read()
        elif pilihan == "3":
            update()
        elif pilihan == "4":
            delete()
        elif pilihan == "5":
            print("Logout berhasil.\n")
            break
        else:
            print("Pilihan tidak valid!")


def menu_karyawan():
    while True:
        print("\n=== MENU KARYAWAN ===")
        print("1. Lihat Data (Read)")
        print("2. Logout")

        pilihan = input("Pilih menu (1-2): ")

        if pilihan == "1":
            read()
        elif pilihan == "2":
            print("Logout berhasil.\n")
            break
        else:
            print("Pilihan tidak valid!")


# =============================
# Sistem Login
# =============================
def login():
    print("\n=== LOGIN SISTEM ===")
    username = input("Username: ").strip()
    password = input("Password: ").strip()

    if username in users and users[username]["password"] == password:
        role = users[username]["role"]
        print(f"\nLogin berhasil — role: {role}")
        if role == "manager":
            menu_manager()
        else:
            menu_karyawan()
    else:
        print("Login gagal — username atau password salah.")


# =============================
# Main Program
# =============================
while True:
    login()
