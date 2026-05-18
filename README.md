# API REST - Gestión de Productos y Carrito de Compras

Proyecto desarrollado con Python, Django y Django REST Framework para la gestión de productos y carrito de compras utilizando arquitectura REST.

---

# Descripción del Proyecto

Este proyecto consiste en el desarrollo de una API REST funcional orientada a la administración de productos y carritos de compra.

La aplicación permite:

- Registro de usuarios.
- Autenticación mediante JWT.
- Gestión de productos.
- Administración de carrito de compras.
- Documentación automática con Swagger/OpenAPI.
- Ejecución de pruebas automatizadas.

El sistema fue desarrollado utilizando Django REST Framework siguiendo buenas prácticas de desarrollo backend.

---

# Tecnologías Utilizadas

- Python
- Django
- Django REST Framework
- SimpleJWT
- drf-spectacular
- pytest
- SQLite

---

# Características Principales

## Autenticación JWT

- Registro de usuarios.
- Inicio de sesión mediante tokens JWT.
- Renovación de tokens.
- Protección de rutas privadas.

## Gestión de Productos

- Listado de productos.
- Consulta de productos por ID.
- Creación de productos.
- Actualización de productos.
- Eliminación de productos.

## Carrito de Compras

- Visualización del carrito.
- Agregar productos.
- Modificar cantidades.
- Eliminar productos.
- Vaciar carrito.
- Cálculo automático del total.

## Documentación Automática

- Swagger UI.
- ReDoc.
- Documentación OpenAPI.

## Pruebas Automatizadas

- Validación de endpoints.
- Verificación de autenticación.
- Pruebas del carrito.
- Cobertura mediante pytest.

---

# Instalación del Proyecto

## 1. Clonar el repositorio

```bash
git clone https://github.com/DannyelAlejandro/cemlad-teaching-django.git
```

## 2. Ingresar al directorio

```bash
cd cemlad-teaching-django
```

## 3. Crear entorno virtual

### Windows

```bash
python -m venv venv
```

### Linux / macOS

```bash
python3 -m venv venv
```

---

## 4. Activar entorno virtual

### Windows

```bash
venv\Scripts\activate
```

### Linux / macOS

```bash
source venv/bin/activate
```

---

## 5. Instalar dependencias

```bash
pip install -r requirements.txt
```

---

## 6. Configurar variables de entorno

Crear un archivo llamado `.env` en la raíz del proyecto.

Ejemplo:

```env
SECRET_KEY=django-secret-key
DEBUG=True
DATABASE_URL=sqlite:///db.sqlite3
```

---

## 7. Ejecutar migraciones

```bash
python manage.py migrate
```

---

## 8. Ejecutar servidor

```bash
python manage.py runserver
```

Servidor disponible en:

```text
http://127.0.0.1:8000/
```

---

---

# Endpoints Principales

## Autenticación

| Método | Endpoint | Descripción |
|---|---|---|
| POST | /api/auth/register/ | Registro de usuario |
| POST | /api/auth/token/ | Obtener token JWT |
| POST | /api/auth/token/refresh/ | Renovar token |

---

## Productos

| Método | Endpoint | Descripción |
|---|---|---|
| GET | /api/products/ | Listar productos |
| GET | /api/products/{id}/ | Obtener producto |
| POST | /api/products/ | Crear producto |
| PUT | /api/products/{id}/ | Actualizar producto |
| PATCH | /api/products/{id}/ | Actualización parcial |
| DELETE | /api/products/{id}/ | Eliminar producto |

---

## Carrito de Compras

| Método | Endpoint | Descripción |
|---|---|---|
| GET | /api/cart/ | Ver carrito |
| POST | /api/cart/items/ | Agregar producto |
| PATCH | /api/cart/items/{id}/ | Actualizar cantidad |
| DELETE | /api/cart/items/{id}/ | Eliminar producto |
| DELETE | /api/cart/clear/ | Vaciar carrito |

---

# Ejecución de Pruebas

## Ejecutar pruebas

```bash
pytest
```

## Ejecutar pruebas con cobertura

```bash
pytest --cov
```

---

# Capturas de Pantalla

## Swagger UI

Agregar capturas mostrando:

- Registro de usuarios.
- Login JWT.
- CRUD de productos.
- Carrito de compras.

---

## Pruebas Automatizadas

Agregar capturas mostrando:

- Ejecución de pytest.
- Reporte de cobertura.
- Resultados exitosos.

---

# Estructura General del Proyecto

```text
project/
│
├── products/
├── cart/
├── authentication/
├── tests/
├── manage.py
├── requirements.txt
├── .env
└── README.md
```

---

# Seguridad

El sistema utiliza autenticación JWT para proteger rutas privadas.

Las operaciones sensibles requieren autenticación:

- Crear productos.
- Actualizar productos.
- Eliminar productos.
- Gestionar carrito.

---

# Reglas de Negocio

- Cada usuario posee un único carrito.
- No se pueden agregar productos sin stock.
- El sistema calcula automáticamente el total del carrito.
- Si un producto ya existe en el carrito, la cantidad se incrementa automáticamente.

---

# Autor

Daniel Altamirano

---

# Repositorio GitHub

[https://github.com/DannyelAlejandro/cemlad-teaching-django](https://github.com/Daniel-Metal/cemlad-teaching-django.git)

---



