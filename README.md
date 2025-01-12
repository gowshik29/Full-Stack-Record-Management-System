Full-Stack Contact Management App

This project is a basic full-stack CRUD (Create, Read, Update, Delete) application designed to manage a list of contacts. It showcases how to integrate a Python Flask backend with a React frontend, emphasizing separation of concerns and clean API design.

Features

Backend: Developed using Flask, the backend provides RESTful API endpoints to handle CRUD operations for contact management.

Frontend: Built using React, the frontend consumes the backend API to display and interact with contact data.

Database: Persistent storage is implemented using MySQL, with SQL Workbench used for managing the database schema and data.

CRUD Operations:

Create: Add new contacts with fields like name and email.

Read: View a list of all existing contacts.

Update: Edit details of an existing contact.

Delete: Remove contacts from the database.

Prerequisites

Backend

Python 3.7+

Flask

Flask-SQLAlchemy

Flask-CORS

MySQL server and SQL Workbench

Frontend

Node.js

npm or yarn

Getting Started

Backend Setup

Clone the repository and navigate to the backend directory:

cd backend

Install the required Python packages:

pip install flask flask-sqlalchemy flask-cors

Configure your MySQL database connection in config.py:

app.config['SQLALCHEMY_DATABASE_URI'] = 'mysql+pymysql://username:password@localhost/db_name'

Run the Flask server:

python main.py

The backend will start running on http://127.0.0.1:5000.

Frontend Setup

Navigate to the frontend directory:

cd frontend

Install dependencies:

npm install

Start the React development server:

npm run dev

The frontend will start running on http://127.0.0.1:5173 (port may vary).

API Endpoints

Base URL

http://127.0.0.1:5000

Endpoints

Get All Contacts

GET /contacts

Response: A list of all contacts.

Create Contact

POST /create_contact

Request Body:

{
  "firstName": "John",
  "lastName": "Doe",
  "email": "john.doe@example.com"
}

Update Contact

PATCH /update_contact/<id>

Request Body:

{
  "firstName": "Jane",
  "lastName": "Smith",
  "email": "jane.smith@example.com"
}

Delete Contact

DELETE /delete_contact/<id>

Project Structure

Backend

main.py: Entry point of the Flask application.

models.py: Defines the database schema using SQLAlchemy.

config.py: Configuration file for the Flask application.

Frontend

src/

App.jsx: Main React component.

components/: Contains reusable React components like ContactList and ContactForm.

styles/: Contains CSS files for styling the application.

Usage

Launch the backend server by running main.py.

Start the React frontend using npm run dev.

Open the frontend in your browser and interact with the contact list:

Add new contacts using the form.

View and update existing contacts.

Delete contacts as needed.

Future Enhancements

Add user authentication for secure access.

Implement pagination for large contact lists.

Enhance UI/UX with additional styling frameworks like Material-UI or Tailwind CSS.

Deploy the app to a production environment using tools like Docker or Heroku.
