Name: Prakhar Sharma
Reg No. RA2011026030002
Dept. & Branch: B.tech CSE (AI & ML)

# Project for Hyrr for full stack developer role

I crafted this project as an assignment for the Full Stack Developer position at Hyrr. Here's a breakdown of what I've done:

## What I Did

### User Authentication
I implemented user authentication features, including:
- User registration
- Login functionality
- Protected routes
- Logout capability
- Password change functionality

## How I Built It

### Technologies which I Used for this project
- **Node.js:** For server-side JavaScript.
- **Express:** A framework to build APIs easily.
- **MongoDB:** A NoSQL database to store user data.
- **Mongoose:** To interact smoothly with MongoDB.
- **bcrypt:** For secure password hashing.
- **jsonwebtoken (JWT):** For creating and validating tokens.

### My Project Structure
- **server/:** The main folder for all server-related files.
  - **auth/:** Holds authentication routes and middleware.
    - **auth.js:** Manages user registration, login, protected routes, logout, and password change.
    - **authMiddleware.js:** Middleware for token verification and refresh.
  - **middlewares/:** Custom middleware for the application.
    - **authMiddleware.js:** Ensures secure authentication.
  - **models/:** Defines MongoDB schema.
    - **User.js:** Schema for the User model.
  - **routes/:** Contains various application routes.
    - **auth.js:** Manages user authentication routes.
  - **index.js:** The main entry point for the application.
- **key.env:** Houses sensitive information like the JWT secret key.
- **.gitignore:** Specifies files and directories to exclude from version control.
- **package.json:** Lists project dependencies and configurations.


#### 1. User Registration
- Endpoint: `/auth/signup`
- Description: Allows users to create an account with a unique username, email, and password.
- How to Use:
  bash
curl -X POST -H "Content-Type: application/json" -d '{"username": "your-username", "email": "your-email@example.com", "password": "your-password"}' http://localhost:3003/auth/signup




# Below is a comprehensive overview of what I accomplished.

## What and how I Implemented my project

1. User Registration

- Endpoint: `/auth/signup`
- Description: Allows users to create an account with a unique username, email, and password.
- How to Use:
  bash
  curl -X POST -H "Content-Type: application/json" -d '{"username": "your-username", "email": "your-email@example.com", "password": "your-password"}' http://localhost:3003/auth/signup

2. User Login

Endpoint: /auth/login
Description: Enables users to log in securely using their username and password.
How to Use:
bash
curl -X POST -H "Content-Type: application/json" -d '{"username": "your-username", "password": "your-password"}' http://localhost:3003/auth/login

3.Protected Routes

Endpoints: /auth/user/details, /protected
Description: Accessible only with a valid JWT token, providing user details and a protected route example.
How to Use:
curl -X GET -H "Authorization: Bearer your-jwt-token" http://localhost:3003/auth/user/details
curl -X GET -H "Authorization: Bearer your-jwt-token" http://localhost:3003/protected

//I used 3003 server

4. Logout

Endpoint: /auth/logout
Description: Allows users to log out securely with no server-side action.
How to Use:
curl -X POST -H "Authorization: Bearer your-jwt-token" http://localhost:3003/auth/logout

5.Change Password

Endpoint: /auth/changepassword
Description: Permits users to change their passwords securely.
How to Use:
curl -X POST -H "Authorization: Bearer your-jwt-token" -d '{"oldPassword": "your-old-password", "newPassword": "your-new-password"}' http://localhost:3003/auth/changepassword
