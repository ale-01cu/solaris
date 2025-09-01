# Solaris

Solaris is a full-stack web application inspired by Instagram, built with a modern technology stack. It features a complete backend API using Node.js and GraphQL, and a responsive frontend client built with React and NextUI.

## Features

### Backend

-   **User Authentication**: Secure user registration and login using JSON Web Tokens (JWT).
-   **Profile Management**: Users can view and update their profiles, including uploading and deleting avatars.
-   **Follow System**: Functionality for users to follow and unfollow each other.
-   **Publications**: Full CRUD (Create, Read, Update, Delete) operations for user posts, including image and video uploads.
-   **GraphQL API**: A comprehensive API built with Apollo Server, providing endpoints for all application features.
-   **Search**: Efficient user search functionality with pagination.

### Frontend

-   **Responsive Design**: A complete user interface built with NextUI and Tailwind CSS that works on all screen sizes.
-   **User Authentication**: Login and registration forms with validation.
-   **Dynamic Home Feed**: An infinite-scrolling feed that displays all user publications.
-   **User Profiles**: View user profiles, their publications, and their follower/following counts.
-   **Interactive Modals**: Modals for creating publications, editing profiles, changing avatars, and viewing followers/following lists.
-   **User Search**: Real-time user search with recent search history stored locally using IndexedDB.
-   **Dark Mode**: Toggle between light and dark themes.
-   **State Management**: Efficient state management using Apollo Client and React Hooks.

## Tech Stack

### Backend

-   **Runtime**: Node.js
-   **Framework**: Express.js
-   **API**: Apollo Server (GraphQL)
-   **Database**: MongoDB with Mongoose
-   **Authentication**: JSON Web Token (JWT), bcryptjs
-   **File Uploads**: Multer, fs-extra

### Frontend

-   **Framework**: React
-   **Build Tool**: Vite
-   **UI Library**: NextUI, Tailwind CSS
-   **State Management**: Apollo Client, React Context
-   **Routing**: React Router
-   **Form Handling**: Formik, Yup
-   **Local Storage**: IndexedDB

## Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

-   Node.js (v20.9.0 recommended)
-   npm or yarn
-   MongoDB instance (local or cloud)

### Backend Setup

1.  **Navigate to the backend directory:**
    ```sh
    cd backend
    ```
2.  **Install NPM packages:**
    ```sh
    npm install
    ```
3.  **Create a `.env` file** in the `backend` root and add the following environment variables:
    ```env
    # Your MongoDB connection string
    DATABASE_URL=mongodb+srv://<user>:<password>@<cluster-address>/<database-name>

    # A strong secret key for signing JWTs
    SECRET_KEY=your_super_secret_key

    # The port for the server to run on
    PORT=3000

    # Token expiration time (e.g., 24h, 7d)
    TOKEN_EXPIRATION=24h
    ```
4.  **Start the server:**
    ```sh
    npm run dev
    ```
    The server will be running at `http://localhost:3000`.

### Frontend Setup

1.  **Navigate to the frontend directory:**
    ```sh
    cd frontend
    ```
2.  **Install NPM packages:**
    ```sh
    npm install
    ```
3.  **Start the development server:**
    ```sh
    npm run dev
    ```
    The application will be available at `http://localhost:5173` (or another port if 5173 is in use).

## Folder Structure

The project is organized into two main directories: `backend` and `frontend`.

```
.
├── backend/         # Node.js, Express, GraphQL API
│   ├── config/      # Database connection, environment variables
│   ├── src/         # Source code
│   │   ├── follow/
│   │   ├── publication/
│   │   └── user/
│   └── app.js       # Main server entry point
│
└── frontend/        # React, Vite, NextUI client
    ├── src/
    │   ├── assets/
    │   ├── components/
    │   ├── config/
    │   ├── contexts/
    │   ├── gql/
    │   ├── hooks/
    │   ├── layouts/
    │   ├── pages/
    │   ├── routes/
    │   ├── services/
    │   └── utils/
    └── index.html   # Main HTML entry point
```