# Instadream - Backend

This directory contains the server-side code for the Instadream application. It's a Node.js application that uses Express.js and Apollo Server to provide a comprehensive GraphQL API.

## Features

-   **GraphQL API**: Exposes queries and mutations for users, publications, and follows.
-   **Authentication**: Handles user registration and login with JWT.
-   **Database**: Connects to MongoDB using Mongoose for data modeling and persistence.
-   **File Uploads**: Manages avatar and publication content uploads using Multer.
-   **Middleware**: Includes authorization middleware to protect routes and GraphQL resolvers.

## Environment Variables

To run the backend server, you need to create a `.env` file in this directory with the following variables:

-   `DATABASE_URL`: The connection string for your MongoDB database.
-   `SECRET_KEY`: A secret string used for signing JWTs.
-   `PORT`: The port on which the Express server will run (defaults to 3000).
-   `TOKEN_EXPIRATION`: The expiration time for JWTs (e.g., `24h`, `7d`).

Example `.env` file:

```env
DATABASE_URL=mongodb://localhost:27017/instadream
SECRET_KEY=your-very-strong-secret
PORT=3000
TOKEN_EXPIRATION=24h
```

## Getting Started

1.  **Install dependencies:**
    ```sh
    npm install
    ```
2.  **Set up your `.env` file** as described above.
3.  **Run the development server:**
    ```sh
    npm run dev
    ```

The GraphQL Playground will be available at `http://localhost:3000/graphql`.
