# SIT313 P4 – Login and Registration Page

## Overview

This project extends the DEV@Deakin web application by implementing user login and registration functionality. It uses React to build the frontend and Firebase to authenticate users and store their additional details.

## Features

- User login using email and password.
- New user registration with first name, last name, email and password.
- Firebase Authentication for account management.
- Cloud Firestore for storing user profile details.
- React Router for navigation between pages.
- Shared navigation bar and footer across pages.
- Form validation and error messages.
- Responsive and user-friendly interface.

## Technologies Used

- React
- JavaScript and JSX
- CSS
- React Router
- Firebase Authentication
- Cloud Firestore
- Vite
- Git and GitHub

## Project Structure

```text
src/
├── components/
│   ├── Header.jsx
│   ├── Footer.jsx
│   ├── FeaturedArticles.jsx
│   └── FeaturedTutorials.jsx
├── pages/
│   ├── Login.jsx
│   ├── Register.jsx
│   └── Auth.css
├── firebase.js
├── App.jsx
├── App.css
└── main.jsx

.env
.gitignore
package.json
README.md
```

## Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/Shivamsingla-dev/SIT313-P4.git
cd SIT313-P4
```

### 2. Install Dependencies

```bash
npm install
npm install firebase react-router-dom
```

### 3. Configure Firebase

Create a `.env` file in the root directory and add your Firebase web app configuration:

```env
VITE_FIREBASE_API_KEY=your_api_key
VITE_FIREBASE_AUTH_DOMAIN=your_auth_domain
VITE_FIREBASE_PROJECT_ID=your_project_id
VITE_FIREBASE_STORAGE_BUCKET=your_storage_bucket
VITE_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
VITE_FIREBASE_APP_ID=your_app_id
```

Replace the placeholder values with your own Firebase configuration. Enable Email/Password authentication and create a Cloud Firestore database in the Firebase Console.

### 4. Run the Application

```bash
npm run dev
```

Open the local URL displayed in the terminal to access the application.

## Application Routes

| Route | Description |
|---|---|
| `/` | DEV@Deakin homepage |
| `/login` | User login page |
| `/register` | New user registration page |

## Firebase Integration

Firebase Authentication handles account creation and login. Additional user details, including first name, last name, email address and account creation timestamp, are stored in the Firestore `users` collection. Each user document is identified by the authenticated user's UID.

Firestore Security Rules are used to restrict access to each user's own document.

## Testing

The application can be tested by checking the homepage navigation, opening the login and registration pages, creating a test account, logging in with valid credentials, and verifying the saved account and profile details in Firebase.

## Security Notes

- The `.env` file must not be committed to GitHub.
- Keep service-account private keys and other confidential credentials out of frontend code.
- Configure Firestore Security Rules to prevent unauthorised access to user data.
- Do not store passwords directly in Firestore; Firebase Authentication manages them.

## Author

SIT313 Secure Frontend Applications

**Project:** P4 – Login and Registration Page
