# Kasir Kosmetik Alessandra

Aplikasi kasir (point of sale) sederhana untuk toko kosmetik. Satu file HTML, tanpa server, tanpa instalasi.

## Fitur

- Kasir: cari produk (nama atau SKU), filter kategori, keranjang, diskon (Rp atau %), pembayaran Tunai, QRIS, atau Debit, hitung kembalian otomatis
- Struk pembayaran dengan nama toko, alamat, dan nomor telepon
- Manajemen produk: tambah, ubah harga dan stok, hapus
- Barcode otomatis (Code 39 dari SKU) untuk setiap produk
- Cek harga untuk pembeli: scan barcode (alat scan USB atau kamera) atau ketik SKU
- Riwayat transaksi, omzet harian, dan peringatan stok menipis
- Login admin untuk halaman Produk dan Riwayat
- Mode terang dan gelap otomatis

## Cara memakai

Buka `index.html` di browser, atau pasang di GitHub Pages (lihat di bawah).

Saat pertama kali membuka halaman Produk atau Riwayat, aplikasi meminta Anda membuat kata sandi admin. Kata sandi ini tersimpan (dalam bentuk hash) di browser perangkat yang dipakai.

## Memasang di GitHub Pages

1. Buat repositori baru di GitHub, lalu unggah `index.html` dan `README.md`.
2. Buka **Settings** > **Pages**.
3. Di bagian **Build and deployment**, pilih **Deploy from a branch**, pilih branch `main` dan folder `/ (root)`, lalu simpan.
4. Tunggu beberapa menit. Aplikasi bisa dibuka di `https://NAMA-GITHUB-ANDA.github.io/NAMA-REPOSITORI/`.

Scan kamera butuh alamat https, jadi di GitHub Pages fitur ini bisa dipakai (di browser yang mendukung `BarcodeDetector`).

## Mengubah info toko

Nama toko, alamat, dan nomor telepon di struk bisa diubah di aplikasi: login admin, buka tab **Produk**, lalu edit kartu **Info toko di struk**. Nilai awalnya ada di `index.html`, cari tulisan `Prambon Watutulis`.

## Catatan penting

- Semua data (produk, transaksi, sandi admin) tersimpan di browser masing-masing perangkat (`localStorage`). Data tidak sinkron antar perangkat dan hilang kalau data browser dihapus.
- Login admin hanya pengaman di sisi browser, bukan pengganti sistem keamanan server. Jangan dipakai untuk melindungi data yang sangat sensitif.
- Karena repositori ini publik, semua isi `index.html` bisa dilihat siapa saja, termasuk alamat dan nomor telepon toko.

## Teknologi

HTML, CSS, dan JavaScript murni. Font Plus Jakarta Sans dari Google Fonts.
