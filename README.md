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

Project Structure
  
Library-Management-System/
├── barrowing/ # Borrowing/returning functionality
│ ├── forms.py # Borrowing forms
│ ├── models.py # Borrowing models
│ ├── urls.py # Borrowing URLs
│ └── views.py # Borrowing views
├── library/ # Core library app
│ ├── context_processor.py # Global context
│ ├── models.py # Book models
│ ├── utils.py # Utility functions
│ └── views.py # Library views
├── userauths/ # User authentication
│ ├── forms.py # User forms
│ └── views.py # Auth views
├── lms_project/ # Project configuration
│ ├── settings.py # Django settings
│ └── urls.py # Main URLs
├── static/ # Static files
│ ├── css/ # Custom styles
│ ├── scripts/ # JavaScript
│ └── images/ # Library images
├── templates/ # HTML templates
├── media/ # User-uploaded files
├── manage.py # Django management
└── requirements.txt # Python dependencies


## Installation

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Eng-AlaaHosny/Library-Management-System.git
   cd Library-Management-System

2.Set up virtual environment
python -m venv myenv
source myenv/bin/activate  # On Windows use `myenv\Scripts\activate`

3.Install dependencies
pip install -r requirements.txt

4.Apply migrations
python manage.py migrate

5.Create superuser
python manage.py createsuperuser

6.Run development server
python manage.py runserver


Configuration:
Configure your environment variables in .env:
DEBUG=True
SECRET_KEY=your-secret-key-here
DATABASE_URL=sqlite:///db.sqlite3

Usage
Admin Interface
Access the admin panel at http://localhost:8000/admin/ to:
Manage books and categories
View borrowing records
Manage user accounts

User Features
Register/login at http://localhost:8000/userauths/sign-up/
Browse available books
Borrow/return books (if authenticated)
View personal borrowing history


   
