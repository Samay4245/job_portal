# Job Portal

A full-stack job portal built with React, Express, and MongoDB. Users can browse and apply for jobs, manage their profiles, and track applications. Admin users can manage companies, post jobs, and review applicants.

## Project structure

- `backend/` - Express API and MongoDB models
- `frontend/` - React and Vite application

## Requirements

- Node.js 18 or later
- npm
- MongoDB connection string

## Run locally

1. Clone the repository and enter its directory:

   ```bash
   git clone https://github.com/Samay4245/job_portal.git
   cd job_portal
   ```

2. Configure the backend:

   ```bash
   cd backend
   npm install
   ```

   Create `backend/.env` with your own values:

   ```env
   PORT=3000
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_secret_key
   CLOUDINARY_CLOUD_NAME=your_cloud_name
   CLOUDINARY_API_KEY=your_api_key
   CLOUDINARY_API_SECRET=your_api_secret
   ```

   Start the API:

   ```bash
   npm run dev
   ```

3. In a second terminal, install and start the frontend:

   ```bash
   cd frontend
   npm install
   npm run dev
   ```

The frontend is served at `http://localhost:5173` and the API at `http://localhost:3000`.

See [frontend/README.md](./frontend/README.md) for the feature list and API overview.
