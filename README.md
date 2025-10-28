# 💬 Real-Time Chat Application

A **full-stack real-time chat application** built with the **MERN (MongoDB, Express, React, Node.js)** stack, featuring **user authentication**, **real-time messaging with Socket.io**, and **group chat functionality**.

---

## 🚀 Live Links

- **Frontend (Vercel):** [https://chat-app-red-nu-48.vercel.app](https://chat-app-red-nu-48.vercel.app)  
- **Backend (Render):** [https://chatapp-ktbk.onrender.com](https://chatapp-ktbk.onrender.com)

---

## 📖 Table of Contents
1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Tech Stack](#tech-stack)
4. [System Architecture](#system-architecture)
5. [Setup Instructions](#setup-instructions)
6. [Environment Variables](#environment-variables)
7. [API Endpoints](#api-endpoints)
8. [Socket.io Events](#socketio-events)
9. [Folder Structure](#folder-structure)
10. [Deployment](#deployment)
11. [Contributors](#contributors)
12. [License](#license)

---

## 🧩 Project Overview

This project is a **real-time chat system** that allows users to:
- Create accounts and log in securely using JWT authentication.
- Chat one-on-one or in groups.
- See **online/offline status**, **typing indicators**, and **read receipts**.
- Manage contacts and start new conversations instantly.

---

## 🌟 Features

✅ User registration and login (JWT Authentication)  
✅ Real-time one-on-one messaging via Socket.io  
✅ Create and manage group chats  
✅ Typing and online status indicators  
✅ Read and delivered message ticks  
✅ Responsive UI styled like WhatsApp  
✅ Secure password hashing with bcrypt  
✅ Persistent sessions using localStorage  
✅ RESTful API backend  

---

## 🛠 Tech Stack

### **Frontend**
- React.js (Vite)
- Tailwind CSS
- Axios
- React Router DOM
- Socket.io-client

### **Backend**
- Node.js
- Express.js
- MongoDB & Mongoose
- Socket.io
- JWT for authentication
- CORS for cross-origin requests

---

## 🧱 System Architecture

Frontend (React) <-----> Backend (Express API)
↑ ↓
Socket.io Client <-----> Socket.io Server
↑ ↓
MongoDB Database <-----> Mongoose Models

yaml
Copy code

---

## ⚙️ Setup Instructions

### 1️⃣ Clone the repository

```bash
git clone https://github.com/yourusername/chat-app.git
cd chat-app
2️⃣ Setup backend
bash
Copy code
cd server
npm install
3️⃣ Setup frontend
bash
Copy code
cd client
npm install
4️⃣ Run the development servers
Start backend

bash
Copy code
npm run dev
Start frontend

bash
Copy code
npm run dev
🔐 Environment Variables
Create a .env file in the server directory with the following:

env
Copy code
PORT=4000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
CLIENT_URL=https://chat-app-red-nu-48.vercel.app
🔗 API Endpoints
Method	Endpoint	Description
POST	/api/auth/register	Register a new user
POST	/api/auth/login	Login user
GET	/api/users	Fetch all users
GET	/api/chat	Get all chats for user
POST	/api/chat	Create or fetch one-on-one chat
POST	/api/chat/group	Create new group chat
PUT	/api/chat/rename	Rename group chat
PUT	/api/chat/add	Add member to group
PUT	/api/chat/remove	Remove member from group
GET	/api/message/:chatId	Get all messages for a chat
POST	/api/message	Send a new message

💬 Socket.io Events
Event	Description
setup	Initialize socket connection
join chat	Join a chat room
new message	Send/receive a message in real-time
typing	Show typing indicator
stop typing	Remove typing indicator
online / offline	Update user online status
delivered / read	Update message delivery status

🗂 Folder Structure
bash
Copy code
chat-app/
│
├── client/                # React frontend
│   ├── src/
│   │   ├── components/    # UI components
│   │   ├── pages/         # App pages (Login, Chat, etc.)
│   │   ├── context/       # Auth context
│   │   ├── api/           # Axios setup
│   │   └── App.jsx
│   └── package.json
│
├── server/                # Node.js backend
│   ├── controllers/       # Route controllers
│   ├── models/            # MongoDB models
│   ├── routes/            # API routes
│   ├── server.js          # Entry point
│   ├── socket.js          # Socket.io configuration
│   └── package.json
│
└── README.md
🌍 Deployment
Frontend
Deployed using Vercel

bash
Copy code
npm run build
Deploy via https://vercel.com

Backend
Deployed using Render

bash
Copy code
git push origin main
Configure:

Root directory: /server

Start command: npm start

Environment variables: same as .env

👨‍💻 Contributors
Name	Role
Duncan Nyaga Maina	Developer / Designer

📜 License
This project is licensed under the MIT License – feel free to use and modify.

🧠 Acknowledgments
Socket.io Documentation

Render Deployment Guide

Vercel Deployment Guide

MongoDB Atlas
