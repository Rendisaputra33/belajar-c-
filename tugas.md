### Deskripsi Masalah

Anda diminta membuat program kasir sederhana untuk menghitung total belanjaan pelanggan setelah dikurangi diskon berdasarkan **kategori barang** dan **total belanja**.

### Aturan Perhitungan

#### 1. Diskon Berdasarkan Kategori (`if - else if`)

Pelanggan harus memasukkan kode kategori barang (1, 2, atau 3):

* **Kategori 1 (Alat Musik):** Diskon 5% dari harga barang.
* **Kategori 2 (Pakaian Olahraga):** Diskon 10% dari harga barang.
* **Kategori 3 (Sepatu):** Diskon 15% dari harga barang.
* **Selain itu:** Tidak ada diskon kategori.

#### 2. Bonus Tambahan Belanja Banyak (`Logic Operator &&`)

Toko memberikan potongan tambahan sebesar **Rp 20.000** jika:

* Pelanggan membeli barang kategori 3 (Sepatu) **DAN** total harga barang (sebelum diskon) di atas **Rp 500.000**.

#### 3. Promo Member Baru (`Logic Operator ||`)

Pelanggan mendapatkan **Gratis Kaos Kaki** jika:

* Total belanja akhir (setelah semua diskon) di atas **Rp 750.000** **ATAU** pelanggan memiliki kode promo "DISKONAWAL".

---

### Tugas Anda:

1. Buat program C++ yang menerima input: Harga Barang, Kode Kategori (1-3), dan Status Promo (1 untuk punya, 0 untuk tidak).
2. Gunakan rangkaian `if - else if - else` untuk menentukan persentase diskon.
3. Gunakan operator logika `&&` untuk mengecek bonus tambahan.
4. Tampilkan: Total Diskon, Potongan Tambahan, dan Harga Akhir.

---

### Kerangka Kode

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    long hargaBarang;
    int kategori, punyaPromo;
    double persenDiskon = 0;
    long potonganTambahan = 0;

    cout << "=== Kasir Sporty-Go ===" << endl;
    cout << "Masukkan Harga Barang: "; cin >> hargaBarang;
    cout << "Masukkan Kategori (1-3): "; cin >> kategori;
    cout << "Punya Kode Promo? (1:Ya, 0:Tidak): "; cin >> punyaPromo;

    // 1. Tentukan Persen Diskon (if - else if)
    if (kategori == 1) {
        persenDiskon = 0.05;
    } 
    // ... lengkapi else if untuk kategori 2 dan 3 ...
    else {
        persenDiskon = 0;
    }

    // 2. Bonus Tambahan (Gunakan Operator &&)
    // Syarat: Kategori harus 3 DAN harga > 500000
    if (kategori == 3 && hargaBarang > 500000) {
        potonganTambahan = 20000;
    }

    // 3. Hitung Total Akhir
    double totalDiskon = hargaBarang * persenDiskon;
    double hargaAkhir = hargaBarang - totalDiskon - potonganTambahan;

    // 4. Cek Bonus Kaos Kaki (Gunakan Operator ||)
    if (hargaAkhir > 750000 || punyaPromo == 1) {
        cout << "Selamat! Anda mendapatkan Gratis Kaos Kaki." << endl;
    }

    cout << "Total Akhir: Rp " << hargaAkhir << endl;

    return 0;
}

```

---

**Saran Langkah Selanjutnya:**
Coba lengkapi bagian `else if` di atas. Jika sudah, apakah kamu ingin saya jelaskan lebih detail tentang perbedaan fungsi operator **`&&` (DAN)** dan **`||` (ATAU)** dalam soal di atas?
