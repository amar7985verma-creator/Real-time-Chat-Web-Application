# Real-time-Chat-Web-Application
Real Time Chat Web Application

A real-time chat web application built with React (Frontend) and Node.js + Express + MongoDB (Backend). The app supports direct messages (DMs), group chats, authentication, and user management.

Features Authentication

Signup & Login with email and password.

JWT-based token authentication.

localStorage stores token, userId, userName, userEmail.

Direct Messaging (DM)

Send messages to other users.

Messages display sender and receiver names.

Messages fetched automatically on page load.

Group Chat

Create groups and add members.

Send messages to groups.

Messages display sender name.

Search Users

Search for users by username.

Click to start a DM.

Real-time UI (Frontend)

Messages appear automatically on sending.

Conditional rendering based on logged-in status.

Logout clears localStorage and redirects to login.

Tech Stack

Frontend: React, React Router, CSS, React Icons

Backend: Node.js, Express, MongoDB, Mongoose, JWT, bcrypt

Tools: Postman (API testing), VS Code

Backend Setup

Clone the repo and go to backend/.

Install dependencies:

npm install

Create a .env file with:

PORT=5000 MONGO_URI=<your_mongodb_connection_string> JWT_SECRET=<your_jwt_secret>

Start the server:

npm run dev

Server runs at http://localhost:5000.

Frontend Setup

Go to frontend/.

Install dependencies:

npm install

Start the React app:

npm start

App runs at http://localhost:3000.

API Endpoints Auth

POST /api/auth/signup – Signup new user.

POST /api/auth/login – Login existing user.

GET /api/auth/all-users – Fetch all users (token required).

Messages

POST /api/messages/dm/:receiverId – Send direct message.

GET /api/messages/dm/:userId – Get DMs between users.

POST /api/messages/group – Send group message.

GET /api/messages/group/:groupId – Get all group messages.

Groups

POST /api/groups/create – Create group (with members).

GET /api/groups/:userId – Fetch groups user belongs to.

Usage

Signup a new user or login.

Search for other users to chat.

Click on a user to open Text Chat.

Send messages and they will appear instantly.

Create groups via GroupCreate page.

Logout using the red button – clears session.

Notes

For testing DMs, use different browsers or incognito tabs to simulate multiple users.

Make sure MongoDB Atlas or local MongoDB is running.

All passwords are hashed with bcrypt.

Tokens expire in 1 day (can be changed in backend JWT settings).

Future Enhancements

WebSocket / Socket.io for real-time updates without page refresh.

Typing indicators and read receipts.

File/image sharing in chats.

Push notifications.

Author Amar Verma
