# apiRestDjango python 3.8.2
https://www.django-rest-framework.org/tutorial/quickstart/

<h1> Pasos para hacer una api rest con Python-Django</h1>

# Create the project directory
```sh
mkdir tutorial
```

# Go folder
```sh
cd tutorial
```

# Create a virtual environment to isolate our package dependencies locally
```sh
python3 -m venv env
```

# - On Windows use
```sh
source env\Scripts\activate
```

# - On linux use
```sh
source env/bin/activate 
```

# Install Django into the virtual environment
```sh
pip install django
```

# Install Django REST framework into the virtual environment
```sh
pip install djangorestframework
```

# Set up a new project with a single application
```sh
django-admin startproject tutorial  .# Note the trailing '.' character
cd tutorial
django-admin startapp quickstart
cd ..

python manage.py migrate
python manage.py createsuperuser --email admin@example.com --username admin
```


#Cuidado 1

- Encuentras linea de codigo en la pagina oficial de, https://www.django-rest-framework.org/tutorial/quickstart/
- Linea de codigo que esta mal en Archivo 'Views.py' CUANDO ya este el codigo pegado en tu script aparecera esto:
```sh
from tutorial.quickstart.serializers import UserSerializer, GroupSerializer
```

- Archivo 'Views.py' cambialo por esta linea de codigo que es la correcta:
```sh
from .serializers import UserSerializer, GroupSerializer
```

#Cuidado 2
- Encuentras linea de codigo en la pagina oficial de, https://www.django-rest-framework.org/tutorial/quickstart/
- Linea de codigo que esta mal en Archivo 'URLs.py' CUANDO ya este el codigo pegado en tu script aparecera esto:
```sh
from tutorial.quickstart import views
```

- Ahora en el Archivo 'URLs.py' cambialo  por esta linea de codigo que es la correcta:
```sh
from quickstart import views
```
