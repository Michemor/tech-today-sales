# Technology Today Sales

A Flask web application for managing clients and sites for technology today, styled with Tailwind CSS and using PostgreSQL for data storage.

---

## Features

- Client management
- Client Site management

---

## Tech Stack

- **Backend:** Flask, Flask-SQLAlchemy,
- **Frontend:** Jinja2 templates, CSS, JAVASCRIPT
- **Database:** PostgreSQL

---

## Setup Instructions

### 1. Clone the repository

```sh
git clone <repo-url>
cd tech-today-sales
```

### 2. Install Python dependencies

```sh
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
```

### 3. Install Node.js dependencies (for Tailwind CSS)

```sh
npm install
```

### 4. Configure environment variables

Create a `.env` file in the project root:

```
DATABASE_URL=postgresql://<username>:<password>@localhost:5432/<your_db>
SECRET_KEY=your_secret_key
```

### 5. Initialize the database

Make sure PostgreSQL is running and the database exists.

```sh
flask db upgrade
```

Or, if using `db.create_all()` in your code, just run the app once.

### 6. Build Tailwind CSS

```sh
npm run build:css
```
This will generate `static/css/output.css`.

### 7. Run the application

```sh
python main.py
```

Visit [http://localhost:5000](http://localhost:5000) in your browser.

---

## Usage

- **Login:** Go to `/` and log in with your credentials.
- **Add User:** Go to `/admin` to add a new user (admin only).
- **View Users:** Go to `/users` to see the list of users.
- **Client Section:** `/client` (scaffolded for future client features).

---

## Security Notes

- Passwords are **hashed** using Werkzeug and never stored or displayed in plaintext.
- Do **not** attempt to decrypt passwords; always use hashing and `check_password_hash`.

---

## Development

- Templates are in the `templates/` folder.
- Static files (CSS, JS) are in `static/`.
- Models are in `models/`.
- Forms are in `views/forms.py`.

---

## License

MIT License

---

## Author

Michelle Jemator [https://github.com/Michemor]