# Program Kasir

Program kasir ini dibuat untuk memudahkan proses transaksi penjualan, dengan fitur-fitur seperti menambah barang ke keranjang, menampilkan daftar barang, menghitung total harga, dan mencetak struk belanja.

# Code Project Program Kasir 
```
class Item:
    def __init__(self, nama, harga, jumlah):
        self.nama = nama
        self.harga = harga
        self.jumlah = jumlah

class Keranjang:
    def __init__(self):
        self.items = []
    
    def tambah_barang(self, nama, harga, jumlah):
        item = Item(nama, harga, jumlah)
        self.items.append(item)
        print(f"{jumlah} x {nama} telah ditambahkan ke keranjang.")
    
    def tampilkan_daftar_barang(self):
        if not self.items:
            print("Keranjang kosong.")
            return
        print("Daftar Barang di Keranjang:")
        for item in self.items:
            print(f"{item.nama} - {item.jumlah} x Rp{item.harga} = Rp{item.harga * item.jumlah}")
    
    def hitung_total(self):
        total = sum(item.harga * item.jumlah for item in self.items)
        return total
    
    def cetak_struk(self):
        print("\n===== STRUK PEMBELIAN =====")
        self.tampilkan_daftar_barang()
        total = self.hitung_total()
        print(f"Total Harga: Rp{total}")
        print("===== TERIMA KASIH =====\n")
```

# Contoh Penggunaan
```
keranjang = Keranjang()

keranjang.tambah_barang("Magnum Filter", 26000, 2)
keranjang.tambah_barang("Juara Jambu Kretek", 15000, 1)

keranjang.tambah_barang("Golda Coffe", 3500, 3)

keranjang.tampilkan_daftar_barang()

keranjang.cetak_struk()
```


# Output Dari Codingan Project Program Kasir
![Screenshot 2024-11-07 013717](https://github.com/user-attachments/assets/35417c16-03b7-4173-af38-6e2b2baf4cde)



# Penjelasan Singkat Mengenai Algoritma Pada Project Program Kasir

- Membuat kelas Item: Kelas Barang menyimpan data tentang barang, termasuk nama, harga satuan, dan jumlah.

- Membuat kelas Keranjang: Kelas Keranjang menyimpan daftar barang yang dibeli dan menyediakan fungsi untuk menambah barang, menampilkan barang, menghitung total harga, dan mencetak struk.

- Menambahkan barang ke keranjang: Program meminta pengguna untuk memasukkan nama barang, harga satuan, dan jumlah, lalu membuat objek Barang baru dengan data tersebut dan menambahkannya ke dalam keranjang.

- Menampilkan daftar barang: Program menampilkan daftar barang yang ada di keranjang, termasuk nama, harga satuan, jumlah, dan total harga per barang.

- Menghitung total harga: Program menghitung total harga semua barang di keranjang.

- Mencetak struk: Program mencetak struk yang berisi daftar barang, total harga, dan ucapan terima kasih.
