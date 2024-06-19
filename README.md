# Techyon-Assessment
This Django project allows users to register with their email addresses and verifies their email through a confirmation link sent via email.

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
1. Leverage Class-Based Views and DRF Serializers:
   
   1.1 Refactor to Class-Based Views:
      Transition from function-based views to class-based views using Django REST Framework (DRF) ModelViewSets. This promotes code reusability, simplifies view logic, and provides a           cleaner structure for handling common CRUD operations (Create, Read, Update, Delete).
   1.2 Implement DRF Serializers:
         Employ DRF serializers for data validation and serialization/deserialization between models and JSON representations. This ensures data integrity, simplifies data exchange, and           facilitates field-level control.

2. Establish a Robust Backend-Frontend Separation:

   2.1 API-Driven Approach:
         Design a well-defined RESTful API using DRF to decouple the backend logic from the frontend presentation. This enables flexibility in building independent frontend applications          using various frameworks or libraries (e.g., React, Angular, Vue.js) while maintaining a consistent data layer.
   2.2 Clear Separation of Concerns:
         Separate backend and frontend concerns for maintainability and scalability. The backend focuses on data management and business logic, while the frontend handles user                     interactions and presentation.

3. Implement Granular Group-Based Access Control (RBAC):

   3.1 Fine-Grained Permissions:
         Employ Django's built-in permission system or a third-party library like django-guardian to establish role-based access control (RBAC). This grants granular control over what             actions users or groups can perform on specific resources or data sets.
   3.2 Flexible Authorization Policies:
         Design flexible permission policies that define access levels based on user roles or groups. This ensures data security and compliance with business requirements.
   
