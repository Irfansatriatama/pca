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

## Fitur (13 modul, sesuai Concept Deck SYS)
- **Workspace:** Guided Procurement (Smart Matching + Recommendation) · Recommended Catalog (Item/Vendor/HPS) · Buat Pengadaan (wizard 4-langkah + checklist P3/RPA) · Daftar Pengadaan (Historical Search & Filter) · Report & Analytics (Executive Summary, KPI, Budget Absorption, Anomali, Vendor & Price Risk, Kesimpulan Manajemen + Cetak)
- **Proses:** Persetujuan · Evaluasi Vendor & Kontrak · Master Data
- **Analitik:** Peluang Efisiensi (Spend Insight & Opportunity) · Risk Analysis (Risk Score, heatmap, Same-Spec Price Gap)
- **Aset & Otomasi:** Aset & Investasi Proyek (Klasifikasi item, Kontribusi %, Konversi PROYEK→INVESTASI, Custodian/Handover, Idle) · Serapan & Belanja (Ikhtisar Spend, Serapan RUP, Sewa vs Beli, Price Gap) · Otomasi & Peringatan (RPA Perpanjang + Digest + Rencana Aksi + Aktivitas)

Semua aksi dinamis & tersimpan (localStorage): approval, konversi aset, kontrak, handover, rencana aksi, draft PR — bertahan setelah reload. Tidak ada tombol yang hanya menampilkan toast kosong.

## Data
`dummy_pengadaan_40k.csv` — 40.000 baris item (11.354 pengadaan, 2.644 vendor), delimiter `;`.

## Catatan
Prototype. Sebagian metrik nyata dari data (kontribusi %, price gap, serapan, sewa-vs-beli), sebagian heuristik/proxy (pemegang = Nama Pemohon, status idle). Target RUP & klasifikasi KLU/KBLI perlu data tambahan.
