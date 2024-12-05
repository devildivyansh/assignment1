Hosted Link : https://virtual-exhibition-app.vercel.app/login

Virtual Exhibition Web App
This is a full-stack web application designed for virtual exhibitions. It includes a frontend, backend, and database integration with MongoDB for data management. The app allows users to interact with the exhibition, perform CRUD (Create, Read, Update, Delete) operations, and features user authentication.

Technologies Used
Frontend: React.js
Backend: Node.js, Express.js
Database: MongoDB
Authentication: JWT (JSON Web Token)
Features
User registration and login (authentication)
CRUD operations for exhibitions, including creating, viewing, updating, and deleting exhibitions
Secure user authentication using JWT
Dynamic exhibition listings with detailed views
Responsive design for an interactive user experience
Setup Instructions
1. Clone the repository
Clone the repository to your local machine using:

bash
 
git clone https://github.com/yourusername/virtual-exhibition-app.git
2. Install dependencies
Navigate to both the frontend and backend directories and install the necessary dependencies.

Frontend:

Navigate to the frontend directory:

bash
 
cd frontend
npm install


Backend:

Navigate to the backend directory:

bash
 
cd backend
npm install
3. Environment Variables
Create a .env file in the backend directory and add the following environment variables:

bash
 
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
Replace your_mongodb_connection_string with your actual MongoDB URI, and your_jwt_secret with a secret key for signing JWT tokens.

4. Start the Application
Frontend:

Navigate to the frontend directory and run the following command to start the React app:

bash:
npm start
Backend:

Navigate to the backend directory and run the following command to start the backend server:

bash
npm run dev
The backend will run on the default port 5000 and the frontend will run on 3000.

5. Access the App
Once both the frontend and backend are running, you can access the app in your browser by visiting:

bash:
http://localhost:3000
6. MongoDB Setup
Ensure you have a running MongoDB instance or use MongoDB Atlas for cloud-based database hosting. You can sign up and create a cluster on MongoDB Atlas for remote storage.

Project Structure
Frontend
bash:
/frontend
  /public
  /src
    /components
    /contexts
    /services
    App.js
    index.js
  package.json
Backend
bash
 
/backend
  /models
  /routes
  /controllers
  /middlewares
  server.js
  package.json
API Endpoints
POST /api/auth/register: User registration
POST /api/auth/login: User login
GET /api/exhibitions: Fetch all exhibitions
POST /api/exhibitions: Create a new exhibition
GET /api/exhibitions/:id: Get a single exhibition
PUT /api/exhibitions/:id: Update an exhibition
DELETE /api/exhibitions/:id: Delete an exhibition
