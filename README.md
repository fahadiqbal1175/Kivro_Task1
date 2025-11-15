# Contact Form Example

A simple full-stack example: a static HTML contact form that sends JSON to a Node.js + Express backend. The server logs submitted form data to the console.

---

## Features

* Simple frontend: `public/index.html` containing a form (name, email, message).
* Backend: `index.js` — Node.js + Express server with a POST route at `/contact`.
* Server logs each submission to the console (as required).
* Serves the frontend from the same Express app to avoid CORS issues.

---

## Prerequisites

* Node.js (LTS) and npm installed. Verify with:

  ```bash
  node -v
  npm -v
  ```
* Git installed if you plan to push the project to GitHub.

---

## Project structure

```
contact-form-example/
├─ public/
│  └─ index.html
├─ index.js
├─ package.json
├─ README.md
└─ .gitignore
```

---

## Install & Run (local)

1. Clone the repo or copy the project folder to your machine.
2. Install dependencies:

   ```bash
   npm install
   ```
3. Start the server:

   ```bash
   npm start
   # or for development with auto-reload (if nodemon is installed):
   npm run dev
   ```
4. Open your browser at `http://localhost:3000` and submit the form.
5. Check your terminal/console — you should see the submitted data logged.

---

## How it works (brief)

* The frontend uses JavaScript's `fetch()` to send a POST request to `/contact` with a JSON body.
* Express's `express.json()` middleware parses the incoming JSON and `req.body` contains the form values.
* The server side validates the presence of required fields and logs them to the console.

---

## Example server console output

```
New contact form submission:
Name: Alice
Email: alice@example.com
Message: Hello there!
```

---

## Editing & Development tips

* Edit `public/index.html` to change the form or add styles. Refresh in the browser after changes.
* Edit `index.js` to expand validation, save submissions to a file or database, or add new routes.
* Use `nodemon` (install globally or as a dev dependency) for automatic server restarts while developing:

  ```bash
  npm install --save-dev nodemon
  npm run dev
  ```

---

## Git & GitHub (recommended workflow)

1. Initialize git (if not already):

   ```bash
   git init
   ```
2. Add files and commit:

   ```bash
   git add .
   git commit -m "Initial commit: contact form + express server"
   ```
3. Create a GitHub repo, then link and push:

   ```bash
   git remote add origin https://github.com/<USERNAME>/<REPO>.git
   git branch -M main
   git push -u origin main
   ```

---

## Possible Next Steps / Improvements

* Persist submissions to a database (SQLite, MongoDB, PostgreSQL).
* Add server-side email notifications using Nodemailer.
* Add basic validation and sanitization to avoid malformed input.
* Add a simple admin page to view submissions (protect with auth).
* Deploy to a hosting provider (Render, Vercel, Heroku, etc.).

---

## License

This example is provided under the MIT License. Use it freely for learning and projects.

---

## Author

fahadiqbal1175

*Created for a beginner-friendly task showing a frontend and backend connection.*
