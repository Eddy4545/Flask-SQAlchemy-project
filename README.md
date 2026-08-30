# Contact Manager Project

This project is a simple full-stack contact management app built with a Flask backend and a React frontend. It allows a user to create, view, update, and delete contacts through a browser interface while storing the records in a SQLite database.

## Project Overview

The application is split into two main parts:

- Backend: Python + Flask + SQLAlchemy
- Frontend: React + Vite

Together, they form a basic CRUD application where the frontend sends HTTP requests to the backend API and the backend persists the data in SQLite.


### Frontend Responsibilities

- Render the contact list
- Show the create/edit form in a modal
- Send requests to the backend API
- Refresh data after create, update, and delete actions

### Frontend Setup

From the `frontend` folder:

```bash
npm install
npm run dev
```

This usually runs the app at:

```bash
http://localhost:5173
```

### Backend Responsibilities

- Expose API routes for contact operations
- Validate incoming request data
- Store and retrieve contact records from SQLite
- Return JSON responses to the frontend

### Backend Routes

- `GET /contacts` — fetch all contacts
- `POST /create_contact` — create a contact
- `PATCH /update_contact/<id>` — update a contact
- `DELETE /delete_contact/<id>` — delete a contact

### Example Payload

```json
{
  "firstName": "John",
  "lastName": "Doe",
  "email": "john@example.com"
}
```

### Backend Setup

From the project root or the `Backend` folder, install the Python dependencies and run the app:

```bash
pip install flask flask_sqlalchemy flask_cors
python main.py
```

The backend runs on:

```bash
http://127.0.0.1:5000
```

## Notes

- The frontend and backend are meant to run at the same time.
- The backend enables CORS so the browser can call the API from the React app.
- The database used is SQLite, which is stored locally in the project.

## Intent

This project is intended for learning and local development purposes.

