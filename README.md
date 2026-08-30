# Contact Manager Frontend

This is the React + Vite frontend for a simple contact management app. It allows users to view, create, update, and delete contacts by talking to the Flask backend API.

## Features

- View all contacts in a table
- Create a new contact
- Update an existing contact
- Delete a contact
- Modal-based form for create/edit flows
- Live refresh after create, update, or delete actions

## Tech Stack

- React
- Vite
- JavaScript
- Fetch API for backend communication

## Project Structure

```bash
frontend/
├── public/
├── src/
│   ├── App.jsx
│   ├── ContactForm.jsx
│   ├── ContactList.jsx
│   ├── App.css
│   ├── index.css
│   └── main.jsx
├── index.html
├── package.json
├── vite.config.js
├── eslint.config.js
└── README.md
```

## Prerequisites

Before running the frontend, make sure:

- Node.js is installed
- The backend is running on `http://127.0.0.1:5000`
- Dependencies are installed using `npm install`

## Installation

From the frontend folder:

```bash
npm install
```

## Run the app

```bash
npm run dev
```

This starts the Vite development server, usually at:

```bash
http://localhost:5173
```

## Backend API Expectations

The frontend expects the backend to expose these routes:

- `GET /contacts`
- `POST /create_contact`
- `PATCH /update_contact/:id`
- `DELETE /delete_contact/:id`

The app sends JSON payloads like:

```json
{
  "firstName": "John",
  "lastName": "Doe",
  "email": "john@example.com"
}
```

## Scripts

```bash
npm run dev     # start development server
npm run build   # build production bundle
npm run preview # preview production build
npm run lint    # run ESLint checks
```

## Notes

- The frontend is configured for local development and expects the Flask backend to be running separately.
- CORS must be enabled in the backend so browser requests succeed.
- If the backend URL changes, update the fetch calls in the React components.

## License

This project is for local learning/demo purposes.
