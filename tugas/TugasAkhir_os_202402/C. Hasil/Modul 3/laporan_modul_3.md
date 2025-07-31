# 📝 Laporan Tugas Akhir

**Mata Kuliah**: Sistem Operasi
**Semester**: Genap / Tahun Ajaran 2024–2025
**Nama**: `Haidar Habibi Al Farisi`
**NIM**: `240202862`
**Modul yang Dikerjakan**:
`(Contoh: Modul 1 – System Call dan Instrumentasi Kernel)`

---

## 📌 Deskripsi Singkat Tugas

Tuliskan deskripsi singkat dari modul yang Anda kerjakan. Misalnya:

* **Modul 1 – System Call dan Instrumentasi Kernel**:
Setelah proses parent melakukan fork(), kedua proses (parent dan child) berbagi halaman memori yang sama secara read-only.

Ketika salah satu proses mencoba menulis, terjadi page fault, dan halaman tersebut disalin secara terpisah (copy-on-write).

Mengimplementasikan system call shmget(int key) dan shmrelease(int key) untuk mendukung memori bersama (shared memory).

Dua proses (parent dan child) mengakses area memori yang sama menggunakan kunci yang sama.



## ✅ Uji Fungsionalitas

Tuliskan program uji apa saja yang Anda gunakan, misalnya:

* `ptest`: untuk menguji `getpinfo()`
* `rtest`: untuk menguji `getReadCount()`
* `cowtest`: untuk menguji fork dengan Copy-on-Write
* `shmtest`: untuk menguji `shmget()` dan `shmrelease()`
* `chmodtest`: untuk memastikan file `read-only` tidak bisa ditulis
* `audit`: untuk melihat isi log system call (jika dijalankan oleh PID 1)

---

## 📷 Hasil Uji

Lampirkan hasil uji berupa screenshot atau output terminal. Contoh:

![shmtest-haidarhabibia f-240202862](https://github.com/user-attachments/assets/179f4df0-9a03-415f-8789-89a3085cda75)

![cowtest-haidarhabibia f-240202862](https://github.com/user-attachments/assets/1826f118-b9ff-4869-aeed-ec5347bfd423)



## ⚠️ Kendala yang Dihadapi

Tuliskan kendala (jika ada), misalnya:

* Salah implementasi `page fault` menyebabkan panic
* Salah memetakan alamat shared memory ke USERTOP
* Proses biasa bisa akses audit log (belum ada validasi PID)

---

## 📚 Referensi

Tuliskan sumber referensi yang Anda gunakan, misalnya:

* Buku xv6 MIT: [https://pdos.csail.mit.edu/6.828/2018/xv6/book-rev11.pdf](https://pdos.csail.mit.edu/6.828/2018/xv6/book-rev11.pdf)
* Repositori xv6-public: [https://github.com/mit-pdos/xv6-public](https://github.com/mit-pdos/xv6-public)
* Stack Overflow, GitHub Issues, diskusi praktikum

---

