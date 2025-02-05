# Library Management System

A modern library management system built with React and Node.js that supports barcode scanning for efficient book management.

## Features

### User Features
- Browse available books in the library
- View detailed book information
- Scan books using barcode scanner to borrow
- View currently borrowed books
- View personal borrowing history
- Get notifications for due dates
- Search books by title, author, or category

### Admin Features
- Manage books (add, edit, delete)
- Process book returns via barcode scanning
- Track all transaction history
- Monitor overdue books
- Generate reports
- Manage user accounts
- View system analytics

## User Roles

### Regular Users
1. Book Browsing
   - View all available books
   - Search and filter books
   - View detailed book information

2. Book Borrowing
   - Scan book barcode to borrow
   - Select return date (within policy limits)
   - View borrowed books status
   - Get due date reminders

3. Account Management
   - View personal borrowing history
   - Update profile information
   - View notifications

### Admin Users
1. Book Management
   - Add new books to the system
   - Update book information
   - Remove books from circulation
   - Manage book categories

2. Transaction Management
   - Process book returns via barcode scanning
   - View all transaction history
   - Handle overdue cases
   - Generate transaction reports

3. User Management
   - View all user accounts
   - Manage user roles
   - Handle user issues
   - Monitor user activity

4. System Management
   - View system analytics
   - Configure system settings
   - Manage notifications
   - Generate reports

## Technical Implementation

### Authentication
- JWT-based authentication
- Role-based access control (RBAC)
- Secure password hashing
- Session management

### Barcode Scanning
- Support for multiple barcode formats
- Real-time scanning validation
- Error handling for invalid barcodes
- Scan history logging

### Database Schema
1. Users
   - Basic information
   - Role (user/admin)
   - Account status

2. Books
   - Book details
   - Barcode information
   - Availability status
   - Location information

3. Transactions
   - Borrowing records
   - Return records
   - Due dates
   - Status tracking

4. Categories
   - Book categories
   - Sub-categories
   - Category hierarchy

## API Endpoints

### Public Endpoints
- `POST /api/auth/login`
- `POST /api/auth/register`
- `GET /api/books` (with pagination)
- `GET /api/books/:id`

### User Endpoints
- `GET /api/books/search`
- `POST /api/transactions/borrow`
- `GET /api/transactions/my-books`
- `GET /api/user/profile`

### Admin Endpoints
- `POST /api/books/create`
- `PUT /api/books/update`
- `POST /api/transactions/return`
- `GET /api/transactions/all`
- `GET /api/admin/dashboard`
- `GET /api/admin/reports`

## Security Measures
- Input validation
- XSS protection
- CSRF protection
- Rate limiting
- Data encryption
- Secure headers

## Getting Started

1. Clone the repository
2. Install dependencies
   ```bash
   cd frontend && npm install
   cd ../backend && npm install
   ```

3. Set up environment variables
   ```bash
   cp .env.example .env
   ```

4. Start the development servers
   ```bash
   # Start backend
   cd backend && npm run dev

   # Start frontend
   cd frontend && npm start
   ```

## Contributing
Please read our contributing guidelines before submitting pull requests.

## License
This project is licensed under the MIT License.
