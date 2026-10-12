# Job Portal

A full-stack job portal application built with React on the frontend and Express + MongoDB on the backend. Users can browse and apply for jobs, manage their profile, and track applications, while admins can manage companies, create job listings, and review applicants.

## Features

- User authentication and authorization
- Job listing and detailed job view
- Profile management with image upload support
- Company registration and management
- Job posting for admin users
- Applicant review and application status updates
- Responsive, modern UI
- Secure cookie-based session handling

## Tech Stack

### Frontend
- React
- Vite
- JavaScript
- React Router DOM
- Redux Toolkit
- Tailwind CSS
- Axios
- Framer Motion
- Lucide Icons

### Backend
- Node.js
- Express.js
- MongoDB
- Mongoose
- JWT
- Cloudinary
- Multer
- Cors
- Cookie Parser
- Dotenv

## Repository Structure

```text
jobportal-yt/
├── backend/
│   ├── controllers/
│   ├── middlewares/
│   ├── models/
│   ├── routes/
│   ├── utils/
│   ├── .gitignore
│   ├── index.js
│   ├── package.json
│   └── package-lock.json
├── frontend/
│   ├── public/
│   ├── src/
│   ├── .eslintrc.cjs
│   ├── .gitignore
│   ├── components.json
│   ├── index.html
│   ├── jsconfig.json
│   ├── package.json
│   ├── postcss.config.js
│   ├── tailwind.config.js
│   ├── vite.config.js
│   └── README.md
├── README.md
└── .gitignore
```

## Backend API Overview

The backend runs under `/api/v1` and includes the following modules:

### User Routes
- `POST /api/v1/user/register`
- `POST /api/v1/user/login`
- `GET /api/v1/user/logout`
- `POST /api/v1/user/profile/update`

### Company Routes
- `POST /api/v1/company/register`
- `GET /api/v1/company/get`
- `GET /api/v1/company/get/:id`
- `PUT /api/v1/company/update/:id`

### Job Routes
- `POST /api/v1/job/post`
- `GET /api/v1/job/get`
- `GET /api/v1/job/getadminjobs`
- `GET /api/v1/job/get/:id`

### Application Routes
- `GET /api/v1/application/apply/:id`
- `GET /api/v1/application/get`
- `GET /api/v1/application/:id/applicants`
- `POST /api/v1/application/status/:id/update`

## Frontend Overview

The frontend is built with React and Vite, and includes:

- Home page
- Login and Signup pages
- Job browsing and details
- User profile page
- Admin company management
- Admin job posting
- Applicants dashboard

## Prerequisites

Before running this project, make sure you have:

- Node.js 18 or later
- npm
- MongoDB instance or MongoDB Atlas connection string

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Samay4245/job_portal.git
cd job_portal
```

### 2. Setup the backend

```bash
cd backend
npm install
```

Create a `.env` file inside `backend` with the following values:

```env
PORT=3000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
```

Start the backend:

```bash
npm run dev
```

### 3. Setup the frontend

```bash
cd ../frontend
npm install
```

Start the frontend:

```bash
npm run dev
```

The frontend typically runs at:

```text
http://localhost:5173
```

The backend typically runs at:

```text
http://localhost:3000
```

## Environment Notes

- CORS is configured for `http://localhost:5173`
- MongoDB is connected inside `backend/utils/db.js`
- Protected routes use authentication middleware
- Cloudinary is used for file/image handling

## License

This project is licensed under the ISC License.

## Author

Surendrakumar Patel

## Contributing

Contributions are welcome. If you find a bug or want to add a feature, feel free to open an issue or submit a pull request with a clear description of the change.