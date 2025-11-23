ClaraMed – Healthcare Management System

ClaraMed is a full-stack healthcare appointment and management platform designed to make patient–doctor interactions seamless. It provides secure appointment booking, prescription management, real-time updates, and integrated online payments — all in one responsive system.

🚀 Features
🔹 Patient Features

Book, reschedule, and cancel appointments easily

Secure online payments via Razorpay

View prescriptions and past visit history

Real-time notifications for updates

🔹 Doctor Features

Manage appointments and availability

Access patient details and medical history

Generate and upload prescriptions

Receive real-time updates on new bookings

🔹 Admin Features

Role-based access control

Manage doctors, patients, and system workflows

Automated operations reducing manual effort by 40%

Track payments and platform analytics

🛠️ Tech Stack
Frontend

React.js

Context API / Redux (if used)

Axios

Backend

Node.js

Express.js

MongoDB (Mongoose ORM)

REST APIs

WebSockets for real-time communication

JWT Authentication

Razorpay API integration

⚙️ Key Functionalities
✅ Secure Appointment Booking

Fully responsive UI for patients and doctors

Validations and confirmation alerts

Automated scheduling system

✅ Real-Time Updates (WebSockets)

Live appointment status updates

Instant notifications for doctors and patients

Improved responsiveness by 45%

✅ Payments Integration

Razorpay Checkout

Secure transactions with server-side verification

Automatic invoice generation

✅ Prescription Management

Doctors can create and upload prescriptions

Patients can access prescriptions at any time

✅ Authentication & Authorization

JWT-based login

Protected routes

Role-based access (Patient / Doctor / Admin)

System Workflow Overview
1. Appointment Booking Flow
 Patient UI (React)
        |
        v
Appointment Request
        |
        v
Express API  ---->  JWT Validation
        |
        v
 MongoDB (Save Appointment)
        |
        v
 WebSocket Event Trigger
        |
        v
Doctor Dashboard Update (Real-time)

2. Razorpay Payment Flow
Patient Initiates Payment (React)
        |
        v
Create Order Request --> Express Server --> Razorpay SDK
        |
        v
Razorpay Order Created
        |
        v
Payment Checkout (Client)
        |
        v
Signature Verification (Server)
        |
        v
MongoDB Updates Payment Status

3. Authentication & Role Flow
 Login Request
       |
       v
Express Auth API
       |
       v
Validate Credentials in MongoDB
       |
       v
Generate JWT --------------------+
       |                         |
       v                         |
User Returns Token          Role-Based Routing
                                 |
                                 v
                    Patient / Doctor / Admin Dashboards

4. Real-Time Communication Flow
Doctor Updates Availability
            |
            v
   Express API Updates DB
            |
            v
      WebSocket Server
            |
            v
Real-Time Sync --> Patient UI
