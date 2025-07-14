# 📺 ChannelBase

**ChannelBase** is a scalable Node.js API backend for a YouTube-style user system, supporting secure authentication, profile management, media uploads, and watch history — all powered by MongoDB and Cloudinary.

---

## 🚀 Features

- 🔐 JWT-based Auth (Access + Refresh Tokens)
- 🧾 User Registration & Login
- 🍪 Secure Cookie-based Sessions
- 📤 Avatar & Cover Image Upload (Cloudinary)
- 📊 Channel Profile + Watch History
- 🧱 Modular Code Structure (MVC)
- 🔄 Token Refresh System
- ☁️ Multer + Cloudinary Integration

---

## 📁 Directory Overview

project-root/
│
├── controllers/ # Business logic
├── routes/ # Express routes
├── models/ # Mongoose models
├── middlewares/ # Custom middleware (auth, uploads)
├── utils/ # Reusable helpers
├── public/ # Static & temp upload files
├── app.js # Express config
└── index.js # Server entry point

yaml
Copy
Edit

---

## 🛠️ Getting Started

### Prerequisites
- Node.js 18+
- MongoDB URI
- Cloudinary account

### Installation

```bash
git clone https://github.com/yourusername/ChannelBase.git
cd ChannelBase
npm install
cp .env.example .env
# Edit .env with your credentials
npm run dev
🔐 .env Example
env
Copy
Edit
PORT=8000
MONGODB_URI=mongodb+srv://...
DB_NAME=channelbase
ACCESS_TOKEN_SECRET=your_access_secret
REFRESH_TOKEN_SECRET=your_refresh_secret
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEYS=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
CORS_ORIGIN=http://localhost:3000
🧪 API Routes
Auth
POST /api/v1/users/register

POST /api/v1/users/login

POST /api/v1/users/logout

POST /api/v1/users/refresh-token

User
GET /api/v1/users/current-user

PATCH /api/v1/users/update-account

PATCH /api/v1/users/avatar

PATCH /api/v1/users/cover-image

GET /api/v1/users/c/:username

GET /api/v1/users/history

🧱 Tech Stack
Node.js + Express

MongoDB + Mongoose

JWT for Auth

Cloudinary for Image Storage

Multer for File Uploads

Cookie-parser & CORS