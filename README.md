<div align="center">

# 🌙 Taman Bulan · Naffa

**Situs ulang tahun interaktif, dengan 20 stage, sertifikat, photobooth, dan live chat.**

![Made with](https://img.shields.io/badge/dibuat%20dengan-%E2%9D%A4%EF%B8%8F-e8604c?style=flat-square)
![Stack](https://img.shields.io/badge/stack-HTML%20%C2%B7%20CSS%20%C2%B7%20JS-f2b441?style=flat-square)
![Deploy](https://img.shields.io/badge/deploy-GitHub%20Pages-7fae6a?style=flat-square)

</div>

---

## 📁 Struktur folder

```
├── index.html          situs utama (yang dibuka Naffa)
├── styles.css           semua CSS
├── script.js             semua JavaScript
├── chat.html             dashboard khusus Rizqi (balas chat & pantau progres real-time)
├── README.md
└── assets/
    ├── audio/             4 lagu playlist (.opus)
    ├── frames/             11 template bingkai photobooth (.webp)
    └── og-preview.webp     gambar preview saat link dibagikan
```

`index.html` dan `chat.html` **sudah saling terhubung otomatis** lewat Firebase (proyek
`adalahpokoknya-6cabf`, koleksi Firestore `live_chat`, `live_presence`, dll), jadi tidak perlu
konfigurasi tambahan, tinggal deploy semuanya bersamaan.

> [!NOTE]
> Ada satu potongan kode kecil (pengecekan tanggal buka gerbang + kelas anti-kedipan layar)
> yang **sengaja dibiarkan inline** di `index.html`, bukan dipindah ke `script.js`. Kode itu
> harus jalan sinkron sebelum halaman dirender, supaya tidak ada kedipan konten yang salah
> sebelum gerbang terkunci muncul. Jangan dipindahkan manual kalau suatu saat mengedit ulang.

---

## 🚀 Cara deploy ke GitHub Pages

| Langkah | Aksi |
|---|---|
| 1 | Buat repository baru di GitHub (public, atau private dengan GitHub Pro untuk Pages). |
| 2 | Upload seluruh isi folder ini ke **root** repo. Jangan taruh dalam subfolder, supaya `assets/...`, `styles.css`, dan `script.js` tetap ketemu filenya. |
| 3 | Buka **Settings → Pages**. |
| 4 | Di **Source**, pilih branch `main` dan folder `/ (root)`, lalu **Save**. |
| 5 | Tunggu 1–2 menit, situs aktif di `https://<username>.github.io/<nama-repo>/`. |
| 6 | `chat.html` otomatis ikut ter-deploy di `.../chat.html`. Ini khusus Rizqi, **jangan dibagikan ke Naffa**. Kode aksesnya ada di dalam file (cari `ACCESS_CODE`), ganti kalau mau lebih aman. |

---

## ⚠️ Catatan penting

<table>
<tr>
<td width="50%" valign="top">

**`og:image` pakai path relatif**

Setelah repo online, ganti jadi URL absolut supaya preview link muncul benar di
WhatsApp/Telegram:

```html
<meta property="og:image"
  content="https://<username>.github.io/<repo>/assets/og-preview.webp">
```

</td>
<td width="50%" valign="top">

**Format audio `.opus`**

Didukung penuh di Chrome, Firefox, Edge. Safari/iOS lama kurang konsisten. Kalau
target utamanya pengguna iPhone, siapkan cadangan `.mp3`/`.m4a`.

</td>
</tr>
</table>

---

<div align="center">
<sub>Dibuat dengan sepenuh hati, khusus untuk Naffa. 🌸</sub>
</div>
