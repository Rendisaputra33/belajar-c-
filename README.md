# PERCABANGAN

## 🌱 Apa itu Percabangan?

**Percabangan** adalah cara agar program **bisa memilih tindakan** berdasarkan suatu kondisi.

👉 Contoh di kehidupan sehari-hari:

* **Kalau** hujan → bawa payung
* **Kalau tidak** → tidak perlu payung

Dalam C++, percabangan digunakan untuk **mengambil keputusan**.

---

## 1️⃣ `if` (Jika)

### 📌 Pengertian

`if` artinya **"jika"**.
Program akan menjalankan perintah **HANYA JIKA kondisi benar (true)**.

### ✏️ Contoh Kode

```cpp
int nilai = 80;

if (nilai >= 75) {
    cout << "Lulus";
}
```

### 🧠 Penjelasan

* Jika `nilai` **75 atau lebih** → tampilkan **Lulus**
* Jika kurang dari 75 → **tidak terjadi apa-apa**

---

## 2️⃣ `else` (Jika Tidak)

### 📌 Pengertian

`else` artinya **"jika tidak"**
Digunakan sebagai **pilihan kedua** jika kondisi `if` **salah (false)**.

### ✏️ Contoh Kode

```cpp
int nilai = 60;

if (nilai >= 75) {
    cout << "Lulus";
} else {
    cout << "Tidak Lulus";
}
```

### 🧠 Penjelasan

* Jika nilai ≥ 75 → **Lulus**
* Jika nilai < 75 → **Tidak Lulus**

👉 `else` **tidak punya kondisi**, dia otomatis dijalankan kalau `if` salah.

---

## 3️⃣ `else if` (Jika Tidak, Lalu Jika)

### 📌 Pengertian

`else if` digunakan **jika ada banyak kondisi** yang ingin dicek.

### ✏️ Contoh Kode

```cpp
int nilai = 85;

if (nilai >= 90) {
    cout << "A";
} else if (nilai >= 80) {
    cout << "B";
} else if (nilai >= 70) {
    cout << "C";
} else {
    cout << "D";
}
```

### 🧠 Penjelasan

Program membaca dari **atas ke bawah**:

1. Jika nilai ≥ 90 → A
2. Jika tidak, tapi nilai ≥ 80 → B
3. Jika tidak, tapi nilai ≥ 70 → C
4. Jika semua salah → D

⛔ Setelah satu kondisi **benar**, yang lain **tidak dicek lagi**.

---

## 4️⃣ Aturan Penting Percabangan C++

### ✅ 1. Kondisi harus menghasilkan **true atau false**

Contoh kondisi:

```cpp
nilai > 70
nilai == 100
umur <= 17
```

### ❌ Salah

```cpp
if (nilai = 80) // SALAH, ini assignment
```

### ✅ Benar

```cpp
if (nilai == 80)
```

---

### ✅ 2. Gunakan kurung kurawal `{}` untuk banyak perintah

```cpp
if (nilai >= 75) {
    cout << "Lulus";
    cout << "Selamat!";
}
```

---

### ✅ 3. Urutan `else if` itu penting

```cpp
if (nilai >= 70) {
    cout << "Lulus";
} else if (nilai >= 90) {
    cout << "Sangat Lulus";
}
```

⛔ **Salah urutan**, karena nilai 90 sudah lolos di `>= 70`

---

### ✅ 4. `else` selalu di bagian **paling akhir**

```cpp
if (...) {

} else if (...) {

} else {

}
```

---

## 5️⃣ Contoh Sederhana untuk Anak SMP

### 🎮 Contoh Game Nyawa

```cpp
int nyawa = 0;

if (nyawa > 0) {
    cout << "Game masih berjalan";
} else {
    cout << "Game Over";
}
```

---

### 📚 Contoh Umur

```cpp
int umur = 12;

if (umur < 13) {
    cout << "Anak-anak";
} else {
    cout << "Remaja";
}
```

---

## 📝 Ringkasan Singkat

| Kata      | Artinya            |
| --------- | ------------------ |
| `if`      | Jika kondisi benar |
| `else if` | Jika kondisi lain  |
| `else`    | Jika semua salah   |
| `==`      | Sama dengan        |
| `>`       | Lebih besar        |
| `<`       | Lebih kecil        |

---

Kalau mau, aku bisa:

* Buatkan **latihan soal + jawaban**
* Buat **contoh studi kasus sehari-hari**
* Atau versi **ringkas 1 halaman buat catatan sekolah**

Tinggal bilang saja 👍


