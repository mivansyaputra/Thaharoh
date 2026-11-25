# THOHAROH LAUNDRY (Android)

Web app kasir laundry dibungkus jadi APK memakai Capacitor. APK dibuat otomatis oleh GitHub (GitHub Actions), tidak perlu Android Studio.

## Cara dapat APK
1. Buat repository baru di github.com (nama `thoharoh-laundry-android`, Public atau Private).
2. Upload SEMUA isi folder ini, termasuk folder `.github`, `assets`, `www`. Catatan: folder berawalan titik sering tersembunyi di Windows; aktifkan **Tampilkan item tersembunyi**. Upload lewat web kadang melewatkan `.github`; kalau Actions tidak jalan, buat manual: Add file > Create new file > ketik `.github/workflows/build-apk.yml` lalu tempel isinya.
3. Buka tab **Actions**. Build jalan otomatis (3-8 menit). Kalau tidak, pilih **Build APK > Run workflow**.
4. Setelah hijau, klik run-nya, scroll ke **Artifacts**, unduh `THOHAROH-LAUNDRY-apk` (zip), ekstrak, dapat file `.apk`.
5. Kirim APK ke HP, buka, izinkan **Install dari sumber tidak dikenal**, install.

## Revisi
Timpa `www/index.html` dengan versi baru, commit. APK baru otomatis dibuat.

## Batasan yang harus diketahui
- **Cetak struk (window.print) tidak jalan di APK.** WebView Android tidak mendukungnya. Belum ada pengganti; kalau perlu, struk bisa dibuat jadi teks yang dibagikan ke WhatsApp/printer Bluetooth.
- Backup dan ekspor CSV memakai menu Bagikan Android (Filesystem + Share). Ini belum diuji di perangkat. Kalau gagal, kabari.
- APK ini versi debug (ditandatangani kunci debug). Cukup untuk dipasang sendiri, tidak untuk Play Store.
- Data di penyimpanan aplikasi. Hapus data aplikasi atau uninstall = data hilang. Backup rutin.
- Belum ada login.
