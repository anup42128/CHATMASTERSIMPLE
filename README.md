# ChatMaster

A real-time chat application similar to Instagram's messaging feature, built with Node.js, Express.js, MongoDB, and Socket.IO.

## Features

- User authentication (signup/login)
- Real-time messaging
- User search
- Message notifications
- Conversation history
- Modern and clean UI

## Prerequisites

- Node.js (v14 or higher)
- MongoDB
- npm or yarn

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd chatmaster
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file in the root directory with the following variables:
```
MONGODB_URI=mongodb://localhost:27017/chatmaster
JWT_SECRET=your-secret-key
PORT=3000
```

## Running the Application

1. Start MongoDB:
```bash
mongod
```

2. Start the application:
```bash
npm start
```

For development with auto-reload:
```bash
npm run dev
```

The application will be available at `http://localhost:3000`

## Project Structure

```
chatmaster/
├── client/
│   ├── login.html
│   ├── signup.html
│   └── app.html
├── server/
│   ├── models/
│   │   ├── User.js
│   │   └── Message.js
│   ├── routes/
│   │   ├── auth.js
│   │   ├── users.js
│   │   └── messages.js
│   └── server.js
├── package.json
└── README.md
```

## API Endpoints

### Authentication
- POST `/api/auth/signup` - Create a new user account
- POST `/api/auth/login` - Login to existing account

### Users
- GET `/api/users/search` - Search for users
- GET `/api/users/profile` - Get current user profile

### Messages
- GET `/api/messages/conversations` - Get all conversations
- GET `/api/messages/conversation/:userId` - Get conversation with specific user
- PUT `/api/messages/read/:userId` - Mark messages as read

## Technologies Used

- Frontend:
  - HTML5
  - CSS3
  - Vanilla JavaScript
  - Socket.IO Client

- Backend:
  - Node.js
  - Express.js
  - MongoDB with Mongoose
  - Socket.IO
  - JWT for authentication

## Security Features

- Password hashing with bcrypt
- JWT-based authentication
- CORS enabled
- Input validation
- Secure password storage

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License. 