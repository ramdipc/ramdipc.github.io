# Website Portofolio Ramdi Kurniawan

Website statis untuk GitHub Pages, dengan dashboard di `/admin` untuk mengedit isi tanpa menyentuh kode.

```
index.html          ← halaman publik
admin/index.html    ← dashboard (login dengan token GitHub)
data/content.json   ← SEMUA isi website (diedit lewat dashboard)
assets/             ← foto & ikon
.nojekyll           ← wajib ada, jangan dihapus
```

## A. Membuat website online (sekali saja, ±10 menit)

1. **Buat repository**
   - Masuk ke github.com → klik **+** (kanan atas) → **New repository**.
   - Repository name: `rmdkit2026.github.io` (huruf kecil semua, persis username + `.github.io`).
   - Pilih **Public** → klik **Create repository**.

2. **Upload file**
   - Di halaman repository yang baru, klik link **uploading an existing file**.
   - Ekstrak file ZIP di komputer, buka foldernya, **pilih semua isi folder** (index.html, admin, data, assets, .nojekyll, README.md) lalu seret ke halaman GitHub.
   - Catatan: file `.nojekyll` tersembunyi di beberapa komputer. Di Windows: File Explorer → View → centang *Hidden items*. Di Mac: tekan `Cmd + Shift + .`
   - Klik **Commit changes**.

3. **Aktifkan GitHub Pages**
   - Buka tab **Settings** → menu kiri **Pages**.
   - Source: **Deploy from a branch** → Branch: **main**, folder **/ (root)** → **Save**.
   - Tunggu 1–2 menit, lalu buka **https://rmdkit2026.github.io**

## B. Membuat token untuk dashboard (sekali saja)

1. GitHub → foto profil (kanan atas) → **Settings** → paling bawah **Developer settings**.
2. **Personal access tokens** → **Fine-grained tokens** → **Generate new token**.
3. Isi:
   - Token name: `Dashboard portofolio`
   - Expiration: 90 hari atau 1 tahun (nanti tinggal buat baru)
   - Repository access: **Only select repositories** → pilih `rmdkit2026.github.io`
   - Permissions → Repository permissions → **Contents: Read and write**
4. **Generate token** → salin token (`github_pat_…`). Token hanya tampil sekali.

⚠️ Token ini seperti kunci rumah: jangan kirim ke siapa pun dan jangan ditulis di file repository.

## C. Mengedit website lewat dashboard

1. Buka **https://rmdkit2026.github.io/admin/**
2. Isi username `RMDKIT2026`, repository `rmdkit2026.github.io`, branch `main`, tempel token → **Masuk**.
3. Edit isi di tab Profil, Pengalaman, Proyek, Keahlian, Kontak. Klik **Pratinjau** untuk melihat hasilnya langsung.
4. Klik **Terbitkan**. Perubahan tampil di website dalam ±1 menit (muat ulang halaman).

Tips:
- Perubahan yang belum diterbitkan tersimpan otomatis sebagai draf di browser.
- **Pengaturan → Unduh cadangan** untuk menyimpan salinan isi website.
- Foto terbaik: PNG latar transparan, orientasi potret.
- Di perangkat umum/bersama, hilangkan centang "Ingat saya", atau klik **Keluar** setelah selesai.

## D. (Opsional) Domain sendiri

Beli domain (mis. `ramdikurniawan.my.id`), lalu di **Settings → Pages → Custom domain** isi domainnya dan ikuti petunjuk DNS dari GitHub. Centang **Enforce HTTPS** setelah aktif.
