# Two Factor Authentication Implementation with PyOTP and Google Authenticator in Your Flask App

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

Since this is the first time running our app, we will need to run all the above commands. Later, whenever we make changes to the database, we will just need to run the last two commands. 

4. After that, you can run your application using the command:
```python
python manage.py run
```
