💬 Full Stack Real-Time Chat Application
📘 Overview

This project is a real-time chat application built using the MERN stack (MongoDB, Express.js, React.js, Node.js) with Socket.io for live messaging and user presence. It supports private and group chats, authentication, online status, and a clean, responsive UI designed with Tailwind CSS.

The app allows users to:

Register and log in securely.

Send and receive instant messages.

Create and manage group chats.

View the latest messages in chat previews.

See which users are currently online.

🧠 Project Objectives

This project was developed to demonstrate key TVET Level 6 Computer Programming competencies, including:

Full-stack web application development.

REST API design and documentation.

Database modeling using MongoDB.

Real-time communication using WebSockets.

Frontend state management and component design.

Deployment and cloud hosting on Render (backend) and Vercel (frontend).

✨ Features
👤 Authentication

Register, login, and logout using JWT tokens.

Authenticated API routes with token validation.

Secure password storage using bcrypt.

💬 Messaging

Instant text-based communication.

Private 1-on-1 chats.

Group chats with multiple members.

Last message preview in chat list.

👥 Groups

Create new groups.

Add or remove members (admin only).

Manage group names and participants.

🟢 Real-Time Functionality

Live message updates via Socket.io.

Online/offline user status indicators.

⚙️ Other Features

Responsive UI built with Tailwind CSS.

Backend API and frontend integrated seamlessly.

Deployed on cloud services (Render + Vercel).

🧩 Technologies Used
Category	Technology
Frontend	React.js, Vite, Tailwind CSS, Axios, React Router
Backend	Node.js, Express.js
Database	MongoDB, Mongoose
Realtime	Socket.io
Authentication	JWT (JSON Web Token)
Hosting	Render (Backend), Vercel (Frontend)
🏗️ System Architecture

Frontend (React) → communicates via Axios → Backend API (Express) → stores data in MongoDB → syncs live events using Socket.io.

React (Client)
    │
    ├── Axios (HTTP)
    │
    ▼
Express.js (Server)
    │
    ├── Mongoose ORM
    ▼
MongoDB (Database)

🗂️ Folder Structure
Frontend (/client)
client/
 ├── src/
 │   ├── api/
 │   ├── components/
 │   ├── context/
 │   ├── pages/
 │   ├── socket/
 │   ├── App.jsx
 │   └── main.jsx
 ├── package.json
 └── vite.config.js

Backend (/server)
server/
 ├── controllers/
 ├── middleware/
 ├── models/
 ├── routes/
 ├── config/
 ├── server.js
 └── package.json

🧾 Database Design
Collections

User

username

email

password (hashed)

avatar (optional)

Chat

chatName

isGroup (boolean)

users (array of user IDs)

latestMessage (reference)

groupAdmin (if group)

Message

sender (user)

content (text)

chat (reference)

readBy (array of user IDs)

timestamps

🔌 API Endpoints
Method	Endpoint	Description
POST	/api/auth/register	Register a new user
POST	/api/auth/login	Log in existing user
GET	/api/users	Fetch all users
GET	/api/chat	Fetch user’s chats
GET	/api/chat/private/:userId	Access or create private chat
POST	/api/chat/group	Create group chat
PUT	/api/chat/:chatId/add	Add user(s) to group
PUT	/api/chat/:chatId/remove	Remove user from group
GET	/api/messages/:chatId	Get chat messages
POST	/api/messages	Send a new message
⚙️ Setup & Installation
1️⃣ Clone the Repository
git clone https://github.com/your-username/chat-app.git
cd chat-app

2️⃣ Backend Setup
cd server
npm install


Create a .env file:

PORT=4000
MONGO_URI=your_mongodb_connection
JWT_SECRET=your_jwt_secret
CLIENT_URL=https://chat-app-red-nu-48.vercel.app


Run server:

npm start


Server will start at: http://localhost:4000

3️⃣ Frontend Setup
cd client
npm install
npm run dev


Visit: http://localhost:5173

🌍 Deployment
🖥️ Backend (Render)

Push your code to GitHub.

Create a Render Web Service.

Connect repository → Select branch → Add environment variables.

Deploy 🚀

💻 Frontend (Vercel)

Push frontend to GitHub.

Create a Vercel Project.

Add vercel.json to root:

{
  "version": 2,
  "builds": [{ "src": "vite.config.js", "use": "@vercel/static-build", "config": { "distDir": "dist" } }],
  "routes": [{ "src": "/(.*)", "dest": "/index.html" }]
}


Deploy 🎉

🧪 Testing

Unit tests can be added using Jest or Mocha.

Manual testing performed for:

Login & Register

Real-time chat

Group creation

Socket.io live updates

📸 Screenshots

(Attach screenshots here once ready)

✅ Login Page

✅ Chat Interface

✅ Group Creation Modal

✅ Online/Offline Indicators

👨‍💻 Developer

Name: Duncan Nyaga Maina
Email: dun.can.duntez@gmail.com

LinkedIn: linkedin.com/in/duncan-maina58

Location: Ithanga, Murang’a, Kenya

🏁 Conclusion

This project demonstrates the implementation of a complete real-time communication system integrating frontend and backend technologies. It aligns with TVET Level 6 practical assessment requirements, showcasing expertise in:

Full-stack application development

API and database integration

Real-time systems using Socket.io

Modern frontend design and deployment
