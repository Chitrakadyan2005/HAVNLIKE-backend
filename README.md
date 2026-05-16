# ⚙️ HavnLike – Backend (API & Real-Time Services)

HavnLike backend powers the platform by handling **authentication, communities, chats, AI bots, moderation, and real-time communication**.  
It provides secure APIs and socket connections that connect seamlessly with the frontend application.

---

## 🚀 Live API
🔗 `https://girlsgotfeelings-backend.onrender.com`

---

## 📌 Features

✅ User Authentication & Authorization 🔐  
✅ Community Management APIs 🧑‍🤝‍🧑  
✅ Direct Messaging & Public Chat 💬  
✅ AI Bot System for Communities 🤖  
✅ Notification System 🔔  
✅ Content Moderation Engine 🛡️  
✅ Real-time Communication (Sockets) ⚡  
✅ Streaming Support (WebRTC signaling) 🎥  

---

## 🛠️ Tech Stack

- **Runtime:** Node.js  
- **Framework:** Express.js  
- **Database:** MySQL (Neon)  
- **Realtime:** Socket.io  
- **Authentication:** JWT  
- **Language:** JavaScript  
- **Deployment:** Vercel  

---

## 🧠 How It Works

1. Client sends requests via REST APIs.  
2. JWT is used for authentication.  
3. Controllers handle:
   - Users  
   - Communities  
   - Chats  
   - Notifications  
4. Services manage business logic (AI bots, suggestions).  
5. Moderation layer filters unsafe content.  
6. Socket server handles real-time chat & streaming events.  

---

## 🔐 Environment Variables

Create a `.env` file and add the following:

```env
PORT=5000
JWT_SECRET=
FIREBASE_PROJECT_ID=
FIREBASE_PRIVATE_KEY=
FIREBASE_CLIENT_EMAIL=
DB_URL=
CLIENT_URL=
GROQ_API=

```

## 📂 Project Structure

```bash
backend/
│
├── bots/
│   ├── baseBot.js
│   ├── climbBot.js
│   ├── crossedBoundariesBot.js
│   ├── defaultBot.js
│   ├── lifeLately.js
│   ├── mixedSignalsBot.js
│   ├── noFilterBot.js
│   ├── patternBot.js
│   └── secondShiftBot.js
│
├── config/
│   ├── db.js
│   └── firebase.js
│
├── controllers/
│   ├── authController.js
│   ├── botController.js
│   ├── communityController.js
│   ├── dmController.js
│   ├── homeController.js
│   ├── moderationController.js
│   ├── notificationController.js
│   ├── profileController.js
│   ├── searchController.js
│   └── suggestionController.js
│
├── middlewares/
│   └── auth.js
│
├── models/
│   ├── Home.js
│   ├── Notification.js
│   ├── Otp.js
│   ├── Profile.js
│   ├── Search.js
│   ├── User.js
│   ├── community.js
│   └── dm.js
│
├── moderation/
│   ├── moderationRules.js
│   └── userModerationStore.js
│
├── routes/
│   ├── authRoutes.js
│   ├── botRoutes.js
│   ├── communityRoutes.js
│   ├── dmRoutes.js
│   ├── homeRoutes.js
│   ├── moderationRoutes.js
│   ├── notificationRoutes.js
│   ├── profileRoutes.js
│   ├── searchRoutes.js
│   ├── streamRoomRoutes.js
│   └── suggestionRoutes.js
│
├── services/
│   ├── aiService.js
│   └── botServices.js
│
├── socket/
│   ├── chat.js
│   └── stream.js
│
├── utils/
│   ├── chatMemory.js
│
├── server.js
├── package.json
├── package-lock.json
├── vercel.json
└── .gitignore
