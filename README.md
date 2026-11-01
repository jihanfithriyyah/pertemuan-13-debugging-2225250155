# Pertemuan 13 - Debugging dan Testing

Nama: Jihan Fithriyyah[cite: 10]
NIM: 2225250155[cite: 10]
Kelas: 3A[cite: 10]

## Kasus
Program Python yang memproses data nilai mahasiswa (menghitung rata-rata, status kelulusan, dan nilai tertinggi) yang sebelumnya mengandung beberapa logical error[cite: 9].

## Test Case
| ID | Target | Input | Expected | Actual Awal | Status |
|---|---|---|---|---|---|
| T1 | rata-rata | [80, 60, 90, 70] | 75.0 | 60.0 | FAIL |
| T2 | rata-rata | [100, 80] | 90.0 | 36.0 | FAIL |
| T3 | status | 60 | Lulus | Tidak lulus | FAIL |
| T4 | status | 59 | Tidak lulus | Tidak lulus | PASS |
| T5 | tertinggi | [80, 60, 90, 70] | 90 | 0 | FAIL |

## Bug Report
1. **B01 (Rata-rata):** Pembagi menggunakan angka statis `5`, diperbaiki menggunakan `len(nilai)`.
2. **B02 (Status):** Menggunakan operator `>`, sehingga nilai 60 terbaca tidak lulus, diperbaiki menjadi `>=`.
3. **B03 (Nilai Tertinggi):** Inisialisasi awal bernilai `0` dan logika perbandingan salah, diperbaiki dengan elemen pertama list dan operator `>`.

## Retest
Seluruh test case (T1 sampai T5) telah dijalankan kembali setelah perbaikan kode dan menghasilkan status **PASS** tanpa adanya regresi[cite: 9, 14].

## Cara Menjalankan
python3 praktik/praktik_4_debugging.py[cite: 10]

## Refleksi
Teknik debugging yang paling membantu adalah penggunaan breakpoint dan pengujian berbasis test case (khususnya nilai batas), karena dapat langsung menunjukkan letak penyimpangan logika program secara akurat[cite: 10, 14].
