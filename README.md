# Python-API-Rest-Template

[![Open Source Love](https://badges.frapsoft.com/os/mit/mit.svg?v=102)](https://github.com/ellerbrock/open-source-badge/)
[![star this repo](http://githubbadges.com/star.svg?user=antonioalfa22&repo=Python-API-Rest-Template&style=flat)](https://github.com/antonioalfa22/Python-API-Rest-Template)
[![fork this repo](http://githubbadges.com/fork.svg?user=antonioalfa22&repo=Python-API-Rest-Template&style=flat)](https://github.com/antonioalfa22/Python-API-Rest-Template/fork)

## 1. Estructura y Flujo

```bash
└───api
    ├───controllers
    ├───models
    ├───middlewares
    ├───repository
    ├───routes
└───test
```

![flow diagram](./flow.png)

### 1.1. Models

Representa el modelo de datos, (por ejemplo un usuario).

### 1.2. Repository

Se encargan de proporcionar los métodos de acceso a base de datos para trabajar con los modelos (Entidades).

### 1.3. Middlewares

Son los componentes encargados de comprobar si se debe o no seguir con la petición. Por ejemplo autorización o roles.

### 1.4. Controllers

Los controladores son los encargados de realizar las operaciones requeridas por la petición definida en la ruta.

_______

## 2. Ejecutar

### 2.1. Variables de entorno
Mediante las variables de entorno se pueden cambiar tanto la Base de datos como el modo de ejecución. Nombres:

> DATABASE_URL: Url a la base de datos
> MODE: dev, test o prod

Para ejecutar la API-Rest en modo de desarrollo o testeo se deben ejecutar las siguientes instrucciones:

```bash
virtualenv venv
.\venv\Scripts\activate
pip install -r requirements.txt
python server.py run
```

## 2. Ejecutar con Docker

1. **Build**

```docker
docker build . -t api-rest:latest
```

2. **Run**

```docker
docker run api-rest
```

## 3. Ejecutar tests

```python
python server.py test
```
