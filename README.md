# MERNFileSharer

A full-stack file sharing web app built with Node.js, Express, MongoDB, and EJS. Upload any file and share it via a unique link, with optional password protection.

## Features

- Upload files of any type via drag-and-drop or file picker
- Generate a unique shareable download link per file
- Optional password protection using bcrypt hashing
- Download counter tracks how many times a file has been accessed
- Server-side rendered views with EJS templates

## Tech Stack

- **Backend** — Node.js, Express
- **Database** — MongoDB (via Mongoose)
- **Templating** — EJS
- **File handling** — Multer
- **Auth** — bcrypt
- **Dev** — Nodemon

## Setup

```bash
# 1. Clone the repo
git clone https://github.com/sai4621/MERNFileSharer.git
cd MERNFileSharer

# 2. Install dependencies
npm install

# 3. Create a .env file
echo "DATABASE_URL=mongodb://localhost:27017/filesharer" > .env
echo "PORT=3000" >> .env

# 4. Start the dev server
npm run devStart
```

Then open `http://localhost:3000` in your browser.

## Usage

1. Visit the home page and select a file to upload.
2. Optionally enter a password to protect the download.
3. Copy the generated link and share it.
4. Recipients visit the link; if password-protected, they are prompted before downloading.

## API Routes

| Method | Path | Description |
|---|---|---|
| GET | `/` | Upload form |
| POST | `/upload` | Handle file upload |
| GET/POST | `/file/:id` | Download file (POST for password verification) |
