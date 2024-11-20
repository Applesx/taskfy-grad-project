🌟 Overview
The Task Management System is a web-based application designed to help users manage their daily tasks efficiently. With features such as task creation, editing, deletion, and filtering, this system is perfect for improving productivity and staying organized.

🚀 Features
🔒 User Registration & Login: Secure user authentication with JWT.

📝 Task Creation: Add tasks with a title, description, and priority.

✏️ Task Editing: Modify existing tasks.

🗑️ Task Deletion: Remove tasks from the list.

🔍 Task Filtering: Filter tasks by priority, status, or due date.

🔎 Task Search: Search tasks by title or keyword.

👤 Profile Management: Update user profile information.

💻 Technologies Used
Frontend
⚛️ Next.js: React-based framework for frontend rendering.

🎨 Tailwind CSS: For styling and responsive design.

🔄 React Hooks: State management using useState and side effects with useEffect.

📡 Axios: To make HTTP requests to the backend.
Backend
🛠️ Express.js: Node.js framework for backend routing and APIs.

🔐 TypeScript: For strict typing and better code quality.

📊 Prisma ORM: For MongoDB database management.

🛡️ JWT: JSON Web Tokens for authentication and authorization.

Database
🗄️ MongoDB: For storing user data and tasks.

⚙️ Installation

Prerequisites

Ensure you have the following installed:

🟢 Node.js (v14 or later)

🟢 MongoDB

🟢 npm (Node Package Manager)

Steps to Install

Clone the repository:

bash
Copy code
git clone "repo link"
cd to the project
Install dependencies:

bash
Copy code
npm install
Set up environment variables: Create a .env file in the root directory and add the following:

bash
Copy code

PORT=8000

MONGODB_URI=your_mongodb_connection_string

JWT_SECRET=your_secret_key

CLIENT_URI=your client port "localhost:3000http://localhost:3000"

Start the development server:

bash

Copy code

npm run dev

Open your browser and navigate to http://localhost:3000.

📄 API Documentation
Authentication

POST /auth/register

Register a new user.

Request Body:

json
```
{
  "name": "John Doe",
  "email": "john@example.com",
  "password": "yourpassword"
}
```
POST /auth/login
Login and receive a JWT token.
Request Body:

json
```
{
  "email": "john@example.com",
  "password": "yourpassword"
}
```
Tasks
GET /tasks
Fetch all tasks for the authenticated user.

POST /task/create
Create a new task.
Request Body:

json
```{
  "title": "Task Title",
  "description": "Task Description",
  "priority": "high"
}
```
PATCH /task/

Update a task by ID.
Request Body:

json
```{
  "title": "Updated Task Title",
  "description": "Updated Description",
  "priority": "medium"
}
```
DELETE /task/

Delete a task by ID.

Profile
GET /profile
Get the authenticated user's profile information.

PATCH /profile
Update the user's profile.
Request Body:

json
```{
  "name": "Updated Name",
  "email": "updatedemail@example.com"
}
```
🛠️ System Design
Architecture

Frontend: Built using Next.js with Axios for HTTP requests.

Backend: Express.js (TypeScript) REST API handling authentication and task management.

Database: MongoDB with Prisma ORM.

Database Schema

User Collection

json
```json
{
  "_id": "ObjectId",
  "name": "string",
  "email": "string",
  "password": "string (hashed)",
  "createdAt": "Date",
  "updatedAt": "Date"
}
```

Task Collection
```json
{
  "_id": "ObjectId",
  "title": "string",
  "description": "string",
  "priority": "string (low | medium | high)",
  "completed": "boolean",
  "userId": "ObjectId (ref: User)",
  "createdAt": "Date",
  "updatedAt": "Date"
}
```
🔧 Testing
Manual Testing:

Tested using Postman for API endpoint validation.

Frontend Testing:

Verified task creation, editing, and deletion using a browser for manual UI testing.

🧠 Challenges Faced

JWT Implementation: Managing token expiry and user session control.

Efficient MongoDB Queries: Optimizing task filtering and sorting.

Prisma ORM Integration: Ensuring smooth schema management and complex queries.

🔮 Future Enhancements

🔔 Notifications: Push notifications for upcoming tasks or deadlines.

🤝 Task Sharing: Assign tasks to other users for collaboration.

📱 Mobile App: Build a mobile version using React Native or Flutter.

🏷️ Advanced Filtering: Add custom tags and improved task sorting options.

🏁 Conclusion
The Task Management System is a comprehensive solution for managing tasks efficiently.
Built using modern web technologies like Next.js, Express.js, MongoDB, and Prisma ORM, this system is designed to enhance productivity and organization
