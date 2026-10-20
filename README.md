# BEYOND BOOKS — Sistem Informasi Penjualan Buku

Aplikasi demonstrasi frontend-only menggunakan HTML5, CSS3, JavaScript ES Modules, IndexedDB, dan localStorage.

## Menjalankan
1. Ekstrak folder `beyond-books`.
2. Buka folder melalui Visual Studio Code.
3. Jalankan `index.html` menggunakan ekstensi Live Server. Jangan membuka file langsung melalui `file://` karena modul JavaScript dan IndexedDB membutuhkan origin browser.
4. Data demo dibuat otomatis pada kunjungan pertama.

## Akun demo
Semua akun menggunakan password demo `demo123`:
- `admin@beyondbooks.demo` — Super Admin
- `toko@beyondbooks.demo` — Admin Toko
- `kasir@beyondbooks.demo` — Kasir
- `gudang@beyondbooks.demo` — Petugas Gudang
- `manager@beyondbooks.demo` — Manager
- `customer@beyondbooks.demo` — Pelanggan

## Fitur yang tersedia
- Landing page, katalog 50 buku simulasi, pencarian, filter kategori, sorting, detail buku.
- Keranjang lokal, checkout demo, penyimpanan pesanan dan pengurangan stok.
- Login demo berbasis role UI; registrasi pelanggan.
- Dashboard statistik dari data IndexedDB.
- CRUD buku dengan validasi SKU, pencarian, edit, nonaktifkan/aktifkan dan ekspor CSV.
- POS/kasir, validasi uang tunai, pengurangan stok, mutasi inventaris.
- Daftar pesanan dan perubahan status, laporan berdasarkan tanggal, grafik Canvas, ekspor CSV, print.
- Pengaturan toko demo.

## Batasan penting
Ini adalah proyek frontend-only untuk demonstrasi akademik. Password disimpan sebagai data demo lokal, role hanya membatasi antarmuka, tidak ada otorisasi server, pembayaran sungguhan, sinkronisasi lintas perangkat, atau database server. Jangan gunakan data pribadi atau password nyata. IndexedDB terikat browser dan origin yang sama. Gunakan browser print untuk PDF.

## Struktur
- `index.html` — halaman utama
- `assets/pages/` — halaman katalog, detail buku, keranjang, checkout, login, dan registrasi
- `assets/pages/admin/` — dashboard, buku, kasir, pesanan, inventaris, laporan, pengguna, dan pengaturan
- `assets/css/main.css`
- `assets/js/` — database, seed, katalog, keranjang, checkout, autentikasi, dashboard

## Prosedur uji manual
1. Buka Home dan pastikan buku rekomendasi muncul.
2. Buka katalog, cari kata “web”, ubah kategori dan urutan harga.
3. Tambahkan buku ke keranjang, ubah jumlah, hapus item, lanjut checkout.
4. Isi data demo dengan kode pos lima digit dan buat pesanan; pastikan nomor pesanan tampil dan stok berkurang.
5. Login sebagai `admin@beyondbooks.demo` / `demo123`, buka Manajemen Buku, tambah/edit/nonaktifkan buku.
6. Login sebagai `kasir@beyondbooks.demo`, buat transaksi dengan uang tunai cukup, lalu verifikasi stok berubah.
7. Buka Inventaris, catat stok masuk dan pastikan mutasi terlihat.
8. Buka Laporan, pilih tanggal, ekspor CSV dan gunakan Cetak/PDF.
9. Refresh halaman lalu periksa persistensi data.

## Catatan ruang lingkup
Prompt spesifikasi yang luas dapat dikembangkan lebih lanjut: modul penulis/penerbit/supplier/pelanggan terpisah, retur dan pengadaan lengkap, backup/restore JSON, ERD serta diagram UML. Implementasi ini menyediakan kerangka yang dapat dijalankan dan alur utama katalog, checkout, CRUD buku, POS, inventaris, pesanan, laporan, dan pengaturan; modul yang belum lengkap tidak diklaim selesai.
