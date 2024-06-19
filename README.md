# Techyon-Assessment
Assignment Needed to be completed as below:
the assignment is to develop an authorization module. This consists of three parts mainly - signup page, login page and about page. This can be normally seen across the websites like Zomato, Flipkart, Makemytrip to name a few.

## Features

- User registration with username, first name, last name, email, and password.
- Unique username and email validation.
- Password matching validation.
- Email confirmation link sent to the user's registered email address.
- Account activation upon successful email confirmation.
- User login with username and password.
- User logout.

## Prerequisites

Make sure you have the following installed:

- Python (version 3.7 or higher)
- Django (version 3.0 or higher)


## Getting Started

1. Clone the repository:
   ```
    [https://github.com/samysingh983/Techyon-Assessment/](https://github.com/samysingh983/Techyon-Assessment.git)
   ```

2. Create a virtual environment and activate it:
   ```
   pip install virtualenv
   virtualenv venv
   venv\scripts\activate
   ```

3. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```

4. Apply migrations to set up the database:
   ```
   python manage.py makemigrations
   python manage.py migrate
   ```

5. Start the development server:
   ```
   python manage.py runserver
   ```

6. Access the application in your web browser at `http://localhost:8000/`.

## Configuration

1. Set up email settings in `settings.py`:

```python
# Email settings
EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
EMAIL_HOST = 'your_email_host'
EMAIL_PORT = 587
EMAIL_HOST_USER = 'your_email_address'
EMAIL_HOST_PASSWORD = 'your_email_password' #password generated from security page on manage account section of your email account(search for "App Password")
EMAIL_USE_TLS = True
DEFAULT_FROM_EMAIL = 'your_default_from_email_address'
```

2. Configure the email templates for email confirmation and activation in the templates directory.

## Usage
1. Register a new user by providing a username, first name, last name, email, and password.
2. After successful registration, an email with a confirmation link will be sent to the provided email address.
3. Click on the confirmation link in the email to activate the account.
4. Login with the registered username and password.
5. Logout from the application.


## Acknowledgements
1. This project is based on Django, a high-level Python web framework.
2. It utilizes Django's built-in user authentication and email sending capabilities.
3. The project uses Bootstrap for styling the frontend forms and pages.
4. Special thanks to the Django community for providing valuable resources and documentation


## Enhancement/Improvement
1. Leverage Class-Based Views and DRF Serializers.
2. Establish a Robust Backend-Frontend Separation.
3. Implement Granular Group-Based Access Control.
4. Unit Testing Can Be Implemented.
