# FlaskAuthApp

A secure Flask-based authentication application with user registration and login functionality.

## Features

- User Registration with validation
- Secure Login system
- Password hashing with bcrypt
- User Dashboard
- SQLite Database
- Session management

## Requirements

- Python 3.8+
- Flask 3.1.2
- Flask-SQLAlchemy 3.1.1
- bcrypt
- gunicorn (for production)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/VivekDhakrey/Authapp.git
cd Authapp
```

2. Create a virtual environment:
```bash
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

## Running the Application

### Local Development
```bash
python app.py
```
The app will run on `http://localhost:5000`

### Production (with Gunicorn)
```bash
gunicorn app:app
```

## API Routes

- `/` - Home page
- `/register` - User registration (GET, POST)
- `/login` - User login (GET, POST)
- `/dashboard` - User dashboard (requires login)
- `/logout` - User logout

## Validation Requirements

### Registration Validation
- Name: Required, non-empty
- Email: Required, non-empty, unique
- Password: Required, minimum 6 characters

## Database

The application uses SQLite with the following User model:
- `id` - Primary key
- `name` - User name
- `email` - User email (unique)
- `password` - Hashed password (bcrypt)

## Security

- Passwords are hashed using bcrypt
- Session management for user authentication
- Server-side validation on all inputs

## License

MIT License

## Author

Vivek Dhakrey
