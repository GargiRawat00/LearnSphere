# Learn Sphere

Learn Sphere is a full-stack EdTech platform where students can explore and purchase courses, while instructors can create, manage, and track their course content. The project includes authentication, role-based dashboards, course management, secure payments, media uploads, email notifications, ratings, reviews, and course progress tracking.

## GitHub Description

Full-stack EdTech platform built with React, Node.js, Express, MongoDB, JWT authentication, Cloudinary, Nodemailer, and Razorpay.

## Features

- Student and instructor authentication
- OTP-based email verification
- JWT-based protected routes
- Role-based dashboard for students and instructors
- Course creation and management
- Section and subsection management for course content
- Course catalog and course details pages
- Cart and course enrollment flow
- Razorpay payment integration
- Cloudinary media upload support
- Email notifications using Nodemailer
- Ratings and reviews for courses
- Profile management and display picture update
- Course progress tracking
- Responsive frontend UI

## Tech Stack

### Frontend

- React.js
- React Router DOM
- Redux Toolkit
- Tailwind CSS
- Axios
- React Hook Form
- React Hot Toast
- Chart.js

### Backend

- Node.js
- Express.js
- MongoDB
- Mongoose
- JWT Authentication
- Bcrypt
- Cookie Parser
- Express File Upload

### Third-Party Services

- Cloudinary for media storage
- Nodemailer for sending emails and OTPs
- Razorpay for payment processing

## Project Structure

```text
Learn-Sphere/
├── public/
├── src/
│   ├── assets/
│   ├── components/
│   ├── pages/
│   ├── services/
│   ├── slices/
│   ├── utils/
│   ├── App.js
│   └── index.js
├── server/
│   ├── config/
│   ├── controllers/
│   ├── mail/
│   ├── middlewares/
│   ├── models/
│   ├── routes/
│   ├── utils/
│   └── index.js
├── package.json
└── README.md
```

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_GITHUB_USERNAME/Learn-Sphere.git
cd Learn-Sphere
```

### 2. Install frontend dependencies

```bash
npm install
```

### 3. Install backend dependencies

```bash
cd server
npm install
cd ..
```

### 4. Create environment file

Create a `.env` file inside the `server` folder.

```env
PORT=4000
MONGODB_URL=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret

CLOUD_NAME=your_cloudinary_cloud_name
API_KEY=your_cloudinary_api_key
API_SECRET=your_cloudinary_api_secret
FOLDER_NAME=your_cloudinary_folder_name

MAIL_HOST=your_smtp_host
MAIL_USER=your_smtp_user
MAIL_PASS=your_smtp_password

RAZORPAY_KEY=your_razorpay_key
RAZORPAY_SECRET=your_razorpay_secret
```

### 5. Run the project

To run frontend and backend together:

```bash
npm run dev
```

Frontend runs on:

```text
http://localhost:3000
```

Backend runs on:

```text
http://localhost:4000
```

## Main Modules

### Authentication Module

Handles signup, login, OTP verification, password reset, password change, and JWT-based user authentication.

### Course Module

Allows instructors to create courses, add sections and subsections, upload course content, edit courses, delete courses, and view instructor-specific courses.

### Student Module

Allows students to browse courses, view course details, add courses to cart, purchase courses, access enrolled courses, and track progress.

### Payment Module

Uses Razorpay to capture and verify course payments. After successful payment, enrollment and confirmation emails are handled by the backend.

### Profile Module

Allows users to update profile details, upload display pictures, view enrolled courses, and manage account settings.

## API Overview

### Auth Routes

```text
POST /api/v1/auth/signup
POST /api/v1/auth/login
POST /api/v1/auth/sendotp
POST /api/v1/auth/changepassword
POST /api/v1/auth/reset-password-token
POST /api/v1/auth/reset-password
```

### Course Routes

```text
POST /api/v1/course/createCourse
POST /api/v1/course/addSection
POST /api/v1/course/addSubSection
GET  /api/v1/course/getAllCourses
POST /api/v1/course/getCourseDetails
POST /api/v1/course/getFullCourseDetails
POST /api/v1/course/editCourse
GET  /api/v1/course/getInstructorCourses
POST /api/v1/course/updateCourseProgress
```

### Profile Routes

```text
GET    /api/v1/profile/getUserDetails
PUT    /api/v1/profile/updateProfile
PUT    /api/v1/profile/updateDisplayPicture
GET    /api/v1/profile/getEnrolledCourses
GET    /api/v1/profile/instructorDashboard
DELETE /api/v1/profile/deleteProfile
```

### Payment Routes

```text
POST /api/v1/payment/capturePayment
POST /api/v1/payment/verifyPayment
POST /api/v1/payment/sendPaymentSuccessEmail
```

## Learning Purpose

This project is useful for understanding how a real full-stack web application works. It covers frontend development, backend API design, database modeling, authentication, file upload, payment gateway integration, email handling, and role-based access control.

## Author

**Gargi Rawat**
