# 🤖 WhatsApp Booking Automation with n8n

Sistem otomatisasi ini dibangun dengan [n8n](https://n8n.io) untuk memproses booking studio olahraga melalui WhatsApp dan menyimpan datanya ke Google Sheets secara otomatis.

---

## 🚀 Fitur Utama

- 🌐 Webhook endpoint dari WhatsApp API (Notif.my.id)
- 🧠 AI Agent (LangChain + Google Gemini 2.5 Pro) untuk mendeteksi maksud pesan pengguna
- ✅ NLP otomatis mengenali:
  - Booking lapangan (DAFTAR)
  - Cek status booking (CEK_STATUS)
  - Kirim bukti transfer (BUKTI_TRANSFER)
  - Permintaan harga (PRICELIST)
- 📄 Penyimpanan data booking ke Google Sheets
- 📡 Balasan otomatis ke WhatsApp melalui HTTP API

---

## 📁 Folder

| Folder/File         | Penjelasan                                  |
|---------------------|---------------------------------------------|
| `workflows/`        | File JSON hasil export dari n8n              |
| `assets/`           | Screenshot, diagram alur, atau mockup        |
| `README.md`         | Panduan setup dan dokumentasi                |
| `.gitignore`        | File yang diabaikan oleh Git (optional)     |

---

## 🧩 Teknologi

- n8n Cloud
- LangChain + Google Gemini Pro (via LangChain node)
- Google Sheets (OAuth2 API)
- Notif.my.id (WhatsApp API Gateway)

---

## ⚙️ Cara Import Workflow

1. Buka n8n editor.
2. Klik `Import` → `From File`.
3. Pilih file `booking-to-sheets-n8n.json`.
4. Konfigurasikan:
   - Google Sheets credential
   - API Key WhatsApp (`notif.my.id`)
   - Google Gemini credential (LangChain)

---

## 📝 Format Data di Google Sheets

| Kolom              | Keterangan                  |
|--------------------|-----------------------------|
| Timestamp          | Waktu pengiriman pesan      |
| Nama Akun WA       | Nama akun pengirim          |
| Nomor WA           | Nomor WhatsApp pengirim     |
| Nama               | Nama yang ingin booking     |
| Email              | Email pemesan               |
| Alamat             | Alamat pemesan              |
| Tanggal Booking    | Tanggal yang dibooking      |
| Jam Booking        | Jam yang dibooking          |
| Lokasi Main        | Lapangan atau Futsal        |
| Status DP          | Status pembayaran (Pending) |
| Bukti Transfer     | Link/cek bukti transfer     |

---

## 🛡️ Catatan Keamanan

- **JANGAN** push kredensial API (`apikey`, ID OAuth, URL Webhook) ke GitHub publik.
- Gunakan `.gitignore` untuk menghindari file sensitif.

---

## 👤 Kontributor

- Hefri Juanto — WhatsApp Automation Developer  
  [IG: @njtertop](https://instagram.com/hefrijunt)

---

## 📝 Lisensi

Proyek ini tersedia untuk kebutuhan pengembangan internal dan pembelajaran.

