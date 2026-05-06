# 📊 AM Dashboard: Price Competitiveness

Aplikasi *Single Page Application* (SPA) berbasis web statis yang dirancang khusus untuk tim **Account Manager (Accommodation)** di tiket.com. 

Alat ini berfungsi untuk mengotomatisasi analisis data *scrapping* kompetisi harga (Native vs Google Hotel vs PE Log) dari file *raw* CSV/Excel, dan secara otomatis merangkai *draft* komunikasi (Email & WhatsApp) untuk partner hotel yang terdampak.

## ✨ Fitur Utama

- **100% Client-Side Processing:** Membaca dan memproses data file langsung di *browser* pengguna. Sangat aman dan cepat karena tidak ada data sensitif yang diunggah ke server (*backend-less*).
- **Smart Column Detection:** Menggunakan algoritma *Anchor* berbasis kolom `"Competitive Flagging"` sehingga sistem kebal terhadap anomali format file (seperti nama kolom yang tersembunyi/kosong dari sistem extranet).
- **Auto-Generate Drafts:** Mengubah baris-baris data mentah menjadi *draft* Email (dengan format tabel teks yang rapi) dan *draft* WhatsApp.
- **Copy-to-Clipboard:** Tombol praktis untuk langsung menyalin teks dan mem- *paste* nya ke Gmail, Outlook, atau WhatsApp Web.
- **Multi-Format Support:** Mendukung file `.csv`, `.tsv` (UTF-16), `.xls`, dan `.xlsx`.

## 🛠️ Tech Stack

Proyek ini dibangun seringan mungkin agar mudah di-*embed* ke dalam platform seperti Google Sites:
- **HTML5 & CSS3**
- **Tailwind CSS** (via CDN) untuk *styling* dan *layout*.
- **Vanilla JavaScript** (ES6+) untuk logika analisis.
- **PapaParse** (via CDN) untuk *parsing* file CSV/TSV.
- **SheetJS / xlsx** (via CDN) untuk membaca file Excel.

## 🚀 Cara Penggunaan (Panduan AM)

1. Buka URL Dashboard (bisa diakses melalui *embed* di Google Sites internal).
2. Klik **Choose File** dan unggah file hasil *download* dari sistem internal tiket.com.
3. Tunggu hingga status file berubah menjadi indikator hijau (Ready).
4. Klik tombol **Analyze Data**.
5. Tabel akan memunculkan daftar properti mana saja yang harganya kalah saing beserta ringkasan di platform mana mereka kalah.
6. Klik tombol **Buat Draft** di kolom Action pada properti yang diinginkan.
7. Di bagian bawah, klik **Copy Email** atau **Copy WA** untuk menyalin teks yang sudah terisi otomatis dengan nama hotel, platform kompetitor, dan detail tanggalnya.

## 🌐 Deployment (GitHub Pages ke Google Sites)

Repositori ini dikonfigurasi untuk berjalan di **GitHub Pages**.

1. Pastikan kode di-*push* ke *branch* `main`.
2. Aktifkan GitHub Pages di menu **Settings -> Pages** (Source: Deploy from a branch, Branch: `main`).
3. Dapatkan URL GitHub Pages yang *live* (misal: `https://[username].github.io/tiket-dashboard/`).
4. Buka Google Sites, pilih fitur **Embed -> By URL**.
5. Masukkan URL GitHub Pages tersebut. 
6. Setiap pembaruan (*commit*) yang dilakukan di GitHub akan otomatis memperbarui tampilan di Google Sites tanpa perlu mengubah tautan *embed*.

---
*Developed for tiket.com Accommodation Team to streamline daily workflows.*
