#  API de Inventario v1 (FastAPI + SQLAlchemy + SQLite)

##  Descripción

Este proyecto es una API REST diseñada para la gestión de un sistema de inventario básico. Está desarrollada con FastAPI, utilizando SQLAlchemy como ORM y SQLite como base de datos.

La aplicación permite realizar operaciones CRUD (crear, leer, actualizar y eliminar productos), aplicando una arquitectura en capas para mejorar la organización del código, la escalabilidad y el mantenimiento.

---

##  Objetivos del proyecto

- Construir una API REST con FastAPI.
- Aplicar arquitectura en capas (routes, services, repositories, models y schemas).
- Integrar SQLAlchemy como ORM para la gestión de datos.
- Utilizar SQLite como base de datos ligera.
- Implementar validaciones de datos con Pydantic.
- Desarrollar operaciones CRUD completas para productos.

---

##  Arquitectura del sistema

- Routes: manejan las peticiones HTTP.
- Services: contienen la lógica de negocio.
- Repositories: gestionan el acceso a la base de datos.
- Models: definen las tablas en SQLAlchemy.
- Schemas: validan la entrada y salida de datos con Pydantic.

---

##  Tecnologías utilizadas

- Python 3
- FastAPI
- SQLAlchemy
- SQLite
- Pydantic
- Uvicorn

---

##  Estructura del proyecto

inventario_api/
├── app/
│   ├── main.py
│   ├── database/
│   │   └── connection.py
│   ├── models/
│   │   └── product.py
│   ├── schemas/
│   │   └── product.py
│   ├── repositories/
│   │   └── product_repository.py
│   ├── services/
│   │   └── product_service.py
│   └── routes/
│       └── product_routes.py
├── requirements.txt
└── README.md

---

##  Instalación

git clone <URL_DEL_REPOSITORIO>
cd inventario_api

python -m venv venv
venv\Scripts\activate   (Windows)
source venv/bin/activate (Linux/Mac)

pip install -r requirements.txt

---

##  Ejecución

uvicorn app.main:app --reload

API:
http://127.0.0.1:8000
Swagger:
http://127.0.0.1:8000/docs
Redoc:
http://127.0.0.1:8000/redoc

---

##  Base de datos

Se genera automáticamente:

inventario.db

---

##  Endpoints

POST /products/
GET /products/
GET /products/{id}
PUT /products/{id}
DELETE /products/{id}

---

##  Validaciones

- Nombre mínimo 3 caracteres
- Precio > 0
- Stock ≥ 0
- Categoría mínimo 3 caracteres

---

##  Autor

Edith caro 

