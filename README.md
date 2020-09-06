# apiRestDjango python 3.8.2
https://www.django-rest-framework.org/tutorial/quickstart/


# Create the project directory
mkdir tutorial
cd tutorial

# Create a virtual environment to isolate our package dependencies locally
python3 -m venv env

# - On Windows use
source env\Scripts\activate

# - On linux use
source env/bin/activate 

# Install Django into the virtual environment
pip install django

# Install Django REST framework into the virtual environment
pip install djangorestframework

# Set up a new project with a single application
django-admin startproject tutorial  .# Note the trailing '.' character
cd tutorial
django-admin startapp quickstart
cd ..

python manage.py migrate
python manage.py createsuperuser --email admin@example.com --username admin



OJO
-encuentras linea de codigo en la pagina oficial de, https://www.django-rest-framework.org/tutorial/quickstart/
-una Linea de codigo que esta mal en Archivo 'Views.py' CUANDO ya este el codigo pegado en tu script aparecera esto:
from tutorial.quickstart.serializers import UserSerializer, GroupSerializer

-Archivo views cambialo por la correcta que es:
from .serializers import UserSerializer, GroupSerializer


OJO
-encuentras linea de codigo en la pagina oficial de, https://www.django-rest-framework.org/tutorial/quickstart/
una Linea de codigo que esta mal en Archivo 'URLs.py' CUANDO ya este el codigo pegado en tu script aparecera esto:
from tutorial.quickstart import views

-Ahora en el Archivo 'URLs.py' cambialo porla correcta que es:
from quickstart import views

