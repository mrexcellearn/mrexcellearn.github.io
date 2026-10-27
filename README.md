# mrexcellearn.github.io

Link hub untuk **excellearn.online** (GitHub Pages). Satu halaman: profil, produk unggulan, dan tombol ke Lynk.id.

## Ganti isi halaman

Semua teks dan link ada di [`links.json`](links.json). Buka file itu di github.com, klik ikon pensil, ubah, lalu **Commit changes**. Sekitar 1 menit kemudian situsnya sudah berubah.

| Bagian | Isi |
|---|---|
| `profil` | `nama`, `handle`, `bio` |
| `sosial` | Daftar ikon sosmed. `ikon` salah satu dari `tiktok`, `instagram`, `threads`, `linkedin` |
| `unggulan` | Kotak hijau, cukup satu produk. `label` (misal Gratis, Baru, Promo), `judul`, `deskripsi`, `harga`, `hargaCoret` (boleh `""`), `tombol`, `link`, `kampanye`. Isi `null` untuk menyembunyikan kotaknya |
| `tombol` | Tombol di bawah kotak unggulan. `judul`, `link`, `kampanye`, `ikon` (opsional: `toko` atau `kopi`) |

`kampanye` dipakai sebagai `utm_campaign`. Tulis huruf kecil pakai tanda hubung, misal `tes-interview`.

Kalau `links.json` salah ketik (misal kurang koma atau tanda kutip), halaman tetap tampil dengan isi cadangan di `index.html`. Cek dulu di [jsonlint.com](https://jsonlint.com) kalau ragu.

## Link untuk bio

| Bio di | Pasang link | Tercatat di Lynk.id sebagai |
|---|---|---|
| TikTok | `excellearn.online/tt` | `utm_source=tiktok` |
| Instagram | `excellearn.online/ig` | `utm_source=instagram` |
| Threads | `excellearn.online/th` | `utm_source=threads` |
| Dibuka langsung | `excellearn.online` | `utm_source=direct` |

Semua link ke `lynk.id` otomatis diberi `utm_source`, `utm_medium=linkhub`, `utm_campaign` (dari `kampanye`) dan `utm_content` (`unggulan` atau `tombol`).

## File

- `index.html`: tampilan dan isi cadangan. HTML, CSS dan sedikit JS, tanpa library.
- `links.json`: isi halaman.
- `tt/`, `ig/`, `th/`: alamat pendek untuk bio.
- `assets/`: avatar, favicon, gambar preview share (`og.png`), font Montserrat.
- `logo/`: logo lama, dibiarkan karena mungkin masih dipakai halaman lain.

`/landingpage`, `/webstore` dan `/template` adalah repo terpisah.
