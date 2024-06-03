# e-com-app

Welcome to the back end of the eCommerce site developed for Fullstack Solutions' client. This README.md provides instructions for setting up the project locally and any necessary environment variables.

## Local Setup

To run this project locally, follow these steps:

1. **Clone the Repository**:
   git clone <repository-url>

2. **Install Dependencies**:
   cd e-com-app
   npm install

3. **Set Up Environment Variables**:
   Create a `.env` file in the root directory of the project and add the following environment variables:

**//THESE WILL NEED CHANGED WHEN DATA IS AVAILBE//**

-PORT=<port-number>
-DATABASE_URL=<database-connection-url>
-SECRET_KEY=<secret-key-for-authentication>

4. **Database Setup**:
   Make sure you have the necessary database set up and running. If you're using PostgreSQL, you can create a database using the following command:
   createdb <e-com-app>

5. **Run Migrations**:
   npm run migrate

6. **Start the Server**:
   npm start

7. **Access the API**:
   Once the server is running, you can access the API endpoints at `http://localhost:<port-number>`

## Environment Variables

- `PORT`: The port number on which the server will run.
- `DATABASE_URL`: The connection URL for your database.
- `SECRET_KEY`: A secret key used for authentication and session management.

## Feedback and Improvements

After reviewing the back end, please provide any feedback or suggestions for improvement. We will incorporate your feedback before starting work on the front end.

## Contact

If you have any questions or need further assistance, please contact Jbaumil07@gmail.com

**Database Schema** =

**Users Table:**
-user_id (Primary Key)
-username
-email
-password
-address
-phone_number

**Products Table:**
-product_id (Primary Key)
-name
-description
-price
-quantity_available
-category_id (Foreign Key referencing Categories Table)

**Categories Table:**
-category_id (Primary Key)
-name

**Orders Table:**
-order_id (Primary Key)
-user_id (Foreign Key referencing Users Table)
-order_date
-total_amount

**Order_Details Table:**
-order_detail_id (Primary Key)
-order_id (Foreign Key referencing Orders Table)
-product_id (Foreign Key referencing Products Table)
-quantity
-unit_price
