run.py	This is the file that is invoked to start up a development server. It gets a copy of the app from your package and runs it. This won’t be used in production, but it will see a lot of mileage in development.

requirements.txt	This file lists all of the Python packages that your app depends on. You may have separate files for production and development dependencies.

config.py	This file contains most of the configuration variables that your app needs.

/instance/config.py	This file contains configuration variables that shouldn’t be in version control. This includes things like API keys and database URIs containing passwords. This also contains variables that are specific to this particular instance of your application. For example, you might have DEBUG = False in config.py, but set DEBUG = True in instance/config.py on your local machine for development. Since this file will be read in after config.py, it will override it and set DEBUG = True.

/yourapp/	This is the package that contains your application.

/yourapp/__init__.py	This file initializes your application and brings together all of the various components.

/yourapp/views.py	This is where the routes are defined. It may be split into a package of its own (yourapp/views/) with related views grouped together into modules.

/yourapp/models.py	This is where you define the models of your application. This may be split into several modules in the same way as views.py.

/yourapp/static/	This directory contains the public CSS, JavaScript, images and other files that you want to make public via your app. It is accessible from yourapp.com/static/ by default.

/yourapp/templates/	This is where you’ll put the Jinja2 templates for your app.
