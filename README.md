# 🎨 Aruna Studio — Web Portofolio Seni

> Web portofolio seni berbasis **Bootstrap 5** murni — satu file HTML, langsung buka di browser, tanpa instalasi apapun.

---

## 📋 Daftar Isi

- [Demo & Screenshot](#-demo--screenshot)
- [Fitur](#-fitur)
- [Komponen Bootstrap 5](#-komponen-bootstrap-5-yang-digunakan)
- [Struktur File](#-struktur-file)
- [Cara Menggunakan](#-cara-menggunakan)
- [Kustomisasi](#-kustomisasi)
- [Dependensi](#-dependensi)
- [Lisensi](#-lisensi)

---

## 🖥️ Demo & Screenshot

Buka file `portfolio-seni.html` langsung di browser untuk melihat tampilan lengkap.

**Sections yang tersedia:**
```
🏠 Navbar         → Sticky navigasi dengan link aktif
🦸 Hero           → Jumbotron fullscreen dengan statistik
📢 Alert          → Pengumuman pameran terbaru
🖼️ Galeri         → Grid 6 karya seni (Cards)
📊 Katalog        → Tabel inventaris lengkap
🏆 Penghargaan    → List group rekam jejak
👤 Tentang        → Profil seniman
📬 Kontak         → Form pengiriman pesan
🔻 Footer         → Multi-kolom + newsletter
```

---

## ✨ Fitur

- ✅ **Single file** — satu file `.html`, langsung jalan
- ✅ **Responsive** — mobile, tablet, dan desktop
- ✅ **No build tools** — tidak perlu Node.js, npm, atau webpack
- ✅ **Koneksi internet** — CDN Bootstrap 5 & Google Fonts (butuh internet)
- ✅ **Smooth scroll** — navigasi antar section mulus
- ✅ **Filter galeri** — toggle kategori karya (UI)
- ✅ **Modal interaktif** — detail karya & form kontak
- ✅ **Custom CSS Variables** — warna mudah diganti dari satu tempat

---

## 🧩 Komponen Bootstrap 5 yang Digunakan

| # | Komponen | Lokasi di Halaman |
|---|---|---|
| 1 | **Navbar** | Atas — sticky, collapsible di mobile |
| 2 | **Hero / Jumbotron** | Section pertama — fullscreen |
| 3 | **Cards** | Section Galeri — 6 karya seni |
| 4 | **Form** | Section Kontak & dalam Modal |
| 5 | **Table** | Section Katalog — inventaris karya |
| 6 | **Modal** | Detail karya + modal kontak navbar |
| 7 | **Badge** | Status karya, media, kategori |
| 8 | **Button** | Seluruh halaman — berbagai variant |
| 9 | **Alert** | Banner pengumuman pameran |
| 10 | **Footer** | Bawah halaman — multi-kolom |
| 11 | **List Group** | Section Penghargaan |
| 12 | **Utilities** | `d-flex`, `gap-*`, `text-*`, `bg-*`, `py-*`, `ms-auto`, `shadow-sm`, dll |

---

## 📁 Struktur File

```
portofolio-seni/
│
├── portfolio-seni.html   ← File utama (semua dalam 1 file)
└── README.md             ← Dokumentasi ini
```

> Semua CSS dan JavaScript sudah ditulis **inline** dalam satu file HTML.
> Gambar menggunakan URL dari **Unsplash** (butuh koneksi internet).

---

## 🚀 Cara Menggunakan

### 1. Buka Langsung di Browser

```bash
# Klik dua kali file-nya, atau:
start portfolio-seni.html       # Windows
open portfolio-seni.html        # macOS
xdg-open portfolio-seni.html    # Linux
```

### 2. Jalankan via Live Server (Opsional)

Jika menggunakan VS Code, install ekstensi **Live Server** lalu klik kanan → *Open with Live Server*.

### 3. Upload ke Hosting

Cukup upload `portfolio-seni.html` ke:
- **GitHub Pages** — gratis, dari repository GitHub
- **Netlify / Vercel** — drag & drop langsung
- **cPanel / FTP** — upload ke folder `public_html`

---

## 🎨 Kustomisasi

### Ganti Warna Tema

Semua warna diatur lewat **CSS Variables** di bagian `:root`:

```css
:root {
  --cream: #f5f0e8;   /* Warna latar belakang utama */
  --ink:   #1a1209;   /* Warna teks gelap / navbar */
  --rust:  #c0440e;   /* Warna aksen utama (tombol, border) */
  --gold:  #c9922a;   /* Warna aksen emas */
  --sage:  #5a7a5e;   /* Warna hijau sage (cadangan) */
  --paper: #ede8dc;   /* Warna latar section terang */
}
```

### Ganti Identitas Seniman

Cari dan ganti teks berikut di dalam file HTML:

| Teks Lama | Ganti Dengan |
|---|---|
| `Aruna Studio` | Nama studio/brand Anda |
| `Aruna Dewanti` | Nama lengkap Anda |
| `aruna@arunastudio.id` | Email Anda |
| `+62 812-3456-7890` | Nomor telepon Anda |
| `Surabaya, Jawa Timur` | Kota Anda |

### Ganti Foto Karya Seni

Cari tag `<img src="https://images.unsplash.com/...">` dan ganti URL-nya dengan:

```html
<!-- Menggunakan gambar lokal -->
<img src="foto/karya-saya.jpg" alt="Judul Karya"/>

<!-- Atau URL gambar online -->
<img src="https://link-gambar-anda.com/foto.jpg" alt="Judul Karya"/>
```

### Tambah Karya Baru di Galeri

Duplikasi blok card berikut dan sesuaikan isinya:

```html
<div class="col-sm-6 col-lg-4">
  <div class="art-card card h-100">
    <div class="card-img-wrap">
      <img src="URL_GAMBAR" alt="Judul Karya"/>
      <span class="card-year">2024</span>
    </div>
    <div class="card-body d-flex flex-column p-4">
      <div class="card-category mb-1">Kategori Media</div>
      <h5 class="card-title-art mb-2">Judul Karya</h5>
      <p class="card-text text-muted small mb-3 flex-grow-1">
        Deskripsi singkat karya...
      </p>
      <div class="d-flex align-items-center justify-content-between">
        <span class="badge rounded-0 bg-success me-1">Tersedia</span>
        <a href="link-file.jpg" download class="btn btn-dl">
          <i class="bi bi-download me-1"></i>Unduh
        </a>
      </div>
    </div>
  </div>
</div>
```

### Badge Status Karya

```html
<span class="badge rounded-0 bg-success">Tersedia</span>
<span class="badge rounded-0 bg-warning text-dark">Terjual</span>
<span class="badge rounded-0 bg-danger">Gratis</span>
<span class="badge rounded-0 bg-secondary">Edisi Terbatas</span>
```

### Aktifkan Link Download

Ganti `href="#"` dengan path file yang ingin diunduh:

```html
<a href="files/karya-saya.jpg" download class="btn btn-dl">
  <i class="bi bi-download me-1"></i>Unduh
</a>
```

---

## 📦 Dependensi

Semua dimuat via **CDN** (butuh koneksi internet):

| Library | Versi | Kegunaan |
|---|---|---|
| [Bootstrap](https://getbootstrap.com) | 5.3.3 | Framework CSS & JS |
| [Bootstrap Icons](https://icons.getbootstrap.com) | 1.11.3 | Ikon SVG |
| [Google Fonts — Playfair Display](https://fonts.google.com/specimen/Playfair+Display) | Latest | Font display/heading |
| [Google Fonts — DM Sans](https://fonts.google.com/specimen/DM+Sans) | Latest | Font body |

### Offline / Tanpa Internet

Download Bootstrap dan font secara lokal:

```html
<!-- Ganti CDN dengan file lokal -->
<link href="bootstrap/bootstrap.min.css" rel="stylesheet"/>
<script src="bootstrap/bootstrap.bundle.min.js"></script>
```

Download Bootstrap: [getbootstrap.com/docs/5.3/getting-started/download](https://getbootstrap.com/docs/5.3/getting-started/download/)

---

## 🛠️ Teknologi

- **HTML5** — Struktur semantik
- **CSS3** — Custom properties, flexbox, grid, transitions
- **JavaScript (Vanilla)** — Filter toggle, smooth scroll
- **Bootstrap 5.3** — Layout, komponen, utilities

---

## 📱 Responsivitas

| Breakpoint | Lebar | Tampilan Galeri |
|---|---|---|
| `xs` | < 576px | 1 kolom |
| `sm` | ≥ 576px | 2 kolom |
| `lg` | ≥ 992px | 3 kolom |

Navbar otomatis collapse menjadi hamburger menu di layar kecil.

---

## 📄 Lisensi

Proyek ini dibuat untuk keperluan **edukasi dan portofolio pribadi**.

- Kode: bebas digunakan dan dimodifikasi
- Foto: dari [Unsplash](https://unsplash.com) — silakan ganti dengan karya sendiri untuk penggunaan komersial
- Bootstrap: lisensi [MIT](https://github.com/twbs/bootstrap/blob/main/LICENSE)

---

## 🙋 Dibuat Dengan

```
Bootstrap 5  ·  HTML murni  ·  Tanpa framework JS
Dibuat oleh: Claude (Anthropic)
Untuk: Aruna Studio — Portofolio Seni
```

---

> 💡 **Tips:** Gunakan **Ctrl+F** di browser atau code editor untuk mencari dan mengganti teks dengan cepat.
