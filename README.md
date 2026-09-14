# 🔥 F34RDOWN & WORM-GPT WHATSAPP BOT

Panduan instalasi lengkap bot WhatsApp berbasis Baileys dan OpenRouter AI untuk dijalankan di **Termux (Android)** maupun **Linux (Ubuntu/Debian)**.

---

## 📦 KEBUTUHAN UTAMA (DEPENDENCIES)

Sebelum mulai, pastikan sistem lu udah terinstall:
1. **Node.js** (Versi 18.x atau terbaru)
2. **NPM** (Biasanya udah satu paket sama Node.js)
3. **Git** (Buat clone repo jika diperlukan)
4. **FFmpeg** & **Libwebp** (Wajib buat pemrosesan media/sticker)

---

## 📱 CARA INSTALL DI TERMUX (ANDROID)

Buka aplikasi Termux lu, lalu jalankan perintah berurutan ini satu per satu:

bash
# 1. Update dan upgrade package Termux
pkg update && pkg upgrade -y

# 2. Install Node.js, Git, FFmpeg, dan Build Essentials
pkg install nodejs git ffmpeg make python -y

# 3. Buat folder project dan masuk ke dalam foldernya
mkdir f34rdown-bot && cd f34rdown-bot

# 4. Inisialisasi package.json (jika belum ada)
npm init -y

# 5. Install semua dependencies yang dibutuhkan script
npm install @whiskeysockets/baileys pino readline openai axios

---

## 🐧 CARA INSTALL DI LINUX (UBUNTU / DEBIAN)

Buka terminal Linux lu, lalu jalankan perintah berikut:

bash
# 1. Update system repository
sudo apt update && sudo apt upgrade -y

# 2. Install curl dan dependensi dasar
sudo apt install curl git ffmpeg build-essential -y

# 3. Install Node.js versi terbaru (LTS) dari Nodesource
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt install -y nodejs

# 4. Buat direktori bot dan masuk
mkdir f34rdown-bot && cd f34rdown-bot

# 5. Install dependencies Baileys, OpenAI, dan Axios
npm install @whiskeysockets/baileys pino readline openai axios

---

## ⚙️ KONFIGURASI SCRIPT

1. Simpan script bot utama lu dengan nama `index.js` di dalam folder project `FIRDHAN_BOT_WA`.
2. Buka file `index.js`, lalu masukkan API Key OpenRouter lu ke dalam array `apiKeys`:
javascript
   const apiKeys = [
       "sk-or-v1-API_KEY_LU_DISINI",
   ];

   ---

## 🚀 CARA MENJALANKAN BOT

1. Jalankan script menggunakan Node.js:
bash
--------------------
   node index.js

3. Masukkan nomor WhatsApp bot lu saat diminta di terminal (format: `628123456789`).
4. Salin **Kode Tautan (Pairing Code)** yang muncul di terminal, lalu masukkan ke perangkat WhatsApp lu (*Setelan > Perangkat Tertaut > Tautkan dengan nomor telepon*).
5. Selesai! Bot lu bakal aktif dan siap dipakai. 😈
