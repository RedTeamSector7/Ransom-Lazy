# 🛑 Ransomware Lazy

> ⚠️ **Peringatan:** Proyek ini adalah simulasi dan dokumentasi dari sebuah ransomware yang kompleks. Semua eksperimen hanya boleh dilakukan di lingkungan tertutup dan legal, seperti sandbox atau VM penelitian.

---

## 📌 Deskripsi

**Ransomware Lazy** adalah malware enkripsi tingkat lanjut yang menggunakan kombinasi **AES-256-CBC** dan **RSA** untuk mengenkripsi data pengguna. Malware ini dikembangkan dengan tujuan utama untuk demonstrasi dan riset keamanan siber, bukan untuk disebarluaskan secara ilegal.

---

## 🔐 Mekanisme Enkripsi

- **Algoritma Simetris:** AES-256 (mode CBC)
- **Algoritma Asimetris:** RSA (public key encryption untuk AES key)
- **Ekstensi Output:** `.lazy` untuk setiap file terenkripsi
- **File kunci:** AES key disimpan dan dienkripsi menggunakan RSA public key (`public.pem`)

---

## 🛠️ Fitur Utama

| Fitur                   | Deskripsi                                                                 |
|------------------------|---------------------------------------------------------------------------|
| 🔐 **Enkripsi Data**     | Semua file target dienkripsi menggunakan AES 256-bit + RSA                |
| 🛡 **UAC Bypass**        | Bypass hak administrator melalui teknik Registry dan silent escalation    |
| 🧬 **Bypass Antivirus**  | Memodifikasi Registry Defender dan layanan Windows secara diam-diam      |
| 🔁 **Persistence**       | Menambahkan diri ke Startup folder untuk persistensi setelah reboot      |
| ⌨ **Keylogger**         | Mencatat input keyboard korban secara diam-diam                          |
| 🌐 **Server C2C**        | Terhubung ke server Command and Control (C2C) untuk komunikasi            |
| 🧾 **Show Ransom Note**  | Menampilkan pesan tebusan menggunakan GUI                                |
| 📤 **Data Exfiltration** | Mengunggah file target ke server remote (mengunduh salinan korban)       |
| 💻 **send_info_device**  | Mengirim informasi sistem: IP, lokasi, OS, antivirus, user, dll.         |
| 🧭 **Panel Admin**       | Mendukung integrasi dengan backend/admin panel berbasis Flask/Django     |

---

## 📁 File & Struktur

- `main.py` – Entrypoint skrip ransomware (ter-encode)
- `lazy.py` – Loader marshal yang mengeksekusi bytecode terenkripsi
- `public.pem` – RSA public key untuk mengenkripsi AES key
- `aes_key.bin` – Kunci AES terenkripsi (jika disimpan lokal)
- `.lazy` – Ekstensi file yang telah dienkripsi

---

## 🧪 Mode Operasi

- **Silent Execution**: Tidak menampilkan konsol jika dijalankan dari `.exe`
- **Autonomous**: Tidak membutuhkan interaksi pengguna
- **Online/Offline Mode**: Tetap bisa mengenkripsi tanpa koneksi internet

---

## ⚠️ Legal Disclaimer

Penggunaan proyek ini hanya diperbolehkan untuk:

- **Penelitian keamanan siber**
- **Analisis malware**
- **Pengujian honeypot / EDR**
- **Simulasi serangan di lab tertutup**

Segala penyalahgunaan untuk tujuan kriminal atau distribusi ilegal dapat dikenai sanksi hukum sesuai yurisdiksi masing-masing.

---

## 🧑‍💻 Kontributor

- **Nama:** [Anonim / Peneliti Keamanan]
- **Tujuan:** Edukasi & riset keamanan ofensif

---

## 📜 Lisensi

Distributed for research and educational purposes only. Use at your own risk.

---


