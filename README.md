# My Proyect
Proyecto Django Base configurado para entorno Docker

## Desarrollo
Teniendo pipenv instalado, ejecutar su entorno virtual:

```
pipenv shell
```

Si descarga el repositorio por primera vez, instale las dependencias con:

```
pipenv install --system
```

Para instalar paquetes adicionales en la etapa de desarrollo:

```
pipenv install name_package
```

Para levantar la base de datos:

```
cd myproject
python manage.py migrate
```

Para crear un usuario administrador:

```
cd myproject
python manage.py createsuperuser
```

Para levantar el servidor

```
cd myproject
python manage.py runserver
# Ir a la direccion http://localhost:8000 o http://127.0.0.1:8000
```

## Produccion
En un servidor con docker y docker-compose instalado:

```
docker-compose up -d --build
```

Para levantar la base de datos:

```
docker-compose exec webapp python /app/myproyect/manage.py migrate 
```

Para crear un usuario administrador:

```
docker-compose exec webapp python /app/myproyect/manage.py createsuperuser
```

Luego de estos pasos, solo debe acceder a la direccion en la que esta alojada su aplicación:

[http://ip_servidor:8000](http://ip_servidor:8000)
