# ExamFlow — Online Examination System

A complete starter project for an online examination portal built with **Node.js, Express, HTML, CSS, and vanilla JavaScript**. It stores data in a local JSON file, so a separate database is not required to run the demo.

## Features

- Student registration and login (passwords hashed with bcrypt)
- Administrator and student roles
- Administrator dashboard with student, exam, submission, and average-score statistics
- Create multiple-choice examinations with custom questions and answer keys
- Publish/deactivate exams
- Exam timer with automatic submission when time runs out
- One submission per student per exam
- Instant scoring, percentage, and answer review
- Searchable exam library and result history
- Responsive dashboard UI
- Seeded sample JavaScript exam

## Requirements

- Node.js 18 or newer
- npm

## Run on Windows

1. Extract `online-examination-system.zip`.
2. Open Command Prompt in the extracted `online-examination-system` folder.
3. Install packages:

   ```bat
   npm install
   ```

4. Start the application:

   ```bat
   npm start
   ```

5. Open `http://localhost:3000` in your browser.

> Run `npm install` in the folder containing `package.json`. If npm says it cannot find `package.json`, you are in the wrong folder.

## Demo administrator login

- **Email:** `admin@exam.com`
- **Password:** `Admin@12345`

Students can create accounts using the **Create account** tab. Use a different email for each account.

## Where data is stored

The first launch creates `data/db.json` and seeds the administrator and a sample exam. Users, exams, and attempts are saved there. Back up this file if you need to preserve local demo data. To reset demo data, stop the server and delete `data/db.json`; it will be recreated on the next launch.

## Important before public deployment

This is a learning/demo project, not a production-hardened exam platform. Before deploying publicly:
- Set a strong random `SESSION_SECRET` environment variable.
- Use HTTPS and secure cookies.
- Replace Express's default in-memory session store with a persistent session store.
- Use a database such as PostgreSQL or MySQL for concurrent users and durable data.
- Add rate limiting, CSRF protection, input validation, audit logs, backups, and appropriate privacy controls.
- The timer is enforced in the browser for user experience; a production version should also enforce exam deadlines on the server.
- Do not use the seeded demo administrator password on a public deployment.

## Project structure

```text
online-examination-system/
├── data/
│   └── .gitkeep
├── public/
│   ├── app.js
│   ├── index.html
│   └── style.css
├── .gitignore
├── package.json
├── README.md
└── server.js
```
