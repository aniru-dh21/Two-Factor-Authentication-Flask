# Two Factor Authentication Implementation with PyOTP and Google Authenticator in Your Flask App

Two-Factor Authentication, or 2FA, is like having an extra lock on the door to your online accounts. Instead of just using a password, 2FA adds another layer of security. It's a bit like needing both a key and a special code to open a vault.

## Two-Factor Authentication Workflow in Our Application

1. **Registration with 2FA Setup**: When users sign up on our website, they're prompted to set up an extra layer of security-2FA. This involves scanning a QR code using an authenticator app, such as Google Authenticator, to link their account securely.

2. **Login Initiation:** When user return to log in, they start by entering their usual email/username and password combo to access their account.

3. **Extra Security Check:** Before granting access, our website throws in an additional hurdle: users need to provide an OTP (One-Time Password) displayed on their authenticator app. This ensures they're not just entering the password but also confirming their identify with a unique, time-sensitive code.

4. **Validation and Authorization:** The user inputs the received OTP into our platform. The system then double-checks this OTP against the expected code, validating the information. If the OTP matches, it's like handing over the secret handshake, granting the user access to their account.

This seamless back-and-forth between passwords, authenticator apps, and unique codes ensures that only the rightful account can access the precious content behind the digital doors of your website.

## Libraries Used
- <ins>Flask</ins> is a simple, easy-to-use microframework for Python that helps you build scalable and secure web applications.
- <ins>Flask-Login</ins> provides user session management for Flask. It handles the common tasks of logging in, logging out, and remembering your users' sessions over extended periods of time.
- <ins>Flask-Bcrypt</ins> is a Flask extension that provides bcrypt hashing utilities for your application.
- <ins>Flask-WTF</ins> is a simple integration of Flask and WTForms that helps you create forms in Flask.
- <ins>Flask-Migrate</ins> is an extension that handles SQLAlchemy database migrations for Flask applications using Alembic. The database operations are made available through the Flask command-line interface.

## File Structure after development

```
Two-Factor-Authentication-Flask/
├── migrations/
├── src/
│   ├── accounts/
│   │   ├── __init__.py
│   │   ├── forms.py
│   │   ├── models.py
│   │   └── views.py
│   ├── core/
│   │   ├── __init__.py
│   │   └── views.py
│   ├── static/
│   │   └── styles.css
│   ├── templates/
│   │   ├── accounts/
│   │   │   ├── login.html
│   │   │   ├── register.html
│   │   │   ├── setup-2fa.html
│   │   │   └── verify-2fa.html
│   │   ├── core/
│   │   │   └── index.html
│   │   ├── _base.html
│   │   └── navigation.html
│   ├── __init__.py
│   └── utils.py
├── .env
├── config.py
└── manage.py
```

## Clonning the repository 

1. Clone this repository to your local machine:

```bash
git clone https://github.com/aniru-dh21/Two-Factor-Authentication-Flask.git
```

2. Install the required Python packages:

```bash
pip install -r requirements.txt
```

## Running the Flask for the First Time

1. To initialize the database (create a migration repository), use the command:
```python
flask db init
```

2. To migrate the database changes, use the command:
```python
flask db migrate
```

3. To apply the migrations, use the command:
```
flask db upgrade
```

4. Since this is the first time running our app, we will need to run all the above commands. Later, whenever we make changes to the database, we will just need to run the last two commands. 

5. After that, you can run your application using the command:
```python
python manage.py run
```
