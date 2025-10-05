# The Wheel Decides - Complete Project

A full-stack gamified giveaway platform with wheel spinning mechanics, user management, and store integration.

## 🎯 Project Overview

**The Wheel Decides** is a complete web application that allows users to participate in a wheel-based giveaway system. Users can register, purchase items to increase their wheel entries, and participate in real-time wheel spins. SuperAdmins can manage the game, trigger spins, and declare winners.

## 🏗️ Architecture

- **Frontend**: Next.js 14 with TypeScript, Tailwind CSS, and Radix UI
- **Backend**: Node.js with Express.js and MongoDB
- **Database**: MongoDB Atlas
- **Authentication**: JWT-based authentication
- **Real-time**: Socket.io for live updates
- **Documentation**: Swagger/OpenAPI

## 📁 Project Structure

```
TheWheelDecides/
├── backend/                 # Backend API
│   ├── models/             # Database models
│   ├── routes/             # API routes
│   ├── middleware/         # Authentication middleware
│   ├── utils/              # Utility functions
│   ├── server.js           # Main server file
│   └── package.json        # Backend dependencies
├── TheWheelDecides-main/   # Frontend application
│   ├── app/                # Next.js app directory
│   ├── components/         # React components
│   ├── lib/                # API service and utilities
│   └── package.json        # Frontend dependencies
└── README.md               # This file
```

## 🚀 Quick Start

### Prerequisites

- Node.js (v18 or higher)
- MongoDB Atlas account
- Git

### Backend Setup

1. **Navigate to backend directory**
   ```bash
   cd backend
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Setup environment**
   ```bash
   npm run setup
   ```

4. **Initialize database**
   ```bash
   npm run init-data
   ```

5. **Start backend server**
   ```bash
   npm start
   ```

The backend will be running on `http://localhost:5000`

### Frontend Setup

1. **Navigate to frontend directory**
   ```bash
   cd TheWheelDecides-main
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Setup environment**
   ```bash
   npm run setup
   ```

4. **Start frontend development server**
   ```bash
   npm run dev
   ```

The frontend will be running on `http://localhost:3000`

## 🎮 Features

### User Features
- **Registration & Authentication**: Secure user registration and login
- **Dashboard**: Personal dashboard with statistics and wheel status
- **Store**: Purchase items to increase wheel entries
- **Game Status**: View leaderboard and recent winners
- **Profile Management**: Update personal information
- **Real-time Updates**: Live wheel spinning and winner announcements

### SuperAdmin Features
- **Admin Dashboard**: Complete game management interface
- **User Management**: View, block/unblock users, manage entries
- **Wheel Control**: Manual spin triggering and winner declaration
- **Game Settings**: Configure timer, auto-spin, and maintenance mode
- **Statistics**: Real-time game statistics and monitoring
- **Store Management**: Add, edit, and manage store items

### Technical Features
- **JWT Authentication**: Secure token-based authentication
- **Role-based Access Control**: Different permissions for users and admins
- **Real-time Communication**: Socket.io for live updates
- **Database Integration**: MongoDB with Mongoose ODM
- **API Documentation**: Swagger/OpenAPI documentation
- **Responsive Design**: Mobile-first responsive UI
- **Error Handling**: Comprehensive error handling and validation

## 📚 API Documentation

Once the backend is running, visit `http://localhost:5000/api/docs` for interactive Swagger documentation.

### Key API Endpoints

#### Authentication
- `POST /auth/signup` - User registration
- `POST /auth/signin` - User login
- `GET /auth/me` - Get current user profile

#### Wheel Management
- `GET /wheel/entries` - Get all wheel entries
- `POST /wheel/spin` - Trigger manual spin (SuperAdmin)
- `GET /wheel/latest-winner` - Get latest winner
- `GET /wheel/check-winner` - Check if current user is winner

#### Store
- `GET /store/items` - Get all store items
- `POST /store/purchase` - Purchase items
- `GET /store/purchases` - Get user's purchase history

#### Admin
- `GET /admin/dashboard` - Get admin dashboard data
- `PUT /admin/settings` - Update game settings
- `GET /admin/users` - Get all users
- `POST /admin/declare-winner` - Manually declare winner

## 🎯 User Flow

1. **Registration**: Users visit the main page and register with their details
2. **Dashboard**: After registration, users see their dashboard with statistics
3. **Store**: Users can purchase items to increase their wheel entries
4. **Wheel Spinning**: The wheel spins automatically or manually by admin
5. **Winner Announcement**: Winners are announced in real-time
6. **Admin Management**: SuperAdmins can manage the entire game system

## 🛠️ Development

### Backend Development
- Uses Express.js with middleware for authentication and validation
- MongoDB with Mongoose for database operations
- Socket.io for real-time communication
- JWT for secure authentication
- Swagger for API documentation

### Frontend Development
- Next.js 14 with App Router
- TypeScript for type safety
- Tailwind CSS for styling
- Radix UI for accessible components
- Custom API service for backend communication

### Database Models
- **User**: User accounts with roles and statistics
- **WheelEntry**: Individual wheel entries tracking
- **Spin**: Spin records with winner information
- **Winner**: Winner records with prize details
- **Store**: Store items with pricing and entry values
- **Purchase**: Purchase records with entry calculations
- **GameSettings**: Configurable game parameters

## 🔧 Configuration

### Backend Configuration
The backend uses environment variables for configuration. The setup script creates a `.env` file with the correct MongoDB credentials and JWT secrets.

### Frontend Configuration
The frontend uses `.env.local` for API URL configuration. The setup script creates this file automatically.

## 📱 Mobile Support

The application is fully responsive and optimized for mobile devices with:
- Mobile-first design approach
- Touch-friendly interface
- Bottom navigation for mobile users
- Responsive grid layouts

## 🚀 Deployment

### Backend Deployment
1. Set up MongoDB Atlas cluster
2. Configure environment variables for production
3. Deploy to your preferred hosting platform (Heroku, Railway, etc.)

### Frontend Deployment
1. Build the application: `npm run build`
2. Deploy to Vercel, Netlify, or your preferred platform
3. Update API URL in environment variables

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📄 License

This project is licensed under the ISC License.

## 🆘 Support

For support or questions, please check the API documentation or create an issue in the repository.

---

**The Wheel Decides** - Where luck meets strategy! 🎰✨
