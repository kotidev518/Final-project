# How to Run the Project

## Prerequisites
- **Python 3.8+**
- **Node.js 16+**
- **MongoDB** (Must be running locally on port 27017)

## Backend Setup (FastAPI)
1. Navigate to the backend directory:
   ```bash
   cd backend
   ```
2. Ensure `backend/.env` exists. It should contain:
   ```
   MONGO_URL=mongodb://localhost:27017
   DB_NAME=learning_platform
   JWT_SECRET=development_secret_key
   CORS_ORIGINS=http://localhost:3000
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the server:
   ```bash
   uvicorn server:app --reload
   ```
   The backend will start at `http://localhost:8000`. You can view the API documentation at `http://localhost:8000/docs`.

## Frontend Setup (React)
1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Configure environment variables:
   - Create a `.env` file in the `frontend` directory (you can rename `env.txt` to `.env`).
   - Update `REACT_APP_BACKEND_URL` to point to your local backend:
     ```
     REACT_APP_BACKEND_URL=http://localhost:8000
     ```
   *(Note: The default `env.txt` might point to a remote URL. Change it to localhost for local development.)*

4. Start the application:
   ```bash
   npm start
   ```
   The application will open at `http://localhost:3000`.
