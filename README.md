# Affilio — Pantau Komisi Harian

Aplikasi PWA (Progressive Web App) untuk memantau posting & komisi harian
akun Shopee Video dan TikTok. Data tersimpan lokal di perangkat (localStorage),
jalan offline, dan bisa dipasang sebagai aplikasi Android.

## 1. Deploy ke GitHub Pages (gratis, tanpa command line)

1. Buka https://github.com dan login/daftar.
2. Klik **New repository** → beri nama, mis. `affilio-app` → pilih **Public** → Create repository.
3. Di halaman repo, klik **Add file → Upload files**.
4. Upload SEMUA file di folder ini: `index.html`, `manifest.json`, `sw.js`, `icon-192.png`, `icon-512.png`.
5. Klik **Commit changes**.
6. Buka tab **Settings → Pages** (di sidebar kiri, bagian "Code and automation").
7. Di **Build and deployment → Source**, pilih **Deploy from a branch**.
8. Branch: `main`, folder: `/ (root)` → **Save**.
9. Tunggu ~1 menit, lalu buka URL yang muncul, contoh:
   `https://<username-kamu>.github.io/affilio-app/`

Situs kamu sudah live dan bisa langsung "Add to Home Screen" dari Chrome Android.

## 2. Bungkus jadi APK dengan PWA Builder

1. Buka https://www.pwabuilder.com
2. Masukkan URL GitHub Pages kamu dari langkah 1, klik **Start**.
3. PWA Builder akan membaca `manifest.json` otomatis (skor akan hijau/oke).
4. Klik **Package for stores → Android**.
5. Pilih opsi default (Signing key: biarkan PWA Builder generate otomatis kalau
   ini untuk pemakaian pribadi/sideload, BUKAN untuk upload ke Play Store).
6. Download file `.apk` (atau `.aab` kalau mau ke Play Store nanti).

## 3. Pasang APK di HP Android

1. Pindahkan file `.apk` ke HP (lewat kabel USB, Google Drive, dsb).
2. Buka file itu di HP → izinkan "Install from unknown sources" kalau diminta.
3. Install seperti aplikasi biasa.

## Catatan penting

- Data tersimpan di **localStorage per perangkat/browser** — tidak otomatis
  sinkron antar HP. Kalau nanti kamu mau data tersinkron lintas perangkat,
  itu perlu backend/database tambahan (bisa saya bantu rancang kalau perlu).
- Simpan file `.apk` hasil build baik-baik — kalau mau publish ke Play Store
  nanti, kamu wajib pakai signing key yang SAMA setiap kali update.
