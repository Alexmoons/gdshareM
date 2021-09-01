# GDshareM
Hanya memodifikasi sedikit dan menerjemahkan beberapa di bagian.  Just modifying and translating some parts. 
Mungkin masih ada yang belum diubah dan diterjemahkan atau mungkin ada kesalahan. **Harap maklum wkwk**
### Source: ###
* https://github.com/iwestlin/gdshare
* https://github.com/masbodo/gedeshare

### Untuk Indtroduction, changelog, dan tips bisa dilihat di [sini](dist/README.md)

## Cara Konfigurasi
Buka file [template-indonesia.js](./template-indonesia.js), lalu ubah variable sesuai pentunjuknya.
```javascript
const CONFIG = {
    PASSKEY: "", // Ini adalah kunci masuk kamu", // Kunci masuk ke web sebagai administrator, silakan buat sendiri dan serumit mungkin
    HASHKEY: "", // Ini adalah kunci hash kamu", // Digunakan untuk memverifikasi link download dan share link yang kamu buat. Silahkan buat sendiri dan serumit mungkin. Setelah diubah, link download dan share link yang dibuat sebelumnya menjadi tidak valid
    RETRY_LIMIT: 5, // Biasanya kesalahan akan dilaporkan ketika Google Drive Api dipanggil untuk membaca direktori, berikut ini adalah jumlah maksimum percobaan ulang yang diizinkan
    PAGESIZE: 30, // Jumlah objek dalam satu halaman, batasnya adalah 1000
    ORDERBY: 'modifiedTime', // Nilai opsional yang "modifiedTime" atau "name", masing-masing akan menguurutkan file berdasarkan Terakhir kali diubah dan menurut nama file
    DESC: true, // Nilai opsional "true" atau "false", masing-masing akan menampilkan file diurutan dari atas atau terbalik/dari bawah
    AUTH: {
        client_id: "", // Ini adalah informasi otorisasi akun Google Drive pribadi kamu, sama seperti goindex
        client_secret: "", // Sama seperti di atas
        refresh_token: "", // Sama seperti di atas
        expires: 0,
        access_token: "" // Opsional
    }
}
```
Setelah mengubah variabel, lalu salin dan tempel seluruh isi yang ada di `template-indonesia.js`  ke [Cloudflare Workers](https://workers.cloudflare.com/). Silahkan lihat referensi di [sini](https://www.jiyiblog.com/archives/031279.html)
