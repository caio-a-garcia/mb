# MB - Message Board app

Project from the 3rd chapter of [Django for Beginners](https://www.amazon.com.br/Django-Beginners-websites-Python-English-ebook/dp/B079ZZLRRL)
All instructions are run on Windows cmd, inside project folder after clonning with:
```git clone https://github.com/caio-a-garcia/mb.git```

## Setup

 1) `python -m venv <env_folder_name>`
 2) `<env_folder_name>\Scripts\activate`
 3) `pip install -r requirements.txt`
 4) `python manage.py migrate`

Command 1 uses python venv to create the virtual environment. <evn_folder_name> is the folder where the files for the environment will be created. It creates the folder if it doesn't exist, use '.' to create the files on current folder.

Command 2 runs the activate batch script to activate the virtual environment. On cmd, you will know it worked if the environment name appear before path at the command line:
```(<env_folder_name) C:\path\to\project```

Command 3 installs the project dependencies listed in 'requirements.txt`. To create or update this file, run:
```pip freeze > requirements.txt```

Command 4 creates the database from project settings. Without this command the database will be created when the project is run. This command ensures the database is up to date with the project.

## Running the project

Run project with `python manage.py runserver`
See the project running by pointing your browser at http://127.0.0.1:8000/
Run tests with `python manage.py test`

## Using [Django Admin](https://docs.djangoproject.com/en/2.1/ref/contrib/admin/)

Run the command `python manage.py createsuperuser` to create a user for accessing the Django Admin site. Django Admin offers a CRM-like graphical user interface to interact with the SQLite database. This is where you can create posts for the blog app.

## Notes
### Differences between the project this implementation and the one on *Django for Begginers*

This implementation uses `venv` for managing the virtual environment as shown in the [official recomendation](https://peps.python.org/pep-0405/). Both `venv` and `pipenv` seem compliant with what is specified in PEP 405.

### Project Features

This project noticeably lacks a client interface for posting. While the admin interface does not properly address this need, the main purpose of this project as show in the book, as well as in the current implementation, is to experiment with the Admin site and a basic Django project structure.

The project should be ready to be deployed with [Heroku](https://devcenter.heroku.com/articles/getting-started-with-python). 