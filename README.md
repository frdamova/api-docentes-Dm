API CRUD de Docentes

Este proyecto consiste en una API REST desarrollada en Spring Boot para gestionar docentes.
Permite crear, consultar, actualizar y eliminar docentes, aplicando reglas de negocio y manejo de excepciones personalizado.
Los datos se almacenan en una base de datos en memoria H2.

Funcionalidades principales

Crear un docente.

Consultar todos los docentes.

Consultar un docente por ID.

Actualizar un docente.

Eliminar un docente.

Regla de negocio implementada

La API no permite crear un docente si ya existe en el sistema otro con el mismo tipo de documento y número de documento.
Al intentar hacerlo, la aplicación genera una excepción personalizada que se devuelve al cliente con un mensaje claro.

Manejo de excepciones

El proyecto incluye:

Excepción personalizada para docentes duplicados.

Controlador global de excepciones para devolver mensajes claros al cliente.

Respuestas con formato estándar que informan el tipo de error y su causa.

Pruebas desde Postman

Se realizaron pruebas de los siguientes endpoints:

POST /api/docentes

GET /api/docentes

GET /api/docentes/{id}

PUT /api/docentes/{id}

DELETE /api/docentes/{id}

Se comprobó que:

El CRUD funciona correctamente.

La regla de negocio evita duplicados.

Las excepciones se visualizan correctamente en las respuestas.

Base de datos H2

La API utiliza H2 como base de datos en memoria.
La consola se accede desde el navegador en la URL:

http://localhost:8080/h2-console

Permite visualizar las tablas y datos creados durante las pruebas.

Tecnologías utilizadas

Java

Spring Boot

Spring Web

Spring Data JPA

H2 Database

Maven

Autor

Freider David Morales Vásquez
Ingeniería de Sistemas
Universidad del Tolima
