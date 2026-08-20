# Folioblox Portfolio Site

Dokumentasi untuk menjalankan website portfolio secara lokal.

## Prasyarat

- Python 3 sudah terpasang.
- Folder `portfolio-site` tetap berada di dalam folder `D:\DATA\PKL`.
- Folder asset background `ezgif-8258e3edc3750f03-jpg` berada sejajar dengan folder `portfolio-site`.
- Folder asset juga tersedia sebagai junction di dalam `portfolio-site`, sehingga background dapat dimuat saat server dijalankan dari folder situs. Junction ini sudah dibuat satu kali dan tidak perlu dibuat ulang setiap menjalankan website.

Struktur folder yang diperlukan:

```text
D:\DATA\PKL\
├── ezgif-8258e3edc3750f03-jpg\
└── portfolio-site\
    ├── index.html
    └── README.md
```

## Menjalankan Website

Buka PowerShell, lalu jalankan:

```powershell
cd "D:\DATA\PKL\portfolio-site"
python -m http.server 8000
```

Setelah muncul pesan bahwa server berjalan, buka browser dan akses:

```text
http://localhost:8000/
```

## Menghentikan Server

Kembali ke terminal yang menjalankan server, lalu tekan:

```text
Ctrl+C
```

## Catatan

- Website menggunakan `index.html` tanpa proses build atau instalasi dependency.
- Background menggunakan file gambar dari folder `ezgif-8258e3edc3750f03-jpg`.
- Jangan menghapus folder `portfolio-site\ezgif-8258e3edc3750f03-jpg`; folder tersebut adalah junction ke folder asset asli.
- Form kontak saat ini hanya berupa tampilan frontend dan belum mengirim data ke backend.
- Jika port `8000` sedang digunakan, jalankan dengan port lain, misalnya:

```powershell
python -m http.server 8080
```

Kemudian buka `http://localhost:8080/`.
