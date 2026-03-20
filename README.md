<div align="center">

<img src="https://img.shields.io/badge/Pinterest--Downloader-v2.3.0-e60023?style=for-the-badge&logo=pinterest&logoColor=white" alt="Pinterest-Downloader v2.3.0" />

# 📌 Pinterest Downloader

### Download Pinterest videos, images, and boards — free, no watermark, no account needed.

[![Node.js](https://img.shields.io/badge/Node.js-20.x-339933?style=flat-square&logo=node.js&logoColor=white)](https://nodejs.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen?style=flat-square)](https://github.com/Advay254/Pinterest-Downloader/pulls)
[![Deploy on Render](https://img.shields.io/badge/Deploy%20on-Render-46E3B7?style=flat-square&logo=render&logoColor=white)](https://render.com)

<br/>

<a href="https://www.buymeacoffee.com/advay254" target="_blank">
  <img src="https://img.shields.io/badge/Support%20Me-%E2%98%95%20Buy%20Me%20a%20Coffee-e60023?style=for-the-badge&logo=buy-me-a-coffee&logoColor=white" alt="Support Me" />
</a>

<br/><br/>

> Paste a Pinterest link. Get your media. No sign-up, no watermark, ever.

<br/>

![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=16&pause=1000&color=E60023&center=true&vCenter=true&width=500&lines=Download+Pinterest+Videos+%F0%9F%8E%AC;Save+Pinterest+Images+%F0%9F%96%BC%EF%B8%8F;Bulk+Download+Entire+Boards+%F0%9F%93%A6;No+Watermark.+No+Account.+Always+Free.)

<br/>

![Pinterest Downloader Demo](https://raw.githubusercontent.com/Advay254/Pinterest-Downloader/main/og-image.jpg)

</div>

---

## ✨ Features

<img align="right" width="380" src="https://media.giphy.com/media/qgQUggAC3Pfv687qPC/giphy.gif" alt="coding gif"/>

- 📌 **Pinterest video downloads** — full quality, no watermark
- 🖼️ **Image downloads** — save single pins in HD
- 📦 **Board downloads** — bulk download entire boards as a zip
- 📱 **Full PWA** — installable on Android and iOS
- 📲 **Android APK** — native app, no browser bar
- ⚡ **Fast and lightweight** — no bloat, no tracking
- 🔒 **Secure** — no data stored, no login required
- 🚀 **Deploy anywhere** — Render, Railway, Fly.io, any Node.js host

<br clear="right"/>

---

## 🗂️ Project Structure

```
Pinterest-Downloader/
├── index.js          # Launcher — fetches and starts the core engine
├── package.json      # Launcher dependencies only
├── .env.example      # Environment variable reference
├── version.txt       # Current release version
└── .gitignore
```

> The core application is loaded securely at runtime. This keeps the source lean and the deployment simple.

---

## 🚀 Quick Start

### 1. Fork or clone the repo

```bash
git clone https://github.com/Advay254/Pinterest-Downloader.git
cd Pinterest-Downloader
```

### 2. Install dependencies

```bash
npm install
```

### 3. Set up environment variables

```bash
cp .env.example .env
```

Edit `.env` with your values:

```env
SITE_URL=http://localhost:3000
API_MASTER_KEY=your_master_key_here
RAPIDAPI_PROXY_SECRET=your_rapidapi_secret_here
```

### 4. Run

```bash
npm start
```

Visit `http://localhost:3000` — you're live. 🎉

---

## 🔑 Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| `SITE_URL` | ✅ **Yes** | Full production domain. Example: `https://yoursite.onrender.com` |
| `API_MASTER_KEY` | ✅ **Yes** | Master key that protects internal API endpoints |
| `RAPIDAPI_PROXY_SECRET` | ✅ **Yes** | Secret for RapidAPI proxy authentication |
| `AD_DECOY_1_URL` | Optional | First ad decoy URL — leave blank to disable |
| `AD_DECOY_2_URL` | Optional | Second ad decoy URL — leave blank to disable |
| `AD_WAIT_URL` | Optional | Ad wait page URL — leave blank to disable |
| `PORT` | Auto | Set automatically by Render — do not set manually |

---

## 🌐 Deploying to Production

### Render (recommended)

<img align="right" width="300" src="https://media.giphy.com/media/RbDKaczqWovIugyJmW/giphy.gif" alt="deploy gif"/>

1. Fork this repo to your GitHub account
2. Go to [render.com](https://render.com) and create a new **Web Service**
3. Connect your forked repo
4. Set **Build Command:** `npm install`
5. Set **Start Command:** `npm start`
6. Add your environment variables under **Environment**
7. Click **Deploy**

> Render free tier sleeps after 15 minutes of inactivity. Use [cron-job.org](https://cron-job.org) to ping your `/api/health` endpoint every 10 minutes to keep it awake.

<br clear="right"/>

### Railway

```bash
npm install -g @railway/cli
railway login && railway init && railway up
```

Add your environment variables in the Railway dashboard under **Variables**.

### Any VPS (Ubuntu/Debian)

```bash
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
sudo apt-get install -y nodejs
git clone https://github.com/Advay254/Pinterest-Downloader.git
cd Pinterest-Downloader && npm install
npm install -g pm2
pm2 start index.js --name pinterest-downloader
pm2 save && pm2 startup
```

---

## 🛠️ How It Works

```
User deploys Pinterest Downloader
        ↓
Launcher starts and fetches the core engine securely at runtime
Core engine extracts and installs its own dependencies
        ↓
App starts — ready to accept Pinterest URLs
        ↓
User pastes a Pinterest pin, video, or board URL
        ↓
Server fetches media metadata and resolves download links
        ↓
User downloads video, image, or full board zip
No watermark. No account. No hassle.
```

---

## 📊 Tech Stack

<div align="center">

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![PWA](https://img.shields.io/badge/PWA-5A0FC8?style=for-the-badge&logo=pwa&logoColor=white)
![Render](https://img.shields.io/badge/Render-46E3B7?style=for-the-badge&logo=render&logoColor=white)

</div>

---

## 🔄 Updates

Check `version.txt` for the latest release version. Sync your fork and redeploy on Render to get the latest update automatically.

---

## 🤝 Contributing

1. Fork the repo
2. Create your branch: `git checkout -b feature/your-feature`
3. Commit: `git commit -m 'Add your feature'`
4. Push: `git push origin feature/your-feature`
5. Open a Pull Request

---

## ⚠️ Disclaimer

Pinterest Downloader is an independent open-source project and is **not affiliated with, endorsed by, or connected to Pinterest** in any way.

This tool is intended for downloading your own saved content or content you have the right to download. Users are responsible for complying with Pinterest's terms of service and copyright laws in their country.

---

## 📄 License

MIT © 2026 Advay — free to use, modify, and distribute.

---

<div align="center">

![Visitor Count](https://visitor-badge.laobi.icu/badge?page_id=Advay254.Pinterest-Downloader)

**If Pinterest Downloader saved you time, drop a ⭐ — it helps others find the project.**

<br/>

<a href="https://www.buymeacoffee.com/advay254" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>

</div>
