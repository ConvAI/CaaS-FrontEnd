# Django Backend for CaaS

To run this project in your development machine, follow these steps:

1. (optional) Create and activate a [virtualenv](https://virtualenv.pypa.io/) (you may want to use [virtualenvwrapper](http://virtualenvwrapper.readthedocs.org/)).

2. Fork this repo and clone your fork:

    `git clone https://github.com/ConvAI/CaaS-FrontEnd.git`

3. Install dependencies:

    `pip install -r requirements.txt`

4. Install mysql server and create a database with name `nervaidb`(or give any other name)

5. Change field values like user,db name(same name as in above step), password, port,etc in `main_site/settings.py`

5. Finally run these commands to sync your models with database:

    `python manage.py makemigrations user userpanel`

    `python manage.py migrate`
    
6. Manually enter userpanel_language table in nervaidb database:

    `id lang_code  lang_name`
    `1  en-us      English-US`
    `1  en-uk      English-UK`
    
7. If everything is alright, you should be able to start the Django development server:

    `python manage.py runserver`

8. Open your browser and go to http://127.0.0.1:8000

