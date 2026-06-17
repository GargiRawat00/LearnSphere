# LearnSphere

LearnSphere is a full-stack EdTech platform that allows students to explore and purchase courses, while instructors can create, manage, and publish course content. The platform includes authentication, OTP verification, role-based dashboards, course management, secure payments, media uploads, ratings, reviews, and course progress tracking.

## Project Overview

LearnSphere is designed to provide a complete online learning experience. Students can browse available courses, view course details, add courses to their cart, make payments, and access enrolled courses. Instructors can create courses, add course sections and lectures, upload thumbnails and videos, and manage their published content.

The project follows a full-stack architecture where the React frontend communicates with the Node.js and Express backend through REST APIs. MongoDB is used as the database, while Cloudinary is used for media storage, Nodemailer for email/OTP services, and Razorpay for payment integration.

## Features

### Student Features

- User signup and login
- OTP-based email verification
- Browse course categories
- View course details
- Add courses to cart
- Purchase courses using Razorpay
- Access enrolled courses
- Track course progress
- Add ratings and reviews
- Manage profile details

### Instructor Features

- Instructor dashboard
- Create and edit courses
- Add course sections and subsections
- Upload course thumbnails and lecture content
- View created courses
- Manage course content
- Track course-related information

### Authentication and Security

- JWT-based authentication
- Password hashing using bcrypt
- Protected routes for authenticated users
- Role-based access for students and instructors
- OTP verification through email
- Password reset functionality

## Tech Stack

### Frontend

- React.js
- React Router DOM
- Redux Toolkit
- Tailwind CSS
- Axios
- React Hook Form
- React Hot Toast

### Backend

- Node.js
- Express.js
- MongoDB
- Mongoose
- JWT
- Bcrypt
- Cookie Parser
- Express File Upload

### Third-Party Services

- Cloudinary for media upload and storage
- Nodemailer for sending OTP and email notifications
- Razorpay for payment integration

## Folder Structure

```text
LearnSphere/
│
├── public/
│   └── Static assets
│
├── src/
│   ├── assets/
│   ├── components/
│   ├── pages/
│   ├── services/
│   ├── slices/
│   ├── utils/
│   └── App.js
│
├── server/
│   ├── config/
│   ├── controllers/
│   ├── mail/
│   ├── middlewares/
│   ├── models/
│   ├── routes/
│   ├── utils/
│   └── index.js
│
├── package.json
├── tailwind.config.js
└── README.md
```

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/GargiRawat00/LearnSphere.git
cd LearnSphere
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

### 4. Configure environment variables

Create a `.env` file in the root folder:

```env
REACT_APP_BASE_URL=http://localhost:4000/api/v1
```

Create another `.env` file inside the `server` folder:

```env
PORT=4000
MONGODB_URL=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret

MAIL_HOST=your_mail_host
MAIL_USER=your_mail_user
MAIL_PASS=your_mail_password

CLOUD_NAME=your_cloudinary_cloud_name
API_KEY=your_cloudinary_api_key
API_SECRET=your_cloudinary_api_secret
FOLDER_NAME=your_cloudinary_folder_name

RAZORPAY_KEY=your_razorpay_key
RAZORPAY_SECRET=your_razorpay_secret
```

### 5. Run the project

Start the backend server:

```bash
cd server
npm run dev
```

Start the frontend in another terminal:

```bash
npm start
```

The application will run at:

```text
Frontend: http://localhost:3000
Backend:  http://localhost:4000
```

## API Modules

The backend is divided into multiple modules:

- Authentication APIs for signup, login, OTP verification, and password reset
- Profile APIs for user profile management
- Course APIs for course creation, editing, category management, and course details
- Payment APIs for Razorpay order creation and payment verification
- Rating and review APIs for course feedback

## Database Design

The project uses MongoDB with Mongoose models. Major collections include:

- Users
- Profiles
- Courses
- Categories
- Sections
- Subsections
- Ratings and Reviews
- OTPs
- Course Progress

## How LearnSphere Works

1. A user signs up and verifies their email through OTP.
2. The backend stores user information securely in MongoDB.
3. After login, the backend generates a JWT token.
4. The frontend uses the token to access protected routes.
5. Students can browse courses and purchase them through Razorpay.
6. Instructors can create courses and upload course content using Cloudinary.
7. Course progress and enrolled course data are stored in MongoDB.

## Screenshots

Add screenshots here after running the project locally.

```text
Home Page
Signup Page
Login Page
Student Dashboard
Instructor Dashboard
Course Details Page
```

## Future Improvements

- Add admin dashboard
- Add live classes support
- Add course search and advanced filters
- Add wishlist functionality
- Add certificate generation after course completion
- Improve analytics for instructors
- Add deployment on cloud platforms

## Author

**Gargi Rawat**

GitHub: [GargiRawat00](https://github.com/GargiRawat00)

## License

This project is created for learning and portfolio purposes.
