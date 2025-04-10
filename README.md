Library Management System (LMS)
A comprehensive Django-based Library Management System designed to streamline library operations, manage book borrowing, and provide an intuitive user interface for both administrators and patrons.
Features
Core Functionality
📚 Book catalog management (CRUD operations)

👥 User authentication and authorization

🔍 Advanced search and filtering for books

📅 Borrowing/returning system with due dates

🔔 Notifications for overdue books

📊 Dashboard with library statistics

Technical Highlights

🏗 Django MVC architecture

🔒 Secure authentication system

📱 Responsive design (using custom CSS)

🗃 SQLite database (can be configured for other DBs)

🛠 Context processors for global template variables

📝 Form validation for all user inputs
```
Project Structure
  
Smart-Budget-Tracker/
├── .gitignore                 # Git ignore rules
├── package.json               # Node.js project configuration
├── package-lock.json          # Automatic npm dependency tree
├── server.js                  # Main application entry point
├── README.md                  # Project documentation (you're editing this)
│
├── .vscode/                   # VS Code workspace settings
│   └── settings.json          # Editor configuration
│
├── server/                    # Backend server files
│   ├── config/
│   │   └── db.js              # Database connection configuration
│   │
│   ├── controller/            # Business logic
│   │   ├── chartController.js # Chart data handling
│   │   ├── crud.js            # Basic CRUD operations
│   │   ├── mainpageController.js # Main page logic
│   │   ├── mainpageCrud.js    # Main page CRUD
│   │   └── userController.js  # User authentication
│   │
│   └── routes/                # API endpoints
│       └── authRoutes.js      # Authentication routes
│
├── view/                      # Frontend templates (EJS)
│   ├── login.ejs              # Login page template
│   ├── mainpage.ejs           # Dashboard template
│   └── resetPassword.ejs      # Password reset template
│
└── style.css                  # Main stylesheet
```

## 🚀 Installation & Setup

### Prerequisites
- Python 3.8+
- pip
- Virtualenv (recommended)

### Installation Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/Eng-AlaaHosny/Library-Management-System.git
   cd Library-Management-System

   Set up virtual environment:
   python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate


Install dependencies:
pip install -r requirements.txt

Configure environment:
cp .env.example .env
nano .env  # Edit with your configuration


Apply migrations:
python manage.py migrate


Create superuser:
python manage.py createsuperuser


Run development server:
python manage.py runserver

⚙️ Configuration

Configure your .env file with these essential variables:
DEBUG=True
SECRET_KEY=your-secret-key-here
DATABASE_URL=sqlite:///db.sqlite3
EMAIL_HOST=your-smtp-host
EMAIL_PORT=587
EMAIL_USER=your-email@domain.com
EMAIL_PASSWORD=your-email-password

💻 Usage
Admin Interface

Access the admin panel at http://localhost:8000/admin/ to:

    Manage books, categories, and inventory

    View and manage borrowing records

    Administer user accounts and permissions

    Generate system reports

User Features

    Register/login at http://localhost:8000/userauths/sign-up/

    Browse and search available books

    Borrow/return books (when authenticated)

    View personal borrowing history and due dates

    Receive email notifications for overdue books
