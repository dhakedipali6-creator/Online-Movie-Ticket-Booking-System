# Online Movie Ticket Booking System

A web-based application that allows users to browse movies, select theaters, choose seats, and book tickets online with an integrated payment system.

## Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Configuration](#configuration)
- [API Endpoints](#api-endpoints)
- [Database Schema](#database-schema)
- [Contributing](#contributing)
- [License](#license)

## Features

- **User Authentication**: Secure user registration and login
- **Movie Browsing**: View available movies with details (genre, duration, ratings)
- **Theater Selection**: Choose theaters and showtimes
- **Seat Selection**: Interactive seat map with real-time availability
- **Booking Management**: View, modify, or cancel bookings
- **Payment Integration**: Secure payment processing
- **Notifications**: Email/SMS confirmations for bookings
- **Admin Panel**: Manage movies, theaters, showtimes, and bookings
- **Search & Filter**: Filter movies by genre, language, ratings, etc.
- **User Reviews**: Rate and review movies and theaters

## Tech Stack

### Frontend
- **Framework**: [React/Vue/Angular - choose based on your project]
- **Styling**: CSS/Bootstrap/Tailwind CSS
- **State Management**: Redux/Context API
- **HTTP Client**: Axios/Fetch API

### Backend
- **Language**: [Node.js/Python/Java - choose based on your project]
- **Framework**: [Express/Django/Spring - choose based on your project]
- **Database**: MySQL/PostgreSQL/MongoDB
- **Authentication**: JWT/OAuth

### Tools & Services
- **Payment Gateway**: Stripe/PayPal/Razorpay
- **Hosting**: Heroku/AWS/DigitalOcean
- **Version Control**: Git

## Installation

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn
- [Database] installed and running
- [Other dependencies]

### Clone the Repository
```bash
git clone https://github.com/dhakedipali6-creator/Online-Movie-Ticket-Booking-System.git
cd Online-Movie-Ticket-Booking-System
```

### Backend Setup
```bash
cd backend
npm install
cp .env.example .env
# Update .env with your configuration
npm run dev
```

### Frontend Setup
```bash
cd frontend
npm install
npm start
```

## Usage

1. **Register/Login**: Create an account or sign in
2. **Browse Movies**: View available movies with showtimes
3. **Select Theater & Showtime**: Choose preferred theater and time
4. **Select Seats**: Pick available seats from the interactive map
5. **Review & Confirm**: Review booking details
6. **Make Payment**: Complete payment securely
7. **Confirmation**: Receive booking confirmation via email/SMS

## Project Structure

```
Online-Movie-Ticket-Booking-System/
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   └── App.js
│   ├── public/
│   └── package.json
├── backend/
│   ├── src/
│   │   ├── models/
│   │   ├── routes/
│   │   ├── controllers/
│   │   ├── middleware/
│   │   └── app.js
│   ├── config/
│   └── package.json
├── database/
│   └── schema.sql
└── README.md
```

## Configuration

Create a `.env` file in the backend directory with the following variables:

```
# Database
DB_HOST=localhost
DB_USER=your_db_user
DB_PASSWORD=your_db_password
DB_NAME=movie_ticket_db

# Server
PORT=5000
NODE_ENV=development

# Authentication
JWT_SECRET=your_jwt_secret_key

# Payment Gateway
STRIPE_API_KEY=your_stripe_key
STRIPE_SECRET_KEY=your_stripe_secret

# Email Service
EMAIL_USER=your_email
EMAIL_PASSWORD=your_email_password

# Frontend URL
REACT_APP_API_URL=http://localhost:5000
```

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout

### Movies
- `GET /api/movies` - Get all movies
- `GET /api/movies/:id` - Get movie details
- `POST /api/movies` - Add movie (Admin)
- `PUT /api/movies/:id` - Update movie (Admin)

### Theaters
- `GET /api/theaters` - Get all theaters
- `GET /api/theaters/:id` - Get theater details

### Bookings
- `GET /api/bookings` - Get user bookings
- `POST /api/bookings` - Create booking
- `GET /api/bookings/:id` - Get booking details
- `PUT /api/bookings/:id/cancel` - Cancel booking

### Payment
- `POST /api/payment/process` - Process payment
- `POST /api/payment/verify` - Verify payment

## Database Schema

### Users Table
```sql
CREATE TABLE users (
  id INT PRIMARY KEY AUTO_INCREMENT,
  name VARCHAR(100),
  email VARCHAR(100) UNIQUE,
  password VARCHAR(255),
  phone VARCHAR(20),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

### Movies Table
```sql
CREATE TABLE movies (
  id INT PRIMARY KEY AUTO_INCREMENT,
  title VARCHAR(200),
  description TEXT,
  genre VARCHAR(100),
  duration INT,
  language VARCHAR(50),
  rating DECIMAL(3,1),
  release_date DATE,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

[Add more tables as per your schema]

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Author

**Dipali Dhake**
- GitHub: [@dhakedipali6-creator](https://github.com/dhakedipali6-creator)

## Support

For support, email [your-email@example.com] or open an issue in the repository.

## Acknowledgments

- [List any libraries, frameworks, or resources used]
- [Credits to team members or contributors]