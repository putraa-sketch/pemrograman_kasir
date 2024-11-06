# Program Kasir

Program kasir ini dibuat untuk memudahkan proses transaksi penjualan, dengan fitur-fitur seperti menambah barang ke keranjang, menampilkan daftar barang, menghitung total harga, dan mencetak struk belanja.

## Struktur Data

Program ini menggunakan tiga kelas utama untuk mengorganisir data:

### class `Item`
Kelas `Item` digunakan untuk menyimpan informasi setiap barang yang dijual.

```python
class Item:
    def __init__(self, nama, harga, jumlah):
        self.nama = nama
        self.harga = harga
        self.jumlah = jumlah
```

**Penjelasan:**
- `nama`: Menyimpan nama barang.
- `harga`: Menyimpan harga jual barang.
- `jumlah`: Menyimpan jumlah barang yang dibeli.

- **Implementasi:**
- Saat membuat program kasir, kita perlu membuat objek `Item` untuk setiap jenis item yang dijual, dengan menyediakan nama, harga, dan jumlah.
- Objek `Item` ini akan digunakan di seluruh program, terutama saat menambahkan Item ke keranjang dan menampilkan daftar Item.

- ### class `Keranjang`
class `Keranjang` digunakan untuk menyimpan detail setiap item dalam keranjang belanja.

```python

