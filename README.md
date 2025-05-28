# 🤖 Gemini AI Chatbot

A ChatGPT-style AI chatbot built using the **MERN stack**, powered by **Google's Gemini API** for intelligent conversations. User authentication is handled using **Clerk**, making it secure and easy to manage users.

---

## 🚀 Features

- 🌐 Full-stack MERN (MongoDB, Express, React, Node.js)
- 🔑 Secure user authentication with Clerk
- 🧠 Conversational AI using Google's Gemini API
- ⚡ Real-time chat interface
- 🖼️ Optional support for multimodal input (text + image, if supported by the model)
- 🔧 Scalable, modular architecture


---

## 🔐 Authentication

This app uses [Clerk](https://clerk.dev) for:
- Sign up / Sign in / User profile
- Session management
- JWT-based backend auth

Frontend is integrated via Clerk’s React SDK, and the backend validates users using Clerk’s middleware.

---

## 🧠 Gemini API Integration

We use the Gemini API from Google AI (Gemini Pro or 1.5) to power the conversation. The API is called from the backend to ensure security and manage rate limits.

🔧 **Backend**: Requests are routed through `/api/chat` where user messages are sent to Gemini and responses are returned.



## 🧪 .env Setup

### Backend (`/backend`)

```
PORT=5001
MONGO_URI=your_mongo_uri
GEMINI_API_KEY=your_gemini_api_key
CLERK_SECRET_KEY=your_clerk_secret_key
```

### Frontend (`/frontend`)

```
VITE_CLERK_PUBLISHABLE_KEY=your_clerk_frontend_key
VITE_API_BASE_URL=http://localhost:5000

```