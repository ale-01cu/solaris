# Instadream - Frontend

This directory contains the client-side code for the Instadream application, built with React and Vite.

## Features

-   **Component-Based UI**: Built with React and the NextUI component library.
-   **Styling**: Styled with Tailwind CSS for a modern, responsive design.
-   **GraphQL Communication**: Interacts with the backend API using Apollo Client.
-   **Routing**: Client-side routing is handled by React Router.
-   **State Management**: Utilizes React Hooks and Context for managing global state like authentication and dark mode.
-   **Form Handling**: Robust forms with validation using Formik and Yup.
-   **Infinite Scroll**: Efficiently loads paginated data for the home feed and search results.
-   **Local Caching**: Uses IndexedDB to store recent search history.

## Getting Started

1.  **Ensure the backend server is running.**
2.  **Install dependencies:**
    ```sh
    npm install
    ```
3.  **Run the development server:**
    ```sh
    npm run dev
    ```

The application will open in your browser, typically at `http://localhost:5173`.

## Key Dependencies

-   `@apollo/client`: For making GraphQL requests to the backend.
-   `@nextui-org/react`: For the UI component library.
-   `tailwindcss`: For utility-first CSS styling.
-   `react-router-dom`: For handling navigation.
-   `formik` & `yup`: For building and validating forms.
-   `jwt-decode`: For decoding JWTs on the client side.