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
