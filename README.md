# E-Shopper E-commerce Platform

A modern e-commerce platform built with the MERN stack (MongoDB, Express.js, React.js, Node.js) featuring a complete shopping experience with user authentication, product management, shopping cart, and secure payment processing.

## Features

### User Features
- User registration and authentication
- Product browsing and searching
- Product filtering and sorting
- Shopping cart management
- Secure checkout process with Stripe integration
- Order tracking and history
- Contact form for customer support

### Admin Features
- Product management (CRUD operations)
- Order management
- Customer message management
- Sales tracking

## Tech Stack

### Frontend
- React.js
- React Router for navigation
- Bootstrap for styling
- Stripe.js for payment processing
- Axios for API requests

### Backend
- Node.js
- Express.js
- MongoDB with Mongoose
- JWT for authentication
- Stripe API for payments

## Prerequisites

Before running this project, make sure you have:
- Node.js (v14 or higher)
- MongoDB
- Stripe account for payment processing

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd eshopper
```

2. Install dependencies:
```bash
# Install server dependencies
npm install

# Install client dependencies
cd client
npm install
```

3. Configure environment variables:
Create a `.env` file in the root directory with the following variables:
```
MONGO_URI=your_mongodb_connection_string
STRIPE_SECRET_KEY=your_stripe_secret_key
JWT_SECRET=your_jwt_secret
```

4. Start the development server:
```bash
# Start backend server
npm run server

# Start frontend development server
npm run client
```

## Project Structure

```
eshopper/
├── client/                 # Frontend React application
│   ├── public/
│   └── src/
│       ├── components/     # Reusable components
│       ├── pages/         # Page components
│       ├── context/       # React context
│       └── utils/         # Utility functions
├── server/                # Backend Node.js/Express application
│   ├── config/           # Configuration files
│   ├── controllers/      # Route controllers
│   ├── middleware/       # Custom middleware
│   ├── models/          # Mongoose models
│   └── routes/          # API routes
└── package.json
```

## API Endpoints

### Authentication
- POST /api/register - Register a new user
- POST /api/login - User login

### Products
- GET /api/products - Get all products
- GET /api/products/:id - Get single product
- POST /api/products - Create new product (admin)
- PUT /api/products/:id - Update product (admin)
- DELETE /api/products/:id - Delete product (admin)

### Orders
- POST /api/create-payment-intent - Create Stripe payment intent
- POST /api/update-order-status - Update order status
- GET /api/orders - Get user orders

### Contact
- POST /api/contact - Submit contact form

## Database Schema

### User
- name
- email
- password (hashed)
- role

### Product
- name
- description
- price
- offerPrice
- category
- images
- stock

### Order
- orderId
- customerInfo
- orderItems
- paymentInfo
- orderStatus
- orderDate

### Contact
- name
- email
- subject
- message
- status
- createdAt

## Payment Integration

The project uses Stripe for payment processing:
1. Client creates payment intent
2. User enters card details
3. Payment is processed securely
4. Order is created upon successful payment

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support, email support@eshopper.com or use the contact form on the website.

## Acknowledgments

- Bootstrap for the UI components
- Stripe for payment processing
- MongoDB for database
- React community for the amazing framework
