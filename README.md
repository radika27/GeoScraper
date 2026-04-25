# GeoScraper 🛰️

GeoScraper adalah aplikasi web berbasis GIS yang dirancang untuk mengekstrak (scrape), memvisualisasikan, dan mengolah data dari **OpenStreetMap (OSM)** secara masif (*batch-scraping*) dengan antarmuka *dashboard* modern.

👨‍💻 **Dibuat oleh:** [Radhyka Galih Pranata](https://www.linkedin.com/in/radhyka-galih-pranata-b78249209)  
🔗 **Repository:** [github.com/radika27/GeoScraper](https://radika27.github.io/GeoScraper)

---

## 🌟 Fitur Unggulan

- **SaaS Modern UI:** Antarmuka yang bersih, premium, mendukung *Dark/Light mode*, dan responsif di berbagai perangkat.
- **Geocoding Pintar:** Cukup ketik nama kota (misal: "Jakarta"), sistem akan otomatis menemukan koordinat wilayahnya.
- **Filter Geometri Canggih:** Memungkinkan pengguna menyaring hasil ekstraksi berdasarkan *Point* (Titik), *Line* (Garis), atau *Polygon* (Area).
- **Interaksi Map-Table Sinkron:** Mengklik salah satu baris di tabel data akan otomatis mengarahkan (zoom) peta tepat ke lokasi fitur tersebut.
- **Smart Data Export:** Unduh data dalam format **CSV**, **GeoJSON**, atau **KML** yang sepenuhnya kompatibel dengan Google Earth (mendukung data Polygon/Area). Data yang terekspor akan otomatis menyesuaikan dengan hasil filter Anda!

---

## 🚀 Cara Menggunakan Aplikasi

1. **Tentukan Area Target:** 
   Di panel kiri, masukkan nama daerah pada kolom "Area Target" lalu klik **Cari**, atau gunakan fitur *Draw* (ikon poligon) untuk menggambar batas area secara manual di atas peta.
2. **Pilih Kategori Objek:**
   Pilih kategori data dari menu dropdown (contoh: *Amenity*), lalu centang jenis tag/objek spesifik yang ingin dicari (contoh: *RS*, *Sekolah*).
3. **Mulai Ekstraksi Data:**
   Tekan tombol **Mulai Ekstraksi**. Aplikasi akan mengambil data dari Overpass API dengan metode antrean (batch) yang aman agar koneksi tidak terputus.
4. **Analisis Data:**
   Buka panel "Analitik" (di sebelah kanan). Anda bisa mencari nama fitur atau memfilter spesifik berdasarkan geometri. Diagram statistik akan otomatis ter-update mengikuti filter Anda secara *real-time*.
5. **Ekspor Data:**
   Klik salah satu format pada bagian **Export Data** untuk mengunduh hasil yang sudah disaring.

---

## 💻 Cara Menjalankan di Komputer Lokal

Karena aplikasi ini menggunakan modul web (*fetch API*), sangat disarankan untuk membukanya melalui *Local Web Server* agar terhindar dari pemblokiran *CORS policy* pada browser.

**Opsi 1: Menggunakan Python (Terminal / CMD)**
Buka terminal/CMD, arahkan ke direktori proyek ini, dan ketik:
```bash
python -m http.server 8000
```
Lalu buka browser Anda di: `http://localhost:8000/index.html`

**Opsi 2: Menggunakan VSCode Live Server**
1. Buka folder ini di *Visual Studio Code*.
2. Pastikan ekstensi **Live Server** sudah terpasang.
3. Klik kanan pada file `index.html` dan pilih **"Open with Live Server"**.

---

## 🛠️ Stack Teknologi & Library Pendukung

- HTML5, Vanilla CSS3, Vanilla JavaScript
- **Leaflet.js** (Peta Interaktif)
- **Leaflet MarkerCluster & Leaflet Draw** (Pengelompokan titik & alat menggambar area)
- **Chart.js** (Visualisasi data ke dalam diagram statistik)
- **Overpass API** (Penyedia data utama OpenStreetMap)
- **Nominatim API** (Mesin pencari Geocoding lokasi)
- **FontAwesome 6** (Koleksi Ikon)
