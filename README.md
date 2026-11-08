# DevAsk — Community Q&A Discussion Platform

**DevAsk** is a full-stack community question-and-answer platform built with the PERN stack (PostgreSQL, Express, React, Node.js). It enables developers and community members to post technical questions, contribute answers, and browse indexed discussions in real time.

---

## Agile Workflow, Pull Requests & Original Repositories

This monorepo consolidates the frontend and backend codebases (preserving the full commit history) originally developed during the **NYC Tech Talent Pipeline (TTP)** Software Engineering Residency.

To view feature branches, peer code reviews, and merged **Pull Requests**, visit the original repositories:
* **Frontend Repository & Pull Requests:** [TTP-CAPSTONE-2/QA-Frontend](https://github.com/TTP-CAPSTONE-2/QA-Frontend) | [View Closed PRs](https://github.com/TTP-CAPSTONE-2/QA-Frontend/pulls?q=is%3Apr+is%3Aclosed)
* **Backend Repository & Pull Requests:** [TTP-CAPSTONE-2/QA-Backend](https://github.com/TTP-CAPSTONE-2/QA-Backend) | [View Closed PRs](https://github.com/TTP-CAPSTONE-2/QA-Backend/pulls?q=is%3Apr+is%3Aclosed)

---

## Key Features

* **Relational Q&A Architecture:** Designed one-to-many PostgreSQL schemas via Sequelize ORM to index and query 400+ community questions and 1,000+ discussion answers with fast relational lookups.
* **Session-Based Authentication & Route Protection:** Enforces strict account ownership across post creation, editing, and deletion workflows using custom authentication middleware and protected Express API routes.
* **Reactive Discussion Threads:** Connects React question-detail and answer-submission forms directly to backend REST endpoints with optimistic/state-driven updates so newly submitted answers render immediately without page reloads.

---

## Tech Stack

* **Frontend (`/client`):** React, React Router, CSS3 / Tailwind CSS, Axios
* **Backend (`/server`):** Node.js, Express.js, RESTful APIs, Session Authentication
* **Database (`/server`):** PostgreSQL, Sequelize ORM

---

## Repository Structure

    DevAsk/
    ├── client/          # React frontend (merged from TTP-CAPSTONE-2/QA-Frontend)
    └── server/          # Express & PostgreSQL backend (merged from TTP-CAPSTONE-2/QA-Backend)

---

## Local Setup & Installation

### 1. Clone the repository

    git clone https://github.com/YeffryF/DevAsk.git
    cd DevAsk

### 2. Backend Setup (`/server`)

    cd server
    npm install

Create a `.env` file in the `server/` directory with your PostgreSQL database credentials:

    PORT=8080
    DATABASE_URL=postgresql://localhost:5432/devask_db
    SESSION_SECRET=your_session_secret

Start the backend server:

    npm start

### 3. Frontend Setup (`/client`)

Open a new terminal window:

    cd client
    npm install
    npm run dev
