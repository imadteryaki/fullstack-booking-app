# Full-Stack Booking App ( cloned from Booking.com )

A full-stack hotel booking application with a **React** frontend and a **Node.js / Express** REST API backed by **MongoDB**.

## Features

- Search hotels by destination, date range and number of guests
- Hotel listing and hotel detail pages with room selection and reservation
- User registration and login with **JWT** authentication (HTTP-only cookies)
- Role-based access: user and admin routes are protected on the API
- REST API for hotels, rooms, users and authentication
- Centralised error handling middleware

## Tech Stack

| Frontend | Backend |
|---|---|
| React 18, React Router 6 | Node.js, Express |
| Context API (auth & search state) | MongoDB, Mongoose |
| Axios, react-date-range, date-fns | JWT, bcryptjs, cookie-parser |

## Project Structure

```
├── api/      # Express REST API (routes, controllers, models, middleware)
└── client/   # React frontend
```

## Getting Started

### Prerequisites
- Node.js 18+
- A MongoDB database (local or MongoDB Atlas)

### Backend

```bash
cd api
npm install
cp .env.template .env   # then fill in PORT, MONGO and JWT_SECRET_KEY
npm start
```

### Frontend

```bash
cd client
npm install
npm start
```

The app runs on `http://localhost:3000`.

## API Overview

| Route | Description |
|---|---|
| `POST /api/auth/register` | Create an account |
| `POST /api/auth/login` | Log in and receive a JWT cookie |
| `/api/hotels` | CRUD for hotels (write access: admin) |
| `/api/rooms` | CRUD for rooms (write access: admin) |
| `/api/users` | User management (protected) |

## Author

**Imad Teryaki** – [GitHub](https://github.com/imadteryaki) · [Portfolio](https://imadteryaki.vercel.app)
