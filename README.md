To run the application, activate the virtual environment, install the requirements from the requirements.txt file and make changes to the `DATABASES` variable in the `django_postgres/setting.py` file.

```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'YOUR_DATABASE',
        'USER': 'YOUR_USER',
        'PASSWORD': 'YOUR_PASSWORD',
        'HOST': 'localhost',
        'PORT': '',
    }
}
```

Run the commands - ```python3 manage.py makemigrations``` and ```python3 manage.py migrate```.
To start server, run - ```python3 manage.py runserver```
The API will be accessible at - `https://127.0.0.1:8000/user`

Make the following requests to the respective endpoints - 
1. `GET /user/` - To get all the data at once.
2. `GET /user/uuid/` - To get the data of any particular user.
3. `POST /user/` - To create a new user.
4. `PUT /user/uuid/` - To update an existing user.
5. `DELETE /user/uuid/` - To delete an existing user.

The User model has the following fields - 
1. id - UUID Field
2. name - String Field
3. email - Email Field
4. password - String Field
5. website - String Field
