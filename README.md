# Portofolio Nesya Cahaya Artianti

Situs statis satu halaman (`index.html`). Tanpa framework, tanpa build, tanpa npm. Buka `index.html` di browser untuk melihat hasilnya.

## Isi paket

- `index.html`: seluruh halaman (CSS dan JavaScript sudah inline)
- `vercel.json`: header keamanan dan `cleanUrls`, tanpa `buildCommand`
- `README.md`: panduan ini

## Cara mengedit konten

Cari komentar `<!-- EDIT: ... -->` di `index.html`. Komentar itu menandai data yang perlu diganti:

- URL situs di `og:url` dan `canonical` (setelah deploy)
- Nomor WhatsApp di tautan `wa.me/...` (format `62...`, tanpa `+` atau spasi)
- Username Instagram di tautan `instagram.com/...`
- Bulan dan tahun PKL (saat ini `Jan – Jun 2026`)
- Tahun pendidikan (saat ini `2024 – 2027`)
- Bahasa Inggris, jika ada, di bagian Keahlian
- Template pengalaman organisasi dan kartu sertifikat ada di dalam komentar. Aktifkan hanya jika datanya sudah ada.

Angka di pita statistik (keahlian dan hasil kerja) dihitung otomatis dari jumlah kartu di halaman. Tidak perlu diubah manual.

## Cara push ke GitHub

```bash
git init
git add .
git commit -m "Portofolio Nesya Cahaya Artianti"
git branch -M main
git remote add origin https://github.com/USERNAME/NAMA-REPO.git
git push -u origin main
```

## Cara deploy ke Vercel

1. Buka vercel.com lalu pilih **Add New → Project**.
2. Import repository GitHub tadi.
3. Pada **Framework Preset**, pilih **Other**.
4. Kosongkan **Build Command**.
5. Kosongkan **Output Directory**, atau isi `.` bila diminta.
6. Klik **Deploy**.

Setelah situs aktif, ganti URL di `og:url` dan `canonical` dengan alamat Vercel yang sebenarnya, lalu push lagi.

## Fitur

- Mode terang dan gelap: otomatis mengikuti perangkat, bisa diganti manual lewat tombol di navigasi (disimpan di localStorage).
- Pengalaman bisa dibuka dan ditutup.
- Filter keahlian menyorot poin dan kartu yang cocok. Yang tidak cocok diredupkan, tidak dihapus.
- Tombol **Salin email** dan **Unduh CV** (memanggil cetak browser).
- Cetak (Ctrl+P) menghasilkan versi CV satu kolom, A4, tanpa navigasi dan tombol.
- Konten tetap terbaca saat JavaScript dimatikan.

## Checklist sebelum dikirim ke HRD

- [ ] Nomor WhatsApp dan username Instagram sudah diganti dari contoh
- [ ] Tidak ada tautan yang mati. Hapus tautan yang tidak dipakai
- [ ] Periode PKL dan tahun pendidikan sudah sesuai data asli
- [ ] Semua tulisan di halaman sudah sesuai data asli dan tidak ada yang dikarang
- [ ] URL di `og:url` dan `canonical` sudah sesuai alamat Vercel
- [ ] Situs dibuka di HP (lebar 360px): tidak ada scroll horizontal
- [ ] Mode terang dan gelap sama-sama terbaca
- [ ] Ctrl+P menghasilkan CV yang rapi di A4
- [ ] Konsol browser tidak menampilkan error
