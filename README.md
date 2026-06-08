# QuizNova

## Overview

**QuizNova** is an interactive, full-stack quiz platform designed to provide a seamless experience for creating and taking assessments. The platform focuses on high-speed performance and user engagement, allowing users to test their knowledge across various topics with real-time feedback.

The system utilizes a modern web stack to ensure secure user authentication, efficient data management, and a responsive interface suitable for both students and educators.

### Key Capabilities

* **Interactive Quiz Interface**
* **Dynamic Question Management**
* **User Authentication & Authorization**
* **Real-Time Score Calculation**
* **Category-based Navigation**
* **Result Tracking**

---

## Problem Statement

Traditional online quiz platforms often suffer from cluttered interfaces, lack of secure progress tracking, or rigid question formats.

**QuizNova** addresses these challenges by:

* Providing a clean, distraction-free **UI/UX**.
* Implementing **secure session management** for users.
* Offering **scalable data storage** for an ever-growing library of questions.
* Ensuring **low-latency responses** during active quiz sessions.

---

## Features

### Dynamic Quiz Engine

Take quizzes across multiple categories with a smooth, responsive flow that adapts to different devices.

### Secure User System

Features robust Signup and Login functionalities using encrypted credentials to keep user data and history safe.

### Real-Time Evaluation

Instantly calculates scores upon submission, providing immediate feedback to the learner.

### Category Explorer

Easily browse through different subjects or difficulty levels to find the perfect challenge.

### History & Progress

(If applicable) Track past performance to monitor learning progress over time.

---

## Tech Stack

### Frontend

* **HTML5**
* **CSS3**
* **JavaScript (ES6+)**

### Backend

* **Node.js**
* **Express.js**
* **JWT (JSON Web Tokens)** for secure authentication
* **Bcrypt** for password hashing

### Database

* **MySQL** (Relational database management for users and quizzes)

---

## System Architecture

```text
User
  │
  ▼
Frontend (HTML/CSS/JS)
  │
  ▼
Express Server (API Layer)
  │
  ├── Auth Middleware (JWT/Bcrypt)
  └── Quiz Logic Router
  │
  ▼
MySQL Database (Users, Questions, Scores)
  │
  ▼
Express Server
  │
  ▼
Frontend
  │
  ▼
User Receives Results/Feedback

```

---

## Project Structure

```text
QuizNova
├── frontend
│   ├── index.html
│   ├── login.html
│   ├── signup.html
│   ├── quiz.html
│   ├── result.html
│   ├── css/
│   │   └── style.css
│   └── js/
│       ├── auth.js
│       └── quiz.js
│
├── backend
│   ├── .env
│   ├── config/
│   │   └── db.js
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   │   ├── authRoutes.js
│   │   └── quizRoutes.js
│   ├── server.js
│   └── package.json
└── database
    └── schema.sql

```

---

## Installation

### Clone Repository

```bash
git clone https://github.com/divyasanthoshini17/quiz-nova.git
cd quiz-nova

```

### Install Backend Dependencies

```bash
cd backend
npm install

```

### Setup Database

1. Open your MySQL client (XAMPP/MySQL Workbench).
2. Create a new database named `quiz_nova`.
3. Import the `schema.sql` (or equivalent) provided in the database folder.

### Configure Environment

Create a `.env` file in the `backend` folder:

```env
PORT=5000
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_password
JWT_SECRET=your_jwt_secret

```

### Run the Project

1. **Start Backend:**
```bash
node server.js

```


2. **Start Frontend:**
```bash
npm run dev

```
---

## Future Improvements

* **Timer Integration:** Add a countdown for each quiz to increase difficulty.
* **Leaderboards:** Global ranking system to compete with other users.
* **Admin Dashboard:** Interface for teachers to add/edit questions without touching the database.
* **Multiplayer Mode:** Real-time quiz battles using WebSockets.