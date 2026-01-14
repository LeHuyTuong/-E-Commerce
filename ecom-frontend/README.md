# E-Commerce Frontend

Modern React application built with Vite, focusing on performance and user experience.

## Technology Stack

*   **Core**: React 18, Vite
*   **State Management**: React Context API (Cart, Auth)
*   **Networking**: Axios (with Interceptors for Auto-Logout on 401)
*   **Styling**: CSS Modules / Vanilla CSS
*   **Notifications**: React Toastify

## Environment Setup

Create a `.env` file in the root directory:

```env
VITE_API_BASE_URL=http://localhost:8080/api
VITE_STRIPE_PUBLIC_KEY=pk_test_...
```

## Project Structure

```
src/
├── api/            # Centralized API definitions (Axios)
├── components/     # Reusable UI components (Buttons, Inputs)
├── context/        # Global State (Auth, Cart)
├── pages/          # Page Views (Login, Checkout, Home)
└── Main.jsx        # Entry point
```

## Security Features

*   **Auto-Logout**: Automatically redirects to login when JWT expires (401 Unauthorized interceptor).
*   **Protected Routes**: `ProtectedRoute` and `SellerRoute` components ensure unauthorized access is blocked at the router level.
