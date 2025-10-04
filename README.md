# Low-PocEats 🍽️

A Django-based web application for healthy, low-cost meal planning and recipe management. This application helps users find nutritious meals that fit their dietary preferences, health conditions, and budget constraints.

## Features

### 🔐 User Authentication
- User registration with email verification via OTP
- Secure login/logout functionality
- Custom password reset with email notifications
- Gmail SMTP integration for email services

### 👤 User Profile Management
- Comprehensive user profiles with health information
- Age, height, weight tracking
- Dietary preferences and food allergy management
- Health condition tracking for personalized recommendations

### 🍽️ Recipe Management
- Extensive recipe database with filtering options
- Filter by meal type (breakfast, lunch, dinner, snacks)
- Diet suitability (vegetarian, vegan, keto, etc.)
- Health condition compatibility
- Cost-based filtering for budget-conscious users

### 📧 Communication Features
- Contact forms for user feedback
- Password reset functionality
- Email notifications for account verification

## Technology Stack

- **Backend**: Django 5.1.3 (Python)
- **Database**: SQLite3
- **Frontend**: HTML, CSS, JavaScript
- **Email Service**: Gmail SMTP
- **Authentication**: Django's built-in authentication system

## Project Structure

```
Low-PocEats/
├── DjangoProject2/          # Main Django project settings
│   ├── settings.py         # Configuration and settings
│   ├── urls.py            # URL routing
│   └── wsgi.py            # WSGI configuration
├── demo/                   # Main application
│   ├── models.py          # Database models
│   ├── views.py           # View functions and classes
│   ├── forms.py           # Form definitions
│   ├── urls.py            # App-specific URL routing
│   ├── templates/         # HTML templates
│   │   └── demo/
│   │       ├── login.html
│   │       ├── signup.html
│   │       ├── password_reset_email.html
│   │       └── ...
│   └── static/            # Static files
├── manage.py              # Django management script
├── db.sqlite3            # SQLite database
└── README.md             # Project documentation
```

## Installation & Setup

### Prerequisites
- Python 3.8+
- Django 5.1.3
- Git

### Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/PoojaSancheti/Low-PocEats.git
   cd Low-PocEats
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install django
   ```

4. **Configure email settings**
   - Open `DjangoProject2/settings.py`
   - Update `EMAIL_HOST_USER` with your Gmail address
   - Update `EMAIL_HOST_PASSWORD` with your Gmail app password
   - Update `DEFAULT_FROM_EMAIL` with your desired sender email

5. **Run migrations**
   ```bash
   python manage.py migrate
   ```

6. **Create superuser (optional)**
   ```bash
   python manage.py createsuperuser
   ```

7. **Run the development server**
   ```bash
   python manage.py runserver
   ```

8. **Access the application**
   - Open your browser and go to `http://127.0.0.1:8000/`

## Email Configuration

To enable email functionality:

1. Enable 2-Factor Authentication on your Gmail account
2. Generate an App Password: https://myaccount.google.com/apppasswords
3. Update the following in `DjangoProject2/settings.py`:
   ```python
   EMAIL_HOST_USER = 'your-email@gmail.com'
   EMAIL_HOST_PASSWORD = 'your-app-password'
   DEFAULT_FROM_EMAIL = 'your-display-email@example.com'
   ```

## Usage

1. **Sign Up**: Create a new account with email verification
2. **Complete Profile**: Add your health information and preferences
3. **Browse Recipes**: Filter recipes by your dietary needs and budget
4. **Password Reset**: Use the password reset feature if needed

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

- **Developer**: Pooja Sancheti
- **Email**: sanchetipooja64@gmail.com
- **GitHub**: https://github.com/PoojaSancheti

---

*Built with ❤️ using Django*
