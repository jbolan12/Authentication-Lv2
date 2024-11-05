# Authentication-Lv2

Express Authentication App
This application is a simple authentication system built with Node.js, Express, PostgreSQL, and bcrypt for password hashing. It allows users to register and log in securely with hashed passwords.

->Features
User Registration: Users can register with an email and password.
Password Hashing: User passwords are hashed using bcrypt for secure storage.
User Login: Registered users can log in using their credentials.
Environment Configuration: Sensitive information (database credentials) is stored in environment variables.

->Technologies Used
Express: Web framework for Node.js
PostgreSQL: Database for storing user information
bcrypt: Library for hashing passwords
dotenv: Module for loading environment variables from a .env file
body-parser: Middleware for parsing form data

->Prerequisites
Node.js (v12 or later)
PostgreSQL
Environment variables configured in a .env file

->Installation
Clone the repository:

bash
git clone (https://github.com/jbolan12/Authentication-Lv2)
cd express-authentication-app

->Install dependencies:

bash
npm install

->Set up the database:

Create a PostgreSQL database and a table for storing users.
Example users table schema:

sql
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  email VARCHAR(255) UNIQUE NOT NULL,
  password VARCHAR(255) NOT NULL
);

Create a .env file in the project root and add your database credentials:

plaintext
Copiar código
DB_USER=your_db_user
DB_HOST=localhost
DB_NAME=your_db_name
DB_PASSWORD=your_db_password
DB_PORT=5432

->Usage
Start the server:

bash
node index.js
Access the application:
Go to http://localhost:3000 in your browser.

->Routes
GET /: Home page
GET /register: Registration page
POST /register: Handles user registration with password hashing
GET /login: Login page
POST /login: Verifies user credentials

->Code Overview
Password Hashing: Passwords are hashed with bcrypt before saving to the database to enhance security.
Environment Variables: Sensitive configuration data is stored in .env to keep it out of the codebase.

->Dependencies:
express: ^4.17.1
body-parser: ^1.19.0
pg: ^8.7.1
bcrypt: ^5.0.1
dotenv: ^10.0.0

License
This project is licensed under the MIT License.
