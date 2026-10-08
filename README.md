# Folioblox Portfolio Site

Dokumentasi untuk menjalankan website portfolio secara lokal.

## Prasyarat

- Python 3 sudah terpasang (jika dijalankan via http.server), atau menggunakan Laragon / Apache.
- Folder asset background `ezgif-8258e3edc3750f03-jpg` berada sejajar dengan folder `portfolio-site`.
- Folder asset juga tersedia sebagai junction di dalam `portfolio-site`, sehingga background dapat dimuat saat server dijalankan dari folder situs.

Struktur folder:

```text
Portofolio/
├── ezgif-8258e3edc3750f03-jpg/
├── index.html (redirector)
└── portfolio-site/
    ├── index.html
    ├── cv.html
    ├── me.png
    ├── backsound.mp3
    └── README.md
```

## Menjalankan Website

### Opsi 1: Menggunakan Laragon (Rekomendasi)
Jika menggunakan Laragon, cukup buka browser dan akses melalui Virtual Host atau:
```text
http://localhost/PROJEK%20SH/MY%20PROJEK%20-%20ALL/Portofolio/
```
atau langsung ke folder situs:
```text
http://localhost/PROJEK%20SH/MY%20PROJEK%20-%20ALL/Portofolio/portfolio-site/
```

### Opsi 2: Menggunakan Python HTTP Server
Buka terminal / PowerShell di folder `portfolio-site`:

```powershell
python -m http.server 8000
```

Buka browser di:
```text
http://localhost:8000/
```

## Fitur Responsif Mobile

Website sudah dioptimalkan penuh untuk tampilan mobile (smartphone & tablet):
- **Hamburger Menu Navigasi**: Menu drawer geser interaktif untuk mobile, lengkap dengan tautan ke seluruh bagian dan link CV.
- **Tipografi Adaptif**: Ukuran font judul, nama autor, dan subjudul menyesuaikan ukuran layar secara proporsional menggunakan CSS `clamp()`.
- **Formulir Ramah Mobile**: Input font size 16px (mencegah auto-zoom di iOS Safari), padding sentuh nyaman, dan tombol aksi lebar penuh di layar kecil.
- **Optimasi Baterai & Canvas**: Loop render sequence background hanya aktif saat terjadi scroll / animasi aktif, menghemat daya baterai perangkat seluler.
- **Halaman CV Responsif**: Tampilan foto, data diri, tombol download, dan riwayat terpusat rapi di layar HP.
