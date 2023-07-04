# Login/Signup Node.js Application

This is a basic login/signup application built with Node.js, Express, and MongoDB. It provides user authentication and registration functionality using a RESTful API.

## Features

- User registration with email and password
- User login with email and password
- Password hashing for security
- JSON Web Tokens (JWT) for session management
- MongoDB for data storage
- RESTful API endpoints for user operations

## Prerequisites

- Node.js installed on your machine
- MongoDB installed and running
- Basic knowledge of JavaScript and Node.js

<h2>Getting Started</h2>
  <ol>
    <li>Clone the repository:</li>
    <code>git clone https://github.com/your-username/login-signup-nodejs.git</code>
    <li>Install the dependencies:</li>
    <code>cd login-signup-nodejs</code><br>
    <code>npm install</code>
    <li>Configure the environment variables:</li>
    <p>Create a <code>.env</code> file in the root of the project and provide the following values:</p>
    <pre>
PORT=3000
MONGODB_URI=mongodb://localhost:27017/login-signup
JWT_SECRET=your-secret-key
    </pre>
    <ul>
      <li><code>PORT</code> - Port on which the server will run.</li>
      <li><code>MONGODB_URI</code> - Connection string for your MongoDB database.</li>
      <li><code>JWT_SECRET</code> - Secret key for signing JSON Web Tokens.</li>
    </ul>
    <li>Start the server:</li>
    <code>npm start</code>
    <p>The server will start running on the specified port.</p>
  </ol>
  <h2>API Endpoints</h2>
  <h3>Signup</h3>
  <ul>
    <li>URL: <code>/api/signup</code></li>
    <li>Method: <code>POST</code></li>
    <li>Body:</li>
    <pre>
{
  "email": "user@example.com",
  "password": "password123"
}
    </pre>
    <li>Response:</li>
    <pre>
{
  "success": true,
  "message": "User registered successfully"
}
    </pre>
  </ul>
  <h3>Login</h3>
  <ul>
    <li>URL: <code>/api/login</code></li>
    <li>Method: <code>POST</code></li>
    <li>Body:</li>
    <pre>
{
  "email": "user@example.com",
  "password": "password123"
}
    </pre>
    <li>Response:</li>
    <pre>
{
  "success": true,
  "token": "your-jwt-token"
}
    </pre>
  </ul>
  <h3>Profile</h3>
  <ul>
    <li>URL: <code>/api/profile</code></li>
    <li>Method: <code>GET</code></li>
    <li>Headers:</li>
    <pre>
Authorization: Bearer your-jwt-token
    </pre>
    <li>Response:</li>
    <pre>
{
  "email": "user@example.com"
}
    </pre>
  </ul>
  <h2>Contributing</h2>
  <p>Contributions are welcome! If you find any issues or have suggestions for improvements, please feel free to submit a pull request.</p>
  <h2>License</h2>
  <p>This project is licensed under the <a href="LICENSE">MIT License</a>.</p>
