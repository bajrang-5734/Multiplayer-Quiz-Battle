# Multiplayer-Quiz-Battle 🧠

**McqBattleApp** is a real-time multiplayer MCQ battle game where users can challenge each other, join private rooms, and play quiz battles with live question delivery and scoring.

---

## 🔧 Tech Stack

This application is built with a modern, full-stack approach, leveraging the following technologies:

* **Frontend**: Next.js, Tailwind CSS, Pusher
* **Backend**: Node.js, Express.js, Prisma, PostgreSQL
* **Real-Time Communication**: Pusher
* **Authentication**: JWT
* **Email Service**: Gmail SMTP
* **Deployment**: Vercel (Frontend), Render (Backend)

---

## 📦 Folder Structure

The project is organized into two primary directories for the frontend and backend services.

```

mcq-battle-app/
├── backend/
└── frontend/

````



## ⚙️ Backend Setup

### Step 1: Navigate to the backend directory

```bash
cd backend
```

### Step 2: Install dependencies

```bash
npm install
```

### Step 3: Create your .env file

Copy the example environment file and fill in the required values.

```bash
cp .env.example .env
```

| Variable | Description |
| :--- | :--- |
| `DATABASE_URL` | Your PostgreSQL connection string. |
| `USER_JWT_SECRET_KEY` | A secret key for JWT signing. |
| `PUSHER_APP_ID` | Your App ID from the Pusher dashboard. |
| `PUSHER_KEY` | Your Pusher key. |
| `PUSHER_SECRET` | Your Pusher secret. |
| `PUSHER_CLUSTER` | Your Pusher cluster (e.g., `ap2`). |
| `OTP_SECRET` | A random string for OTP encryption. |
| `GMAIL_USER` | The Gmail address used to send OTPs. |
| `GMAIL_APP_PASS` | The app-specific password for your Gmail account. |

### Step 4: Run database migrations

Use Prisma to generate the client and apply database migrations.

```bash
npx prisma generate
npx prisma migrate dev
```

### Step 5: Start the backend server

```bash
npm run start
```

The backend server will now be running at `http://localhost:3001` (or your configured port).

-----

## 🌐 Frontend Setup

### Step 1: Navigate to the frontend directory

```bash
cd ../frontend
```

### Step 2: Install dependencies

```bash
npm install
```

### Step 3: Create your .env.local file

Create a new local environment file and add the Pusher credentials.

```bash
touch .env.local
```

| Variable | Description |
| :--- | :--- |
| `NEXT_PUBLIC_PUSHER_KEY` | Same as `PUSHER_KEY` from the backend. |
| `NEXT_PUBLIC_PUSHER_CLUSTER` | Same as `PUSHER_CLUSTER` from the backend. |

### Step 4: Run the frontend dev server

```bash
npm run dev
```

The frontend will be accessible at `http://localhost:3000`.

-----

## ✅ Features

  * **Secure Signup & Login**: Implemented with JWT for secure user authentication.
  * **OTP Verification**: Users can verify their email via OTP.
  * **Real-Time 1v1 Multiplayer**: Fast matchmaking for head-to-head battles.
  * **Live MCQ Questions**: Questions are delivered live with a timer for answers.
  * **Game Stats & Leaderboard**: (Optional) Tracks game stats and displays a leaderboard.
  * **Private Games**: Invite friends to private quiz rooms.

-----

## 📦 Deployment

  * **Frontend**: The frontend is deployed to [Vercel](https://vercel.com/).
  * **Backend**: The backend is deployed on [Render](https://render.com/).

-----
