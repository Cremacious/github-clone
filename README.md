# GitHub Clone

A full-stack GitHub clone application built with modern web technologies, featuring user authentication, repository browsing, and a responsive user interface.

## Technologies Used

### Frontend
- **React 19** - Modern UI library with latest features
- **React Router DOM** - Client-side routing and navigation
- **Vite** - Fast build tool and development server
- **Tailwind CSS** - Utility-first CSS framework for styling
- **React Hot Toast** - Beautiful toast notifications
- **React Icons** - Icon library for UI components

### Backend
- **Node.js** with **Express.js** - Server-side runtime and web framework
- **MongoDB** with **Mongoose** - NoSQL database and ODM
- **Passport.js** with **GitHub OAuth** - Authentication system
- **Express Session** - Session management
- **CORS** - Cross-origin resource sharing

### Development Tools
- **ESLint** - Code linting and formatting
- **Nodemon** - Auto-restart development server
- **PostCSS & Autoprefixer** - CSS processing
- **Vite Plugin React** - React support for Vite

## Features

- GitHub OAuth authentication
- User profile display
- Repository browsing and sorting
- User search functionality
- Responsive design
- Modern UI with Tailwind CSS
- Fast development with Vite

## 🛠️ Installation & Setup

### Prerequisites
- Node.js (v16 or higher)
- MongoDB database
- GitHub OAuth App credentials

### 1. Clone the repository
```bash
git clone https://github.com/Cremacious/github-clone.git
cd github-clone
```

### 2. Install dependencies
```bash
# Install root dependencies
npm install

# Install frontend dependencies
cd frontend
npm install
cd ..
```

### 3. Environment Variables
Create a `.env` file in the root directory:
```env
GITHUB_CLIENT_ID=your_github_client_id
GITHUB_CLIENT_SECRET=your_github_client_secret
MONGO_URI=your_mongodb_connection_string
SESSION_SECRET=your_session_secret
```

### 4. GitHub OAuth Setup
1. Go to GitHub Settings > Developer settings > OAuth Apps
2. Create a new OAuth App
3. Set Authorization callback URL to: `http://localhost:5000/auth/github/callback`
4. Copy Client ID and Client Secret to your `.env` file

## Running the Application

### Development Mode
```bash
# Start both frontend and backend in development mode
npm run dev
```

### Production Build
```bash
# Build the application
npm run build

# Start production server
npm start
```

The application will be available at:
- Frontend: `http://localhost:5173` (development)
- Backend API: `http://localhost:5000`

## Project Structure

```
github-clone/
├── backend/
│   ├── server.js          # Express server setup
│   ├── routes/            # API routes
│   ├── models/            # MongoDB models
│   └── middleware/        # Custom middleware
├── frontend/
│   ├── src/
│   │   ├── components/    # React components
│   │   ├── pages/         # Page components
│   │   ├── context/       # React context
│   │   └── assets/        # Static assets
│   ├── public/            # Public assets
│   └── package.json       # Frontend dependencies
├── package.json           # Root dependencies
└── README.md
```

## API Endpoints

- `GET /api/users/profile/:username` - Get user profile and repositories
- `GET /auth/github` - Initiate GitHub OAuth
- `GET /auth/github/callback` - GitHub OAuth callback
- `GET /auth/logout` - Logout user
- `GET /auth/user` - Get current authenticated user


