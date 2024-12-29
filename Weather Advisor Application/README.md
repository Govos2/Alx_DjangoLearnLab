# Healthy Habits Tracker

A Django-based web application to track daily habits and promote healthy lifestyle choices.

## Setup Instructions

Installation
Clone the Repository:

git clone <repository_url>
cd e-commerce_product_api
Create a Virtual Environment:

python -m venv venv
source venv/bin/activate    # On Windows: venv\Scripts\activate
Install Dependencies:

pip install -r requirements.txt
Configure Database:

If using MySQL, update the DATABASES setting in settings.py with your database credentials.
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': '<database_name>',
        'USER': '<username>',
        'PASSWORD': '<password>',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
Apply Migrations:

python manage.py makemigrations
python manage.py migrate
Create Superuser:

python manage.py createsuperuser
Run the Server:

python manage.py runserver
Usage
Endpoints
Authentication
POST /api/token/ - Obtain authentication tokens
POST /api/token/refresh/ - Refresh authentication tokens
Products
GET /api/products/ - List all products
POST /api/products/ - Create a new product (Admin only)
GET /api/products// - Retrieve a single product
PUT /api/products// - Update a product (Admin only)
DELETE /api/products// - Delete a product (Admin only)
Environment Variables
Set the following environment variables in a .env file or in your environment:

SECRET_KEY=<your_django_secret_key>
DEBUG=True
ALLOWED_HOSTS=*
DATABASE_NAME=<database_name>
DATABASE_USER=<database_user>
DATABASE_PASSWORD=<database_password>
Deployment
Configure ALLOWED_HOSTS in settings.py.
Use a production-ready web server like Gunicorn with Nginx.
Set up a production database and update the DATABASES setting accordingly.
Use HTTPS for secure connections.
