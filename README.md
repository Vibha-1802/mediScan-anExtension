# 🩺 MediScan — Medicine Authentication via Secure QR Codes

**MediScan** is a full-stack web application that verifies medicines via secure UUID-based QR codes. It enables instant validation of authenticity, expiry checks, and simple admin QR generation.

---

## ⚡ Quick Links

* **Demo video:** `docs/prototype.mp4`

---

## 📌 Table of contents

* [Overview](#overview)
* [Features](#features)
* [Tech Stack](#tech-stack)
* [Prerequisites](#prerequisites)
* [Installation & Setup (Bash)](#installation--setup-bash)
* [Environment (.env) Example](#environment-env-example)

---

## Overview

MediScan lets users verify medicines by scanning/uploading a QR code. Each QR encodes a UUID stored in a secure PostgreSQL database. Admins generate QR codes for batches and manage medicine metadata from a protected portal.

---

## Features

* Secure QR verification (UUIDs)
* Detect valid / expired / fake medicines
* Admin dashboard: add medicines, generate QR codes
* Frontend QR decoding using `jsQR` (upload or camera)
* Backend: Node.js + Express + PostgreSQL
* Password hashing (bcrypt) and environment-based config

---

## Tech Stack

* **Frontend:** React, jsQR, Axios
* **Backend:** Node.js, Express, bcrypt, dotenv
* **Database:** PostgreSQL (UUIDs),50 most commonly used medicines csv and the tablets database
* **QR Generation:** goQR or `api.qrserver.com`

---

## Prerequisites

Install these before starting:

```bash
node -v       
npm -v
psql --version  

```

---

## Installation & Setup (Bash)

### 1. Clone repo

```bash
git clone https://github.com/Vibha-1802/mediScan-anExtension.git
cd mediScan-anExtenstion
```

### 2. Backend setup

```bash
cd backend
npm install
node index.js
```

### 3. Frontend setup

```bash
cd frontend
npm install
npm run dev
```

---

## Environment Variables(.env) 

### `backend/.env`

```env
PG_USER= "postgres"
PG_HOST= "localhost"
PG_DATABASE= "postgres"
PG_PASSWORD="yourpassword"
PG_PORT= 5432
CORS_ORIGIN_URL=http://localhost:5173
```
---
