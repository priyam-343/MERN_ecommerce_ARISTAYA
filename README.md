ARISTAYA E-commerce Platform
The ARISTAYA E-commerce Platform is a complete e-commerce solution with a powerful backend and a user-friendly frontend. It’s designed to handle everything from user authentication and product management to secure payments and detailed analytics.

Key Features
User and Admin Authentication: The platform uses secure JWT-based authentication for both regular users and administrators. It also supports email verification via Firebase and Google Sign-In for easy registration and login.

Comprehensive Admin Controls: A dedicated admin dashboard gives administrators extensive control over the platform. They can manage products, users, orders, and reviews. A unique feature is the ability for a super-admin to approve new admin registrations, and for admins to toggle free shipping for individual users.

Product Management & Catalog: The backend provides APIs for a dynamic product catalog, allowing users to browse products by type or category. Admins have full CRUD (Create, Read, Update, Delete) capabilities to manage product listings.

Shopping & Wishlist Management: Users can add, remove, and manage items in their shopping carts and wishlists.

Secure Payment Processing: The platform integrates with Razorpay for a secure checkout process. It uses a robust webhook system to ensure transaction statuses are always accurate.

Email Services: The system automatically sends emails for important events like order confirmations, password resets, and new admin approvals using Nodemailer.

Analytics: The admin dashboard provides valuable insights with charts and graphs on revenue trends, order performance, and user activity.

Tech Stack
Backend

Frontend

Node.js

ReactJS

Express.js

Material UI

MongoDB (Mongoose ODM)

ContextAPI

JWT (for authentication)



Bcrypt (for password hashing)



Razorpay (for payments)



Nodemailer (for email)



HTML-PDF (for receipts)



Firebase Admin SDK





React-router-dom

How to Run Locally
To get the ARISTAYA platform running on your local machine, you need to set up both the backend and frontend.

Prerequisites
Node.js & npm (or Yarn)

A MongoDB instance (local or cloud-hosted)

A Razorpay account

A Gmail account (to send emails)

A Firebase project

Backend Setup
Clone the backend repository:

git clone https://github.com/priyam-343/ARISTAYA_backend_ecommerce.git
cd ARISTAYA_backend_ecommerce


Install dependencies:

npm install


Create a .env file in the project root and fill in your details:

PORT=2000
MONGO_URL=YOUR_MONGODB_CONNECTION_STRING
JWT_SECRET=YOUR_JWT_SECRET_KEY
RAZORPAY_API_KEY=YOUR_RAZORPAY_KEY_ID
RAZORPAY_API_SECRET=YOUR_RAZORPAY_KEY_SECRET
RAZORPAY_WEBHOOK_SECRET=YOUR_RAZORPAY_WEBHOOK_SECRET
PAYMENT_SUCCESS=YOUR_FRONTEND_URL/paymentsuccess
EMAIL=YOUR_GMAIL_ADDRESS@gmail.com
EMAIL_PASSWORD=YOUR_GMAIL_APP_PASSWORD
FORGOT_PASSWORD=YOUR_FRONTEND_URL/user/reset
ADMIN_KEY=YOUR_ADMIN_SECRET_KEY
ADMIN_EMAIL=YOUR_SUPER_ADMIN_EMAIL@gmail.com
FRONTEND_URL_1=YOUR_FRONTEND_URL
BACKEND_URL=YOUR_BACKEND_URL
FIREBASE_PROJECT_ID=YOUR_FIREBASE_PROJECT_ID
FIREBASE_ADMIN_SDK_CONFIG={YOUR_FIREBASE_ADMIN_SDK_JSON_CONFIG}


Run the application:

npm start


The backend will start at http://localhost:2000.

Frontend Setup
Clone the frontend repository:

git clone https://github.com/priyam-343/ARISTAYA_frontend_ecommerce.git
cd ARISTAYA_frontend_ecommerce


Install dependencies:

npm install


Create a .env file in the project root and add the following variables. The URLs should point to your running backend instance.

REACT_APP_BACKEND_URL=YOUR_BACKEND_URL
REACT_APP_PRODUCT_TYPE=YOUR_BACKEND_URL/api/product/fetchproduct/type
REACT_APP_PRODUCT_TYPE_CATEGORY_=YOUR_BACKEND_URL/api/product/fetchproduct/category
REACT_APP_ADMIN_LOGIN=YOUR_BACKEND_URL/api/admin/login
REACT_APP_ADMIN_REGISTER=YOUR_BACKEND_URL/api/admin/register
REACT_APP_FORGOT_PASSWORD=YOUR_BACKEND_URL/api/password/forgot-password
REACT_APP_GET_USER_DETAILS=YOUR_BACKEND_URL/api/auth/getuser
REACT_APP_LOGIN=YOUR_BACKEND_URL/api/auth/login
REACT_APP_REGISTER=YOUR_BACKEND_URL/api/auth/register
REACT_APP_UPDATE_USER=YOUR_BACKEND_URL/api/auth/updateuser
REACT_APP_DELETE_USER=YOUR_BACKEND_URL/api/auth/delete/user
REACT_APP_GET_REVIEW=YOUR_BACKEND_URL/api/review/fetchreview
REACT_APP_ADD_REVIEW=YOUR_BACKEND_URL/api/review/addreview
REACT_APP_DELETE_REVIEW=YOUR_BACKEND_URL/api/review/deletereview
REACT_APP_ADMIN_DELETE_REVIEW=YOUR_BACKEND_URL/api/admin/review
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
REACT_APP_ADMIN_ADD_PRODUCT=YOUR_BACKEND_URL/api/admin/addproduct
REACT_APP_ADMIN_GET_ALL_USERS=YOUR_BACKEND_URL/api/admin/getusers
REACT_APP_ADMIN_GET_SINGLE_USER=YOUR_BACKEND_URL/api/admin/getuser
REACT_APP_ADMIN_GET_USER_CART=YOUR_BACKEND_URL/api/admin/getcart
REACT_APP_ADMIN_GET_USER_WISHLIST=YOUR_BACKEND_URL/api/admin/getwishlist
REACT_APP_ADMIN_GET_USER_REVIEW=YOUR_BACKEND_URL/api/admin/getreview
REACT_APP_ADMIN_GET_USER_ORDER=YOUR_BACKEND_URL/api/admin/getorder
REACT_APP_ADMIN_GET_CHART_DATA=YOUR_BACKEND_URL/api/admin/chartdata
REACT_APP_ADMIN_UPDATE_PRODUCT=YOUR_BACKEND_URL/api/admin/updateproduct
REACT_APP_ADMIN_DELETE_USER_CART_ITEM=YOUR_BACKEND_URL/api/admin/usercart
REACT_APP_ADMIN_DELETE_USER_WISHLIST_ITEM=YOUR_BACKEND_URL/api/admin/userwishlist
REACT_APP_ADMIN_DELETE_PRODUCT=YOUR_BACKEND_URL/api/admin/deleteproduct
REACT_APP_ADMIN_DELETE_USER=YOUR_BACKEND_URL/api/admin/deleteuser
REACT_APP_ADMIN_USER_TOGGLE_SHIPPING=YOUR_BACKEND_URL/api/admin/user
REACT_APP_REORDER_API=YOUR_BACKEND_URL/api/payment/reorder
REACT_APP_FIREBASE_API_KEY="YOUR_FIREBASE_API_KEY"
REACT_APP_FIREBASE_AUTH_DOMAIN="YOUR_FIREBASE_AUTH_DOMAIN"
REACT_APP_FIREBASE_PROJECT_ID="YOUR_FIREBASE_PROJECT_ID"
REACT_APP_FIREBASE_STORAGE_BUCKET="YOUR_FIREBASE_STORAGE_BUCKET"
REACT_APP_FIREBASE_MESSAGING_SENDER_ID="YOUR_FIREBASE_MESSAGING_SENDER_ID"
REACT_APP_FIREBASE_APP_ID="YOUR_FIREBASE_APP_ID"
REACT_APP_FIREBASE_MEASUREMENT_ID="YOUR_FIREBASE_MEASUREMENT_ID"


Run the application:

npm start


The application will open in your browser at http://localhost:3000.

Developed by Priyam Kumar.