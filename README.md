# D-1 — Portofolio Naufal Fikrianto

Website portofolio satu halaman untuk **Naufal Fikrianto** — mahasiswa **Teknik Lingkungan,
Universitas Singaperbangsa Karawang (UNSIKA)**, semester 7, sekaligus pemain futsal.

Dibuat murni dengan HTML + CSS: tanpa JavaScript, tanpa build tool, tanpa CDN.

**Live:** https://kazeminato335.github.io/D-1/

## Isi repo

| File | Keterangan |
|---|---|
| `index.html` | Struktur & konten halaman |
| `style.css` | Tampilan, tema, dan aturan responsif |
| `assets/*.jpg` | Gambar proyek (DED, skema unit, ilustrasi unit) |
| `README.md` | Dokumentasi ini |

## Bagian halaman

1. **Hero** — perkenalan, kartu identitas, ringkasan keahlian
2. **Tentang** — latar belakang Teknik Lingkungan + futsal
3. **Kompetensi** — 4 kartu dengan progress bar
4. **Proyek** — timeline: capstone TPA Jalupang, AMDAL TPS 3R, Etika Profesi, futsal
5. **Galeri** — gambar DED & skema unit pengolahan lindi
6. **Kontak** — email, lokasi, kampus, Instagram, GitHub

## Data yang sudah terisi

- Nama, kampus (UNSIKA), semester 7
- Email: `riantonaufal8@gmail.com`
- Lokasi: Bekasi, Jawa Barat
- Instagram: [@nfiknt](https://instagram.com/nfiknt)
- GitHub: [kazeminato335](https://github.com/kazeminato335)
- Tiga proyek akademik semester 7

## Yang masih perlu dilengkapi

| Bagian | Lokasi | Catatan |
|---|---|---|
| Prestasi futsal | `.timeline-item` terakhir (tahun 2025) | Masih teks placeholder |
| Nomor punggung & posisi | `.jersey-number`, `.jersey-role` | Sekarang `7` dan "Futsal" |
| Foto futsal | galeri, blok `.ph ph-1` | Ganti dengan `<img src="assets/...">` |
| Persentase kompetensi | `style="--w: 80%"` + `.stat-value` | Sesuaikan penilaian sendiri |

## Catatan tentang gambar proyek

Gambar di `assets/` berasal dari dokumen capstone **Kelompok K04** (redesain drainase &
IPAL lindi TPA Jalupang). Sudah dicantumkan atribusi kelompok pada caption. Jika rekan tim
tidak ingin karyanya dipublikasikan, hapus file `assets/*.jpg` dan ganti blok galeri
dengan foto pribadi.

## Menjalankan lokal

```bash
start index.html        # Windows
```

Cek tampilan ponsel: `F12` → ikon perangkat (Ctrl+Shift+M).

## Kustomisasi

Warna aksen diatur lewat variabel di `style.css`:

```css
:root {
  --bg: #080b0f;
  --accent: #c8f542;   /* lime */
  --accent-2: #ff6a3d;
}
```

## Publikasi

GitHub Pages sudah aktif dan menyajikan branch `main` folder root. Setiap `git push`
ke `main` otomatis memperbarui situs dalam 1–2 menit.

## Catatan teknis

- Menu mobile memakai trik `:checkbox` CSS — tetap bisa diakses lewat keyboard.
- Responsif di 980px, 760px, 420px; tipografi memakai `clamp()`.
- Aksesibilitas: skip link, `aria-label`, focus ring, `prefers-reduced-motion`.
- Form kontak memakai `mailto:`; ganti ke Formspree/Netlify Forms bila ingin form langsung.
