# PCA — Procurement Intelligence (Prototype)

Aplikasi pengadaan cerdas **satu-file** (`pca.html`) berbasis histori CSV. Ringan (±137 KB), tanpa dependency eksternal, AI summary memakai statistik lokal (tanpa API key).

## Cara Testing

### 1. Server lokal (auto-load CSV) — direkomendasikan
```bash
python -m http.server 8000
# buka http://localhost:8000/pca.html
```
Data `dummy_pengadaan_40k.csv` termuat otomatis.

### 2. Dobel-klik file
Buka `pca.html`, klik **Impor CSV**, pilih `dummy_pengadaan_40k.csv`.

### 3. GitHub Pages (live)
Settings → Pages → Branch `main` → Save. Akses: `https://irfansatriatama.github.io/pca/`

## Fitur (12 modul)
- **Workspace:** Guided Procurement · Buat Pengadaan · Daftar Pengadaan · Report & Analytics
- **Proses:** Persetujuan · Evaluasi Vendor & Kontrak · Master Data
- **Analitik:** Peluang Efisiensi · Risk Analysis
- **Aset & Otomasi:** Aset & Investasi Proyek · Serapan & Belanja · Otomasi & Peringatan (RPA + Digest)

## Data
`dummy_pengadaan_40k.csv` — 40.000 baris item (11.354 pengadaan, 2.644 vendor), delimiter `;`.

## Catatan
Prototype. Sebagian metrik nyata dari data (kontribusi %, price gap, serapan, sewa-vs-beli), sebagian heuristik/proxy (pemegang = Nama Pemohon, status idle). Target RUP & klasifikasi KLU/KBLI perlu data tambahan.
