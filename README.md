# Task-week-11
# 📝 Full Stack Blogging Platform

A complete full-stack blogging application built with **React**, **Node.js**, and **MongoDB**. This project demonstrates modern web development practices including authentication, protected routes, global state management, and RESTful API integration.

---

## 🚀 Features

### 🔐 Authentication & Security

* User registration and login
* JWT-based authentication (access + refresh tokens)
* Protected routes for authenticated users
* Secure password hashing

### 📝 Blog Functionality

* Create, read, update, and delete (CRUD) blog posts
* Rich text editor for writing posts
* View all posts and individual post pages

### 💬 Social Features

* Nested comment system
* Like/unlike posts
* User profiles and settings

### ⚙️ System Features

* Global state management using Context API
* Error handling and loading states
* Responsive UI

---

## 🛠️ Tech Stack

### Frontend

* React
* Context API
* Axios
* React Router

### Backend

* Node.js
* Express.js
* MongoDB (Mongoose)
* JSON Web Tokens (JWT)

---

## 📁 Project Structure

```
root/
│
├── client/               # React frontend
│   ├── src/
│   ├── components/
│   ├── pages/
│   └── context/
│
├── server/               # Node.js backend
│   ├── controllers/
│   ├── routes/
│   ├── models/
│   ├── middleware/
│   └── config/
│
└── README.md
```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the repository

```bash
git clone https://github.com/your-username/blogging-platform.git
cd blogging-platform
```

### 2️⃣ Setup Backend

```bash
cd server
npm install
```

Create a `.env` file:

```
PORT=5000
MONGO_URI=your_mongodb_connection
JWT_SECRET=your_secret_key
JWT_REFRESH_SECRET=your_refresh_secret
```

Run backend:

```bash
npm run dev
```

---

### 3️⃣ Setup Frontend

```bash
cd client
npm install
npm start
```

---

## 🔐 Authentication Flow

1. User registers or logs in
2. Server returns:

   * Access Token (short-lived)
   * Refresh Token (long-lived)
3. Access token used for API requests
4. Refresh token used to generate new access tokens

---

## 🔒 Protected Routes

* Only authenticated users can:

  * Create posts
  * Edit/delete their posts
  * Comment on posts
* Unauthorized users are redirected to login

---

## 🌐 API Endpoints (Sample)

### Auth

```
POST /api/auth/register
POST /api/auth/login
POST /api/auth/refresh
```

### Posts

```
GET    /api/posts
POST   /api/posts
PUT    /api/posts/:id
DELETE /api/posts/:id
```

### Comments

```
POST   /api/comments
GET    /api/comments/:postId
```

---

## 🧠 State Management

* Implemented using **React Context API**
* Stores:

  * User authentication state
  * Global loading and error states

---

## ⚠️ Error Handling

* Centralized error handling in backend
* User-friendly error messages in frontend
* Loading indicators for async actions

---

## 📅 Development Timeline

| Day | Task                                        |
| --- | ------------------------------------------- |
| 1-2 | Project setup & architecture                |
| 3   | Authentication system                       |
| 4   | Blog CRUD features                          |
| 5   | UI development                              |
| 6   | Advanced features (comments, likes, search) |
| 7   | Testing, styling & deployment               |

---

## 🚀 Deployment

### Frontend

* Vercel / Netlify

### Backend

* Render / Railway / AWS

### Database

* MongoDB Atlas

---

## 🧪 Future Improvements

* Add image uploads
* Implement notifications
* Add markdown support
* Improve SEO
* Add unit & integration tests
