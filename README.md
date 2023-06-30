
# Django Job Application Form

It is a basic Job Application form created using **Python** and **Django** which takes the user input and whenever user clicks on submit it stores the user information in SQLite database and sends an email to the employer regarding the information of the candidate.
- You can edit the database by accessing admin page with the url 
```bash
localhost:8000/admin/login/?next=/admin/
```
- Bootstrap was used to add styling the form.
- With Dockerfile you can create a Docker Image of the app.
- To use this code you have to create an app on your google account and copy paste its password in **mysite/variables.py** file.
- Link to create app in google account [https://myaccount.google.com/apppasswords](https://myaccount.google.com/apppasswords)




## Run Locally

Install requirements

```bash
  pip install --no-cache-dir -r requirements.txt
```

Initialise model in database

```bash
  python manage.py makemigrations
  python manage.py migrate
```

Create super user to access admin page
```bash
  python manage.py createsuperuser
```
Run the Server
```bash
  python manage.py runserver
```

### Run with Docker

- Before building the docker image you can change the admin credentials in **Dockerfile**

Build the docker image
```bash
  docker build -t django-form .
```
Run the image
```bash
  docker run -p 8000:8000 django-form
```



## Screenshots

![ss1](https://github.com/AkramExp/django-form/blob/main/screenshots/ss1.png)
![ss2](https://github.com/AkramExp/django-form/blob/main/screenshots/ss2.png)

