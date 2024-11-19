# Proyecto Django: Desafío - Django y PostgreSQL Básico

Este proyecto aborda la creación de un entorno Django conectado a una base de datos PostgreSQL. El proyecto se llama **desafiodb** y contiene una aplicación llamada **testdb**. Se ha configurado para crear y gestionar una tabla personalizada llamada `adltest`, además de utilizar las tablas generadas automáticamente por Django.

## Requerimientos Técnicos

- **Motor de base de datos:** PostgreSQL
- **Framework web:** Django
- **Entorno de Python:** Virtual environment (opcional, pero recomendado)

## Instrucciones de Desarrollo

### 1. Instalación y configuración del motor de base de datos PostgreSQL

1. Instalar PostgreSQL en el sistema.
2. Crear una base de datos llamada `adl-test`:
   ```sql
   CREATE DATABASE "adl-test";

### 2. Configuración del Proyecto Django

1. Crear el proyecto Django
```sql
django-admin startproject desafiodb

2. Crear la aplicación dentro del proyecto:
```sql
python manage.py startapp testdb

3. Configurar la conexión a PostgreSQL en el archivo settings.py
```sql
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'adl-test',
        'USER': 'myuser',
        'PASSWORD': 'mypassword',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}

### 3. Creación del Modelo y Migraciones

1. Definir el modelo en el archivo models.py de la aplicación testdb:
```sql
from django.db import models
class AdlTest(models.Model):
    campo1 = models.CharField(max_length=100)
    valor1 = models.IntegerField()

2. Generar las migraciones:

```sql
python manage.py makemigrations
```

3. Aplicar las migraciones:

```sql
python manage.py migrate
```

### 4.Verificación en consola de Postgres

1. Acceder a SQL Shell y verificar la creación de la base de datos.

2. Confirmar la existencia de la tabla personalizada adltest y las tablas generadas automáticamente por Django (auth_user, django_migrations, etc.).

3. Captura: Se incluye una imagen de la vista, con las tablas correctamente creadas.

## 5. Capturas  

Las capturas solicitadas están en la carpeta capturas.

## Autor  
**Karen Limarí**
