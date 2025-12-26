# 🏥 Doctor System – Advanced Healthcare Appointment Platform

![Node.js](https://img.shields.io/badge/Node.js-v18+-brightgreen)
![Express](https://img.shields.io/badge/Express-4.x-blue)
![MongoDB](https://img.shields.io/badge/MongoDB-6.x-green)
![JWT](https://img.shields.io/badge/JWT-Auth-orange)
![NodeMailer](https://img.shields.io/badge/NodeMailer-email-green)
![Socket.io](https://img.shields.io/badge/Socket.io-Realtime-red)

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

## ⚙️ Installation & Setup

### Prerequisites

* **Node.js** v18+
* **MongoDB** (Atlas or local)
* **Cloudinary, Twilio, Google Developer accounts** (for full functionality)

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

3. **Configure environment variables**
   Create a `.env` file:

   ```env
   PORT=3000
   NODE_ENV=development
   MONGO_URI=mongodb://localhost:27017/doctor_system
   ACCESS_TOKEN_KEY=access_token
   REFRESH_TOKEN_KEY=refresh_token
   ACCESS_TOKEN_SECRET=your_access_token_secret_here
   REFRESH_TOKEN_SECRET=your_refresh_token_secret_here
   ACCESS_TOKEN_DURATION=1h
   REFRESH_TOKEN_DURATION=7d
   ENC_SECRET_KEY=your_encryption_secret_key_here
   APP_EMAIL=your_email@gmail.com
   APP_PASSWORD=your_app_specific_password
   APPLICATION_NAME=Doctor_System
   CLOUDINARY_CLOUD_NAME=your_cloud_name
   CLOUDINARY_API_KEY=your_api_key
   CLOUDINARY_API_SECRET=your_api_secret
   PAYPAL_CLIENT_ID=your_paypal_client_id
   PAYPAL_CLIENT_SECRET=your_paypal_client_secret
   PAYPAL_BASE_URL=https://api-m.sandbox.paypal.com
   PAYPAL_RETURN_URL=http://localhost:4200/booking/success
   PAYPAL_CANCEL_URL=http://localhost:4200/booking/cancel
   TWILIO_ACCOUNT_SID=your_twilio_sid
   TWILIO_AUTH_TOKEN=your_twilio_auth_token
   TWILIO_PHONE_NUMBER=your_twilio_phone_number
   WEB_CLIENT_ID=your_google_client_id.apps.googleusercontent.com
   GOOGLE_MAPS_API_KEY=your_google_maps_api_key
   ```

4. **Run the application**

   ```bash
   # Development
   npm run dev

   # Production
   npm start
   ```

---

## 🛡️ Security Highlights

* XSS protection and Helmet headers
* Rate limiting on sensitive endpoints
* CORS configured for secure cross-origin requests
* Joi schema validation for strict input control

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

---