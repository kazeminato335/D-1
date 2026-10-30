# D-1 — Portofolio Naufal Fikrianto

Website portofolio satu halaman untuk **Naufal Fikrianto**, mahasiswa Teknik Lingkungan
sekaligus pemain futsal. Dibuat murni dengan HTML + CSS (tanpa JavaScript, tanpa build tool,
tanpa CDN) sehingga bisa dibuka langsung dari file lokal.

## Isi repo

| File | Keterangan |
|---|---|
| `index.html` | Seluruh struktur & konten halaman |
| `style.css` | Tampilan, tema, dan aturan responsif |
| `README.md` | Dokumentasi ini |

## Bagian halaman

1. **Hero** — perkenalan, nomor punggung, strip statistik
2. **Tentang** — narasi singkat + daftar keahlian
3. **Statistik** — 4 kartu dengan progress bar beranimasi
4. **Prestasi** — timeline 2022–2025
5. **Galeri** — grid foto asimetris
6. **Kontak** — email, telepon, sosial, form pesan

## Menjalankan secara lokal

Klik dua kali `index.html`, atau:

```bash
# dari folder repo
start index.html        # Windows
```

Cek tampilan ponsel: `F12` → ikon perangkat (Ctrl+Shift+M).

## Yang perlu diganti sebelum dipublikasikan

> Semua angka dan prestasi di halaman masih **placeholder**. Bagian yang harus diganti
> sudah ditandai komentar `<!-- GANTI ... -->` di `index.html`.

- Nama brand (`NF`, `Naufal`) dan judul halaman
- Angka di `.hero-stats`: gol, assist, IPK
- Nomor punggung (`.jersey-number`, `.jersey-club`) dan posisi (`.jersey-role`)
- Nilai & persentase di `.stat-card` (`style="--w: 64%"`)
- 4 item `.timeline-item` (tahun, event, hasil)
- Foto galeri: ganti `<div class="ph ...">` dengan `<img src="..." alt="...">`
- Email `naufal.fikrianto@example.com`, nomor telepon, dan link sosial (`href="#"`)

## Kustomisasi

Ganti warna aksen lewat variabel di `style.css`:

```css
:root {
  --bg: #080b0f;
  --accent: #c8f542;   /* lime */
  --accent-2: #ff6a3d;
}
```

Pilihan aksen lain: `#00d4ff` (cyan), `#ff4d2d` (oranye), `#22c55e` (hijau lapangan).

## Publikasi (GitHub Pages)

1. Buka **Settings → Pages**.
2. *Source*: **Deploy from a branch**.
3. Branch `main`, folder `/ (root)` → **Save**.
4. Tunggu 1–2 menit, situs aktif di:
   `https://kazeminato335.github.io/D-1/`

## Catatan teknis

- Menu mobile memakai trik `:checkbox` CSS — tetap dapat diakses lewat keyboard.
- Responsif di 980px, 760px, dan 420px; tipografi memakai `clamp()`.
- Aksesibilitas: skip link, `aria-label`, focus ring, `prefers-reduced-motion`.
- Form kontak masih statis (`action="#"`); sambungkan ke Formspree/Netlify Forms bila perlu.
