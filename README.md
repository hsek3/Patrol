# HSE COMMAND CENTER — halaman pintu masuk (GitHub Pages)

Halaman statis berisi tombol **Buka Aplikasi** menuju Web App Google Apps Script, lengkap dengan ikon perisai HSE
(favicon, ikon layar utama HP, dan manifest agar bisa dipasang seperti aplikasi).

## Isi
| File | Fungsi |
|---|---|
| `index.html` | Halaman pintu masuk (URL Web App ada di variabel `APP_URL` dalam script di bagian bawah) |
| `favicon.svg`, `favicon-32.png` | Ikon tab browser |
| `apple-touch-icon.png` | Ikon layar utama iPhone |
| `icon-192.png`, `icon-512.png` | Ikon Android / PWA |
| `manifest.webmanifest` | Nama, warna, dan ikon aplikasi |
| `.nojekyll` | Menonaktifkan Jekyll agar semua file disajikan apa adanya |

## Cara hosting di GitHub Pages
1. Buat repository baru di GitHub (mis. `hse-command-center`), visibilitas **Public** (GitHub Pages gratis memerlukan repo publik).
2. Klik **Add file → Upload files**, unggah **semua isi folder ini** (termasuk `.nojekyll`), lalu **Commit changes**.
3. Buka **Settings → Pages**. Pada *Build and deployment* pilih **Source: Deploy from a branch**, **Branch: main**, folder **/ (root)**, lalu **Save**.
4. Tunggu 1–2 menit. Alamat situs: `https://<username-github>.github.io/hse-command-center/`
5. Buka alamat itu di HP, lalu pasang ke layar utama (Android: menu ⋮ → *Tambahkan ke layar utama*; iPhone: Bagikan → *Tambah ke Layar Utama*).

## Jika URL Web App berubah
URL `/exec` tetap sama selama Anda men-deploy lewat **Manage deployments → Edit → New version**.
Jika Anda membuat *New deployment*, URL berubah: ganti nilai `APP_URL` di `index.html`, lalu commit.

## Catatan
- Halaman ini hanya pintu masuk. Data dan login tetap di Google Apps Script; tidak ada password atau data di GitHub.
- Jangan memasukkan file `KREDENSIAL_AWAL.txt` atau isi Apps Script ke repository publik.
- Centang *Langsung buka aplikasi* agar halaman langsung meneruskan ke aplikasi. Untuk menahan halaman ini, tambahkan `?stay=1` di URL.
