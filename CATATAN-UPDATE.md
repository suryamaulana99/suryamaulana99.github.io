# Update situs, versi 2

## File di paket ini

```
index.html            (ganti file lama)
404.html              (baru)
cv.pdf                (ganti dengan CV terbaru)
sitemap.xml           (ganti, lastmod diperbarui)
og-image.jpg          (ganti, sudah dikompres 66 KB jadi 41 KB)
assets/
  surya-400.webp      (baru)
  surya-640.webp      (baru)
  surya-900.webp      (baru)
  surya-fallback.png  (baru, fallback untuk browser tanpa WebP)
```

## Yang harus dihapus dari repo

```
surya.png             (6,5 MB, sudah digantikan folder assets/)
```

## Cara pasang

```bash
# dari root repo suryamaulana99.github.io
git rm surya.png
# salin isi paket ini ke root repo (timpa yang lama)
git add -A
git commit -m "Perbarui konten dari CV terbaru dan rapikan gaya tulisan"
git push
```

`robots.txt` tidak diubah.

## Isi yang diperbarui dari CV

| | Sebelum | Sesudah |
|---|---|---|
| IPK | 3.49 | 3.47 dari 4.00, 122 SKS |
| Kelulusan | tidak disebut | perkiraan 2027 |
| Kerja praktik | Jun 2026 sampai sekarang | Jun 2026 sampai Sep 2026, Research Intern |
| Jumlah proyek | 6 | 9 |
| Sertifikasi | nama umum | nama dan versi lengkap, CCNAv7 diperjelas sebagai course Cisco Networking Academy |

Proyek baru: implementasi TR-369/USP pada GPON ONT, monitoring telemetri Telegraf
dan InfluxDB dan Grafana, diagnosis dan perbaikan Dell PowerEdge R730.

Skill baru: TR-369/USP, TR-069, MQTT, GPON dan ONT provisioning, Docker, Dell iDRAC,
InfluxDB, Telegraf, SSH, Apache2, NGINX, DNS, Python, Node.js, REST API.

Setiap entri riwayat sekarang punya poin detail yang diambil dari CV, dan ada blok
bahasa (Indonesia dan Inggris).

## Gaya tulisan

Seluruh tanda pisah (em dash dan en dash) sudah dihapus dari `index.html` dan
`404.html`, termasuk di judul proyek, rentang tanggal, dan tag `<title>`.
Rentang tanggal sekarang memakai kata "sampai".

Kalimat berpola AI juga dibuang, misalnya "bagian tersulit bukan membangunnya,
melainkan menjaganya" dan judul berpola "Dari X ke Y". Teksnya ditulis ulang jadi
kalimat biasa.

## Ukuran

| | Sebelum | Sesudah |
|---|---|---|
| Total halaman | ~6,75 MB | ~420 KB |
| Foto hero | 6,5 MB PNG 3000x4000 | 14 sampai 40 KB WebP responsif |
| index.html | 31 KB | 79 KB, sekitar 18 KB setelah gzip |
