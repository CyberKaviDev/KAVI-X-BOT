﻿[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&center=true&size=60&pause=1000&width=435&height=100&lines=KAVI-X+MD)](https://git.io/typing-svg)

KAVI-X is a Multi-Device WhatsApp bot developed by **Cyber Kavi**. It is designed to provide various automation features and can be deployed on multiple platforms.

---

## 🔧 Setup KAVI-X

### 1️⃣ PAIR Code

<a href='https://kavi-x-bot-login.up.railway.app/' target="_blank">
<img alt='PAIR CODE' src='https://img.shields.io/badge/PAIR_CODE-100000?style=for-the-badge&logo=scan&logoColor=white&labelColor=black&color=black'/>
</a>

---

## 🚀 Deployment Options

---

### 🔹 Deploy to **Heroku**
1. If you don’t have a Heroku account, create one.
   
   <a href='https://signup.heroku.com/' target="_blank">
   <img alt='Heroku' src='https://img.shields.io/badge/-Create-black?style=for-the-badge&logo=heroku&logoColor=white'/>
   </a>

2. Deploy KAVI-X:
   
   <a href='https://www.heroku.com/' target="_blank">
   <img alt='Heroku Deploy' src='https://img.shields.io/badge/-Deploy-black?style=for-the-badge&logo=heroku&logoColor=white'/>
   </a>

---

### 🔹 Deploy to **Railway**
1. Create an account on Railway:
   
   <a href='https://railway.app/login' target="_blank">
   <img alt='Railway' src='https://img.shields.io/badge/-Create-black?style=for-the-badge&logo=railway&logoColor=white'/>
   </a>

2. Deploy KAVI-X:
   
   <a href='https://railway.com/' target="_blank">
   <img alt='Deploy Railway' src='https://img.shields.io/badge/-Deploy-black?style=for-the-badge&logo=railway&logoColor=white'/>
   </a>

---

### 🔹 Deploy with **GitHub Codespaces**
1. Click below to open KAVI-X in a GitHub Codespace:

   <a href="https://github.com/codespaces/new?hide_repo_select=true&repo=KaviDeveloperSe/KAVI-X-BOT" target="_blank">
   <img alt="Open in Codespaces" src="https://img.shields.io/badge/Open%20in%20GitHub%20Codespaces-121013?style=for-the-badge&logo=github&logoColor=white"/>
   </a>

---

### 🔹 Deploy with **GitHub Actions**

1. Fork the repo and enable GitHub Actions.  
2. Go to **Actions → set up a workflow yourself**.  
3. Create the workflow file at:  
   `.github/workflows/deploy.yml`  
4. Paste the following code into the file:

<details>
<summary>📜 <strong>Click to view GitHub Actions deploy.yml</strong></summary>

```yaml
name: Node.js CI

on:
  push:
    branches:
      - main
  pull_request:
    branches:
      - main

concurrency:
  group: ${{ github.workflow }}-${{ github.ref }}
  cancel-in-progress: true

jobs:
  build:
    runs-on: ubuntu-latest

    strategy:
      matrix:
        node-version: [20.x]

    steps:
      - name: Checkout repository
        uses: actions/checkout@v3

      - name: Set up Node.js
        uses: actions/setup-node@v3
        with:
          node-version: ${{ matrix.node-version }}

      - name: Clean dependencies and install specific versions
        run: |
          rm -rf node_modules package-lock.json
          npm install cheerio@1.0.0-rc.12 css-select@5.1.0 --legacy-peer-deps

      - name: Install remaining dependencies
        run: npm install --legacy-peer-deps

      - name: Start application
        run: npm start
```
</details>

---

### 🔹 Deploy on **VPS**
You can also deploy KAVI-X on your **own VPS**. Ensure you have **Node.js 22+** installed and set up the **environment variables**.

---

## ⚙️ Environment Variables
Ensure to set the following **environment variables** correctly:

```env
SESSIONID='Put Your Session ID Here'
BOTNAME='KAVI-X MD'
OWNERNUMBER='94702128378'
OWNERNAME='Cyber Kavi'
WEBSITEX='https://kavi-x-bot-login.up.railway.app/'
WAGC='https://chat.whatsapp.com/CG9f0paHJzwDImXiydfuht'
BOTSCRIPT='https://github.com/KaviDeveloperSe/KAVI-X-BOT'
PACKNAME='KAVI-X MD'
AUTHOR='Cyber Kavi'
CREATOR='94702128378@s.whatsapp.net'
BOTPREFIX='.'
RESTART='true'
MONGODB_URI='Put Your Mongo DB URI Here'
```
---

## 🔗 KAVI-X Support

Join the **KAVI-X WhatsApp community** for updates and support:

<a href="https://whatsapp.com/channel/0029VajVe7sC1FuI2qVvRM1R">
<img alt="WhatsApp Channel" src="https://img.shields.io/badge/-Whatsapp%20Channel-white?style=for-the-badge&logo=whatsapp&logoColor=black"/>
</a>

<a href="https://chat.whatsapp.com/CG9f0paHJzwDImXiydfuht">
<img alt="WhatsApp Support" src="https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white"/>
</a>

---

Enjoy using **KAVI-X**! 🚀
