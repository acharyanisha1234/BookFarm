# 📚 BookFarm - Library Management System

A modern, full-stack library management system built with React.js frontend and Express.js backend, featuring a beautiful dark-themed UI and comprehensive functionality for both librarians and borrowers.

## ✨ Features

### 🔐 Authentication & User Management
- **User Registration & Login**: Secure authentication with JWT tokens
- **Role-Based Access Control**: Separate interfaces for librarians and borrowers
- **User Profiles**: Customizable user profiles with reading preferences

### 📖 Book Management
- **Comprehensive Book Database**: Store books with detailed metadata (title, author, ISBN, genre, etc.)
- **Search & Filtering**: Advanced search with genre, availability, and recommendation filters
- **Inventory Management**: Track total copies and available copies
- **Book Recommendations**: AI-powered book suggestions for users

### 📚 Borrowing System
- **Book Borrowing**: Easy book checkout process
- **Due Date Management**: Automatic overdue tracking and fine calculation
- **Return Processing**: Streamlined book return workflow
- **Borrowing History**: Complete record of user borrowing activities

### 📊 Dashboard & Analytics
- **Librarian Dashboard**: Comprehensive statistics and insights
- **Borrower Dashboard**: Personal reading statistics and recommendations
- **Real-time Analytics**: Live updates on library usage and trends
- **Monthly Reports**: Detailed monthly borrowing and book addition statistics

### 🎨 Modern UI/UX
- **Dark Theme**: Eye-pleasing dark color scheme
- **Responsive Design**: Mobile-first responsive layout
- **Interactive Components**: Smooth animations and transitions
- **Accessibility**: WCAG compliant design patterns

## 🛠️ Tech Stack

### Frontend
- **React 18** - Modern React with hooks and functional components
- **Tailwind CSS** - Utility-first CSS framework with custom dark theme
- **React Router** - Client-side routing
- **React Query** - Server state management and caching
- **React Hook Form** - Form handling and validation
- **Lucide React** - Beautiful icon library
- **Recharts** - Data visualization charts

### Backend
- **Node.js** - JavaScript runtime
- **Express.js** - Web application framework
- **MongoDB** - NoSQL database with Mongoose ODM
- **JWT** - JSON Web Token authentication
- **bcryptjs** - Password hashing
- **Express Validator** - Input validation and sanitization
- **Helmet** - Security middleware
- **CORS** - Cross-origin resource sharing

## 🚀 Getting Started

### Prerequisites
- Node.js (v16 or higher)
- MongoDB (local or cloud instance)
- npm or yarn package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/bookfarm.git
   cd bookfarm
   ```

2. **Install Backend Dependencies**
   ```bash
   cd backend
   npm install
   ```

3. **Install Frontend Dependencies**
   ```bash
   cd ../frontend
   npm install
   ```

4. **Environment Configuration**
   
   Create a `.env` file in the backend directory:
   ```env
   PORT=5000
   MONGODB_URI=mongodb://localhost:27017/bookfarm
   JWT_SECRET=your_super_secret_jwt_key_here
   NODE_ENV=development
   ```

5. **Start the Backend**
   ```bash
   cd backend
   npm run dev
   ```

6. **Start the Frontend**
   ```bash
   cd frontend
   npm start
   ```

7. **Access the Application**
   - Frontend: http://localhost:3000
   - Backend API: http://localhost:5000

## 📁 Project Structure

```
BookFarm/
├── backend/                 # Express.js backend
│   ├── config/             # Database configuration
│   ├── middleware/         # Authentication middleware
│   ├── models/             # MongoDB schemas
│   ├── routes/             # API endpoints
│   ├── server.js           # Main server file
│   └── package.json        # Backend dependencies
├── frontend/               # React.js frontend
│   ├── public/             # Static assets
│   ├── src/                # Source code
│   │   ├── components/     # Reusable components
│   │   ├── contexts/       # React contexts
│   │   ├── pages/          # Page components
│   │   ├── services/       # API services
│   │   └── App.js          # Main app component
│   └── package.json        # Frontend dependencies
└── README.md               # Project documentation
```

## 🔧 API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `GET /api/auth/me` - Get current user profile
- `PUT /api/auth/profile` - Update user profile

### Books
- `GET /api/books` - Get all books with filtering
- `GET /api/books/:id` - Get book by ID
- `POST /api/books` - Create new book (Librarian only)
- `PUT /api/books/:id` - Update book (Librarian only)
- `DELETE /api/books/:id` - Delete book (Librarian only)

### Borrows
- `POST /api/borrows` - Borrow a book
- `GET /api/borrows` - Get borrows with filtering
- `PUT /api/borrows/:id/return` - Return a book
- `PUT /api/borrows/:id/extend` - Extend due date

### Statistics
- `GET /api/stats/dashboard` - Get dashboard statistics
- `GET /api/stats/books` - Get book statistics
- `GET /api/stats/users` - Get user statistics

## 👥 User Roles

### Librarian
- Full access to all books and users
- Can add, edit, and delete books
- Manage user accounts and borrowing records
- View comprehensive analytics and reports
- Process book returns and extensions

### Borrower
- Browse and search available books
- Borrow and return books
- View personal borrowing history
- Receive book recommendations
- Update personal profile and preferences

## 🎨 UI Components

- **Responsive Layout**: Sidebar navigation with mobile support
- **Card Components**: Beautiful card designs for content display
- **Form Components**: Styled form inputs with validation
- **Data Tables**: Sortable and filterable data tables
- **Charts & Graphs**: Interactive data visualization
- **Modal Dialogs**: Overlay components for user interactions
- **Loading States**: Smooth loading animations and spinners

## 🔒 Security Features

- **JWT Authentication**: Secure token-based authentication
- **Password Hashing**: bcrypt password encryption
- **Input Validation**: Comprehensive input sanitization
- **CORS Protection**: Cross-origin request security
- **Helmet Security**: HTTP header security
- **Role-Based Access**: Granular permission control

## 📱 Responsive Design

- **Mobile First**: Optimized for mobile devices
- **Tablet Support**: Responsive layout for tablets
- **Desktop Experience**: Full-featured desktop interface
- **Touch Friendly**: Optimized touch interactions

## 🚀 Deployment

### Backend Deployment
1. Set environment variables for production
2. Use PM2 or similar process manager
3. Configure MongoDB connection
4. Set up reverse proxy (Nginx)

### Frontend Deployment
1. Build the production bundle: `npm run build`
2. Deploy to static hosting (Netlify, Vercel, etc.)
3. Configure API endpoint URLs
4. Set up custom domain if needed

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Commit changes: `git commit -am 'Add feature'`
4. Push to branch: `git push origin feature-name`
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **React Team** - For the amazing frontend framework
- **Express.js Team** - For the robust backend framework
- **Tailwind CSS** - For the utility-first CSS framework
- **MongoDB** - For the flexible NoSQL database
- **Open Source Community** - For the amazing libraries and tools

## 📞 Support

If you have any questions or need help:
- Create an issue in the GitHub repository
- Contact the development team
- Check the documentation

---

**Made with ❤️ by the BookFarm Team** 