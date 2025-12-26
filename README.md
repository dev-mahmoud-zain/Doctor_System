# D# 🏥 Doctor System - Healthcare Appointment Platform

A robust and scalable healthcare management system built with **Node.js**, **Express**, and **MongoDB**. This project was developed as part of a professional training program with **Huma-volve**. It streamlines the process of booking doctor appointments, managing patient records, and facilitates real-time communication between doctors and patients.

---

## 🚀 Key Features

### 🔐 Authentication & Authorization
- **Multi-role Support**: Separate workflows for Patients and Doctors.
- **Secure Sign-up/Login**: Using JWT for stateless session management.
- **Social Auth**: Google Authentication integration.
- **Verification**: OTP-based email and phone verification.
- **Account Security**: Password hashing with `bcrypt`, rate limiting, and security headers with `helmet`.

### 📅 Booking & Management
- **Appointment Scheduling**: Patients can browse doctors and book available slots.
- **Status Lifecycle**: Manage booking states (pending, confirmed, cancelled).
- **Doctor Profiles**: Detailed information about specializations and availability.

### 💬 Real-time Communication
- **Instant Messaging**: Integrated **Socket.IO** for real-time chat between doctors and patients.
- **Message Persistence**: All chats are stored for future reference.

### 🌟 Reviews & Feedback
- **Rating System**: Patients can leave reviews and ratings for doctors after their appointments.

---

## 🛠️ Technology Stack

- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: MongoDB with Mongoose ODM
- **Real-time**: Socket.io
- **Security**: JWT, Bcrypt, Helmet, Express-rate-limit
- **Media**: Cloudinary (for profile and medical record uploads)
- **Communication**: Nodemailer (Email), Twilio (SMS/OTP)
- **Validation**: Joi (Schema validation)
- **State Management**: XState

---

## 📂 Project Structure

```text
├── DB                  # Database connection and Mongoose schemas
│   ├── models          # Data models (Doctor, Patient, Booking, Chat, etc.)
│   └── connect.js      # MongoDB connection logic
├── modules             # Core application modules (Business logic)
│   ├── auth            # Login, Signup, OTP, and Social Auth
│   ├── booking         # Appointment scheduling logic
│   ├── chats           # Real-time messaging service
│   ├── review          # Feedback and rating system
│   └── users           # User profile management
├── middleware          # Custom Express middlewares (Auth, Validation)
├── utils               # Helper functions (Uploads, Global Error Handling)
├── index.js            # Entry point of the application
└── package.json        # Dependencies and scripts
```

---

## ⚙️ Installation & Setup

### Prerequisites
- Node.js (v18 or higher)
- MongoDB account (Atlas or Local)
- Cloudinary, Twilio, and Google Developer accounts (for full functionality)

### Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/DAvidOsAmAA/Doctor_System.git
   cd Doctor_System
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Configuration**
   Create a `.env` file in the root directory and add the following:
   ```env
   PORT=3000
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   CLOUDINARY_CLOUD_NAME=your_name
   CLOUDINARY_API_KEY=your_key
   CLOUDINARY_API_SECRET=your_secret
   # Add other keys from .env.example
   ```

4. **Run the application**
   ```bash
   # For development
   npm run dev

   # For production
   npm start
   ```

---

## 🛡️ Security Features

- **XSS Protection**: Sanitization and Helmet headers.
- **Rate Limiting**: To prevent brute-force attacks on sensitive endpoints.
- **CORS**: Configured for secure cross-origin requests.
- **Data Validation**: Strict schema validation using Joi before processing any request.

---

## 🤝 Contribution

This project was a collaborative effort during the Huma-volve internship. Special thanks to the team for their contributions to building a comprehensive healthcare solution.

---

## 📄 License

This project is licensed under the ISC License.


# register branch has been added