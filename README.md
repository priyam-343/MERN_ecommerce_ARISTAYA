ARISTAYA E-commerce Platform
This document outlines the setup and features for both the frontend and backend of the ARISTAYA E-commerce platform. The platform is a full-stack application with separate repositories for the client-side and server-side components.

ARISTAYA E-commerce Frontend
This is the client-side application for the ARISTAYA E-commerce Platform, built with modern web technologies to provide a rich and responsive user experience.

Features
User Authentication & Authorization: Secure user sessions using JSON Web Tokens (JWT).

Payment Gateway Integration: Seamless checkout process through an integrated payment gateway.

Mail Service Integration: Handles communication for various actions, like password resets.

Forgot & Reset Password: Securely allows users to reset their password.

Product Listing & Search: Browse and search for products with ease.

Product Details & Reviews: View detailed product information and read or leave reviews.

Cart Management: Add, remove, and manage items in your shopping cart.

Order History: Access a comprehensive history of past orders.

Tech Stack
ReactJS: A JavaScript library for building user interfaces.

Material UI: A popular React UI framework for a polished, modern look.

Context API: State management for the application.

React-router-dom: Handles client-side routing.

How to Run Locally
1. Prerequisites
Node.js & npm (or Yarn)

A running instance of the ARISTAYA E-commerce Backend

2. Installation
First, clone the repository and install the necessary dependencies:

git clone https://github.com/priyam-343/ARISTAYA_frontend_ecommerce.git
cd ARISTAYA_frontend_ecommerce
npm install

3. Environment Variables
Create a .env file in the project's root directory and populate it with the following, replacing YOUR_BACKEND_URL with the URL of your running backend instance.

REACT_APP_BACKEND_URL=YOUR_BACKEND_URL
REACT_APP_PRODUCT_TYPE=YOUR_BACKEND_URL/api/product/fetchproduct/type
REACT_APP_PRODUCT_TYPE_CATEGORY_=YOUR_BACKEND_URL/api/product/fetchproduct/category
REACT_APP_FORGOT_PASSWORD=YOUR_BACKEND_URL/api/password/forgot-password
REACT_APP_GET_USER_DETAILS=YOUR_BACKEND_URL/api/auth/getuser
REACT_APP_LOGIN=YOUR_BACKEND_URL/api/auth/login
REACT_APP_REGISTER=YOUR_BACKEND_URL/api/auth/register
REACT_APP_UPDATE_USER=YOUR_BACKEND_URL/api/auth/updateuser
REACT_APP_DELETE_USER=YOUR_BACKEND_URL/api/auth/delete/user
REACT_APP_GET_REVIEW=YOUR_BACKEND_URL/api/review/fetchreview
REACT_APP_ADD_REVIEW=YOUR_BACKEND_URL/api/review/addreview
REACT_APP_DELETE_REVIEW=YOUR_BACKEND_URL/api/review/deletereview
REACT_APP_EDIT_REVIEW=YOUR_BACKEND_URL/api/review/editreview
REACT_APP_GET_KEY=YOUR_BACKEND_URL/api/payment/getkey
REACT_APP_GET_CHECKOUT=YOUR_BACKEND_URL/api/payment/checkout
REACT_APP_GET_PAYMENTVERIFICATION=YOUR_BACKEND_URL/api/payment/paymentverification
REACT_APP_GET_PREVIOUS_ORDERS=YOUR_BACKEND_URL/api/payment/getPreviousOrders
REACT_APP_GET_PAYMENT_DETAILS=YOUR_BACKEND_URL/api/payment/getpaymentdetails
REACT_APP_FETCH_PRODUCT=YOUR_BACKEND_URL/api/product/fetchproduct
REACT_APP_GET_CART=YOUR_BACKEND_URL/api/cart/fetchcart
REACT_APP_GET_WISHLIST=YOUR_BACKEND_URL/api/wishlist/fetchwishlist
REACT_APP_ADD_CART=YOUR_BACKEND_URL/api/cart/addcart
REACT_APP_DELETE_FROM_CART=YOUR_BACKEND_URL/api/cart/deletecart
REACT_APP_ADD_WISHLIST=YOUR_BACKEND_URL/api/wishlist/addwishlist
REACT_APP_DELETE_WISHLIST=YOUR_BACKEND_URL/api/wishlist/deletewishlist
REACT_APP_RESET_PASSWORD=YOUR_BACKEND_URL/api/password/reset/password

4. Run Application
Start the development server:

npm start

The application will be accessible at http://localhost:3000.

ARISTAYA E-commerce Backend
This is the server-side API for the ARISTAYA E-commerce platform, handling all data processing and business logic.

Features
User Management: Securely handles user authentication and authorization using JWT.

Product Management: Provides full Create, Read, Update, and Delete (CRUD) functionality for products.

Order Processing: Manages the checkout flow, order history, and payment details.

Admin Dashboard APIs: Provides data for an administrative interface.

Payment Gateway Integration: Integrates with Razorpay for secure payments.

Mail Service: Uses Nodemailer to send transactional emails.

Forgot & Reset Password: Backend logic for securely resetting passwords.

Cart & Wishlist Management: Manages a user's shopping cart and wishlist items.

Product Reviews: Allows users to add, edit, and delete product reviews.

Tech Stack
NodeJS: A JavaScript runtime for server-side development.

ExpressJS: A fast and minimalist web framework for Node.js.

MongoDB (Mongoose): A NoSQL database for storing application data.

JWT: Used for secure authentication.

Razorpay: The chosen payment gateway.

Nodemailer: A module for sending emails from Node.js applications.

How to Run Locally
1. Prerequisites
Node.js & npm (or Yarn)

A running MongoDB instance (local or hosted on MongoDB Atlas)

2. Installation
First, clone the repository and install the dependencies:

git clone https://github.com/priyam-343/ARISTAYA_backend_ecommerce.git
cd ARISTAYA_backend_ecommerce
npm install

3. Environment Variables
Create a .env file in the project's root directory and configure it with your specific details.

PORT=2000
MONGO_URL=your_mongodb_atlas_connection_string
JWT_SECRET=your_jwt_secret_key
RAZORPAY_API_KEY=your_razorpay_api_key
RAZORPAY_API_SECRET=your_razorpay_api_secret
EMAIL=your_email@example.com
EMAIL_PASSWORD=your_email_password
FORGOT_PASSWORD=YOUR_FRONTEND_URL/user/reset
PAYMENT_SUCCESS=YOUR_FRONTEND_URL/paymentsuccess
ADMIN_KEY=your_admin_secret_key
FRONTEND_URL=YOUR_FRONTEND_URL

4. Run Server
Start the server:

npm start

The backend API will be running on http://localhost:2000 (or the port you specified in your .env file).

Developed by Priyam Kumar
