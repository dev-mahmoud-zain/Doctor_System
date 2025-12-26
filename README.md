# 🏥 Doctor System – Advanced Healthcare Appointment Platform

![Node.js](https://img.shields.io/badge/Node.js-v18+-brightgreen)

![Express](https://img.shields.io/badge/Express-4.x-blue)

![MongoDB](https://img.shields.io/badge/MongoDB-6.x-green)


A **scalable and secure healthcare management system** built with **Node.js**, **Express**, and **MongoDB**. Developed during the **Huma-volve professional training program**, this platform simplifies doctor appointment scheduling, patient management, and real-time communication between doctors and patients.

---

## 🚀 Core Features

### 🔐 Authentication & Authorization

* Role-Based Access Control for **Patients** and **Doctors**.
* JWT-based stateless authentication.
* Social Authentication (Google OAuth).
* OTP verification via email & SMS.
* Password hashing with `bcrypt`, rate limiting, and security headers using `helmet`.

### 📅 Booking & Appointment Management

* Browse doctors and book available slots.
* Track appointment status: pending, confirmed, cancelled.
* Doctor profiles with specializations, availability, and consultation history.

### 💬 Real-Time Communication

* Instant messaging between doctors and patients using **Socket.IO**.
* Persistent chat storage for auditing and future reference.

### 🌟 Reviews & Feedback

* Patients can leave reviews and ratings for doctors post-consultation.
* Feedback is aggregated for analytics and reporting.

---

## 🛠️ Technology Stack

* **Runtime & Framework**: Node.js, Express.js
* **Database**: MongoDB with Mongoose ODM
* **Real-Time**: Socket.IO
* **Security**: JWT, bcrypt, Helmet, Express-rate-limit
* **Media**: Cloudinary for profile images & medical records
* **Communication Services**: Nodemailer (Email), Twilio (SMS/OTP)
* **Validation**: Joi
* **State Management**: XState

---

## 📂 Project Structure

```text
Doctor_System/
├── DB                  # Database connection & schemas
│   ├── models          # Doctor, Patient, Booking, Chat, Review, etc.
│   └── connect.js      # MongoDB connection
├── modules             # Core application modules
│   ├── auth            # Authentication & social login
│   ├── booking         # Appointment scheduling
│   ├── chats           # Real-time messaging
│   ├── review          # Ratings & feedback
│   └── users           # User profile management
├── middleware          # Express middlewares (Auth, Validation)
├── utils               # Helper functions (Uploads, Error Handling)
├── index.js            # Application entry point
└── package.json        # Dependencies & scripts
```

---

## ⚙️ Environment Configuration

| Section                | Key                    | Description                       |
| ---------------------- | ---------------------- | --------------------------------- |
| **Server**             | PORT                   | Server listening port             |
|                        | NODE_ENV               | Development or production mode    |
| **Database**           | MONGO_URI              | MongoDB connection string         |
| **JWT**                | ACCESS_TOKEN_KEY       | Key name for access token         |
|                        | REFRESH_TOKEN_KEY      | Key name for refresh token        |
|                        | ACCESS_TOKEN_SECRET    | Secret for signing access token   |
|                        | REFRESH_TOKEN_SECRET   | Secret for signing refresh token  |
|                        | ACCESS_TOKEN_DURATION  | Expiry duration for access token  |
|                        | REFRESH_TOKEN_DURATION | Expiry duration for refresh token |
| **Encryption**         | ENC_SECRET_KEY         | Key for encrypting sensitive data |
| **Email (Nodemailer)** | APP_EMAIL              | Sender email address              |
|                        | APP_PASSWORD           | App-specific password             |
|                        | APPLICATION_NAME       | Name of the application           |
| **Cloudinary**         | CLOUDINARY_CLOUD_NAME  | Cloudinary cloud name             |
|                        | CLOUDINARY_API_KEY     | Cloudinary API key                |
|                        | CLOUDINARY_API_SECRET  | Cloudinary API secret             |
| **PayPal**             | PAYPAL_CLIENT_ID       | PayPal client ID                  |
|                        | PAYPAL_CLIENT_SECRET   | PayPal client secret              |
|                        | PAYPAL_BASE_URL        | PayPal API base URL               |
|                        | PAYPAL_RETURN_URL      | Success redirect URL              |
|                        | PAYPAL_CANCEL_URL      | Cancel redirect URL               |
| **Twilio (SMS OTP)**   | TWILIO_ACCOUNT_SID     | Twilio account SID                |
|                        | TWILIO_AUTH_TOKEN      | Twilio auth token                 |
|                        | TWILIO_PHONE_NUMBER    | Twilio phone number               |
| **Google**             | WEB_CLIENT_ID          | Google OAuth client ID            |
|                        | GOOGLE_MAPS_API_KEY    | Google Maps API key               |

---

## 🤝 Team Members

* Mahmoud Zain
* Hossam Ahmed
* Mohammed Adel
* Mostafa Talaat
* Mohammed Farag

---

## 🤝 Contribution

This project was developed collaboratively during the **Huma-volve internship**.
Special thanks to all contributors for building a full-featured healthcare platform.