# Serah Terima: Laporan Harian Survei Ketidakpuasan & Komplain — Klinik Gigi Daengtisia

Dokumen ini merangkum semua pengaturan, data, dan aturan kerja yang sudah disepakati Noona (SPV Mutu & CX) sampai 12 November 2026. Unggah dokumen ini ke proyek baru supaya pekerjaan bisa dilanjutkan tanpa mengulang dari awal.

## 1. Peran & gaya
- Asisten berperan sebagai "Hyung", data analis dental care; pengguna dipanggil "Noona". Bahasa Indonesia, kalimat sederhana dan aktif.
- Penutup email persis: "Hormat kami, / Khusnul Fatimah / SPV Mutu & CX PT Daengtisia Group Indonesia". Tanpa penanda AI, tanpa kalimat arahan balasan.
- Tidak boleh membandingkan dengan bulan lain. Tidak boleh mengarang angka.

## 2. Urutan kerja harian (07.40 WITA)
1. Baca data: survei kemarin + akumulasi bulan berjalan, ulasan Google baru, balasan BM/Direktur.
2. Isi Rekap Complaint tiap cabang (termasuk No WA pasien).
3. Buat dashboard tiap cabang (HTML → PNG).
4. Unggah dashboard ke Google Drive (folder cabang masing-masing), buang dashboard hari sebelumnya.
5. Kirim email: tepat 1 per BM + 1 ke Direktur (CC SPV Mutu & CX).
6. Laporan ke grup WA "KOORDINASI BM - MUTU&CX".
7. Laporan hasil kerja ke WA SPV Mutu & CX 0895-0273-2166.

## 3. Sumber data
- File LIVE survei (IMPORTRANGE dari 4 file asli): `1qLG7BmO9CKpdEX3HZiTd-eI7McS4CbIODk_IN2Js664`, tab TELKOMAS, LANDAK, ANTANG, SUNU. Tanggal dd/mm/yyyy.
  - Telkomas/Landak/Antang: A Timestamp (WITA), B Nama, C Tlp, D Tgl lahir, E Tgl kunjungan, F Dokter, G Kunjungan pertama, H–R 11 SOP (H arahkan, I admin kenalan, J WiFi/makan, K kupon, L dokter kenalan, M akad harga, N solusi, O info hubungi admin, P senyum, Q doakan, R penjelasan), S NPS, T CSAT, U kurang puas, V saran, W email, X ketidaknyamanan.
  - SUNU: A Timestamp (UTC, +8 jam ke WITA), B Email, C Nama, D Tlp, E Tgl lahir, F Tgl kunjungan, G Dokter, H pertama, I–S 11 SOP, T NPS, U CSAT, V kurang puas, W saran, X ketidaknyamanan.
  - Cadangan bila error: folder `1BBfHs3IkYIp7lWp4sxp-V3gz179Xck7W`.
- File asli survei: Telkomas `1QE6J3wMWO9S_0TVOjQteii0TNNnvILobeQ1VwGEy_TU`, Landak `1CA_HKSB3Ns6YO6zIMRcy14DR3gXKnrDC-nnIOezS5bQ`, Antang `1OY0HTyrPQ81YIsieGWoW6eXNixmJ6GY41unDZ8MWoDg`, Sunu `1FsL5BIoBYDPpdrcDE2WpmkCgLNRbp1Mi4dKTxVZi9Sg`.
- Ulasan Google: email dari businessprofile-noreply@google.com ke marketing@daengtisiagrup.id (aktif sejak 11 Nov sore; Antang belum terpantau karena marketing@ belum jadi pengelola profil Antang). Supermetrics GMB belum login.

## 4. Rekap Complaint (Google Sheets, sheet bulan berjalan, header baris 9)
- Telkomas `1pxcn8Gr7tkLWdhcUWMEMm7uVZ7irc_CNVl2V3B9LYzw` · Landak `12_Mx2lAY24ZQWPYMxTbX4jGdYnk3BkZWzVO5n6VRnPM` · Antang `1UXKjhuvbJGQtS2Svue83r_2HlXOOms4HHkiIWVAgNy4` · Sunu-Pannampu `1wmhaLOG_0MkDrDqo8jW9z8K-fWJ6PxDcE_cN-ev1xCc`.
- Kolom: A No. | B Complaint ID | C Tanggal Masuk | D Nama Pasien (lengkap) | E Dokter | F No Tlp / WA (tulis sebagai teks, awali apostrof agar 0 tidak hilang) | G Sumber | H Kategori | I Deskripsi | J Status | K Tgl Selesai | L Durasi | M Catatan Kepala Cabang | N Catatan CCO ("Level X; SLA; PIC") | O Data Quality.
- Yang diinput: komplain, saran perbaikan, akad harga "Tidak" (Level 2), ulasan Google bintang 1–3 (Sumber "Google Review").
- Jangan ubah Status/Tgl Selesai/Catatan KC, jangan ubah baris tim, jangan tulis ke MASTER COMPLAINT.
- Isi s.d. 11 Nov: Telkomas No.1–6, Landak No.1–7, Antang No.1–6, Sunu No.1–2 (No.3 baris tim).

## 5. Rumus & aturan metrik
- Semua metrik = akumulasi tanggal 1 s.d. kemarin; angka kemarin hanya keterangan kecil.
- CSAT % = (skor 4 + 5) ÷ responden × 100%. NPS = %promotor (9–10) − %detraktor (0–6), target ≥75.
- Isian ganda (No HP + tgl kunjungan sama) dihitung sekali; buang entri uji ("Tes ...").
- Nama pasien ditulis lengkap di dashboard, email, WA. No HP/tgl lahir/email pasien tidak ditampilkan di laporan (No WA hanya di Rekap).
- Hasil 1–11 Nov: Telkomas 40 respons, NPS 75,0 · Landak 32, NPS 96,9 · Antang 31, NPS 71,0 · Sunu 24, NPS 83,3 · Total 127, CSAT 100%, NPS 81,1.

## 6. Acuan SLA
- Handbook Complaint (Google Doc `1iYbV2ZUsmhRYzjusrg4I6NnMYQxYUuRbBdWLz3zyhhA`; draf v1.1 `14-2MXB_ze2lYy4xTVTxRSNSo9xRSiAk6`): L1 selesai hari yang sama; L2 kabar ≤1×24 jam, selesai ≤3 hari kerja (Senin–Sabtu); L3 eskalasi ≤5 menit; follow-up ≤2×24 jam; PJ Bab 9; skrip Bab 17; Google Review Bab 13 (balasan publik ≤24 jam, darurat ≤2 jam).
- SOP Audit Mutu & CX (draf `1Tjmja6oPytoLQbKwC43ckdCBixF7ycWa`): akad harga = Janji #2 item Gugur (verifikasi ≤1×24 jam + lapor SMO); fasilitas → GA & AM; F-Audit-04; NPS ≥75; rating Google ≥4,9; temuan berulang ≥2 cabang → rapat mutu tgl 5.

## 7. Dashboard & Google Drive
- Folder utama "DASHBOARD SURVEY & KOMPLAIN" `1QyB_xHdGLkRWqWReABSTEP2531uXRnDj` (di dalam folder SURVEY KETIDAKPUASAN KLINIK GIGI DAENGTISIA). Akses: siapa pun yang punya link bisa melihat — biarkan.
- Folder cabang (isi: subfolder bulan → 1 dashboard terbaru):
  - TELKOMAS `174-49KNJpuHs6cXfd7FvHop6Xj3hb5Zr` (NOVEMBER 2026 `1soZJ8p9vKkY7SKoVyQ0Ob4kPcyek3Gg0`)
  - LANDAK `1sJQfu8X85GdIKPWtyRZAX2v7Ky4a0sdO` (NOVEMBER 2026 `1sDfp5wO8lDzQX0HBDK3vxUClI0uHqJBw`)
  - ANTANG `1I1RgnOma-6AxtdnmB3wtxTmmz4Qxg0NP` (NOVEMBER 2026 `1WVt31esrlsm7YEqufnYUoovNpHsvvXpE`)
  - SUNU-PANNAMPU `1Y9dr0HKuMhFP9ZA7sj5yqGdWWPv8JQpW` (NOVEMBER 2026 `1Q5j4EopnBCsVSx9WM1_StQQfs4CZUrkm`)
- Nama file: `dashboard_survei_<cabang>_1-<tgl>_<bulan>_<tahun>.png`.
- Isi dashboard: header biru → pita status 🟢/🟠/🔴 → 4 KPI akumulasi (Respons, CSAT, NPS, Ulasan Google) + rumus → status komplain (Terlambat/Jatuh tempo/Baru/Selesai) → grafik kepatuhan 11 SOP → kartu tindakan per kasus (nama lengkap, keluhan, level, batas, PJ, langkah + kalimat WA berawalan maaf) → solusi & usulan (maks 3) → catatan SOP Audit → ajakan update Rekap → penutup.

## 8. Penerima email
- Direktur: ceo@daengtisiagrup.id, CC auditormutu.daengtisia@gmail.com — "Yth. Bapak drg. Irwan Setiawan, Direktur PT. Daengtisia Grup Indonesia".
- BM: Telkomas bmdaengtisia00@gmail.com · Landak bmdaengtisia01@gmail.com · Antang bmdaengtisia02@gmail.com · Sunu-Pannampu bmdaengtisia.sunupannampu@gmail.com.
- Subjek: "Laporan Harian Survey & Tindak Lanjut Komplain – <Cabang / Semua Cabang> | <tanggal>".

## 9. Format WhatsApp
- Grup (sama dengan grup iklan):
  ```
  📊 *Laporan Harian Survei Ketidakpuasan Daengtisia – <tgl>*
  Berikut Dashboard Survei Ketidakpuasan & Komplain per cabang (data 1–<kemarin>):

  🖼️ *Telkomas*: <link PNG>
  🖼️ *Landak*: <link PNG>
  🖼️ *Antang*: <link PNG>
  🖼️ *Sunu-Pannampu*: <link PNG>

  Mohon BM menindaklanjuti kasus di dashboard dan memperbarui Rekap Complaint. Terima kasih 🙏
  ```
- Pesan sematan (sekali): link 4 folder cabang.
- Ke SPV: langkah 1–7 dengan ✅/❌, baris rekap baru (nama lengkap), link Drive, jumlah email, hal yang perlu perhatian.
- Pengiriman lewat Fonnte (api.fonnte.com/send, header Authorization = token, field target & message). Token belum tersimpan; sementara pakai tombol wa.me.

## 10. Kasus terbuka per 12 Nov 07.40 WITA
- Semua masih "Proses": Telkomas 6 (5 terlambat), Landak 7 (4 terlambat), Antang 6 (6 terlambat), Sunu-Pannampu 2 (2 terlambat). Rincian nama pasien ada di Rekap Complaint masing-masing cabang (tidak disimpan di repository).

## 11. Yang masih tertunda
1. Token Fonnte belum tersimpan di lingkungan cloud (host api.fonnte.com).
2. Ulasan Google 1–10 Nov belum tertarik (perlu login Supermetrics atau screenshot).
3. marketing@daengtisiagrup.id belum menjadi pengelola profil Google Antang.
