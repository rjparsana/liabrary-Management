# Book Store Management API
This project is a backend API for a book store management system. The API is built using Node.js and Express, with MongoDB as the database. It handles operations related to managing books, such as adding, updating, deleting books, and retrieving book information.

## Features
User Authentication: Users can register and log in to access the API.
CRUD Operations on Books: You can create, read, update, and delete books.
Borrow/Return Books: Users can borrow and return books (eBooks).
Validation and Error Handling: Input validation and error handling are implemented to ensure data integrity.

## Project Structure
├── controllers/        # Contains all the controller logic
├── models/             # Defines the data schemas (Mongoose models)
├── routes/             # Defines API routes for books and authentication
├── services/           # Business logic for interacting with the database
├── middlewares/        # Custom middleware for validation
├── validations/        # Input validation schemas
├── db/                 # MongoDB connection setup
├── server.js           # Main server file
├── package.json        # Project metadata and dependencies
└── vercel.json         # Configuration file for Vercel deployment

## Prerequisites
Make sure you have the following installed:

Node.js (v14 or higher)
MongoDB (either local or MongoDB Atlas)
Vercel CLI (for deployment)
Installation
Clone the repository:

git clone https://github.com/rjparsana/book-store-main.git
cd book-store-main
Install dependencies:

npm install
Set up MongoDB connection:

Create a .env file in the root directory and add your MongoDB connection string:

MONGODB_URI=mongodb+srv://rjparsana8:0VeJHpbUmW0eab61@cluster0.szmjg.mongodb.net/?retryWrites=true&w=majority&appName=Cluster0
JWT_SECRET=rj_secret

Start the server:
node server.js
The API will now run at http://localhost:5000.

API Endpoints
Authentication
Register: POST /api/auth/register
Login: POST /api/auth/login

Book Management
Get All Books: GET /api/books/get
Add a Book: POST /api/books/add
Update a Book: PUT /api/books/update/:id
Delete a Book: DELETE /api/books/delete/:id

Borrow/Return Books
Borrow a Book: PUT /api/books/borrow/:id
Return a Book: PUT /api/books/return/:id
Error Handling
If any errors occur during the request (e.g., missing fields or invalid IDs), the API will return an error message with a status code of 400.

Example error response:

json
Copy code
{
  "success": false,
  "message": "Error message here"
}
Deployment
To deploy this API using Vercel:
