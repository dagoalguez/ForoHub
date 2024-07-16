# Foro Hub (Proyecto Backend)

La API se centrará específicamente en los tópicos, y debe permitir a los usuarios:

* Crear un nuevo tópico;
* Mostrar todos los tópicos creados;
* Mostrar un tópico específico;
* Actualizar un tópico;
* Eliminar un tópico.

El objetivo principal es implementar una API REST que incluya:

* Rutas API implementadas siguiendo las mejores prácticas REST.
* Validaciones de acuerdo con las reglas de negocio.
* Utilización de una base de datos relacional para la persistencia de datos.
* Implementación de un sistema de autenticación/autorización para restringir el acceso a la información.

## Construcción

Tecnologias con las que fue trabajado el proyecto:

- [Git](https://git-scm.com/) - Control de versions
- [Trello](https://trello.com/) - Gestion de tareas
- [Postman](https://www.postman.com/) y/o [Insomnia](https://insomnia.rest/)- Pruebas API
- [Spring Data JPA](https://spring.io/projects/spring-data-jpa) - Documentacion Spring Data JPA
- [JPA](https://docs.spring.io/spring-data/jpa/reference/jpa.html) - Documentacion JPA

**Configuración del entorno de desarrollo Java para nuestro desafío de construcción del ForoHub en un proyecto Spring.**

Asegúrate de contar con los siguientes programas, archivos y versiones:

- Java JDK: versión: 17 en adelante - [Download the Latest Java LTS Free](https://www.oracle.com/br/java/technologies/downloads/)
- Maven: versión 4 en adelante
- Spring Boot: versión 3.3.1 - [Generar Proyecto](https://start.spring.io/)
- MySQL: versión 8 en adelante - [MySQL: Downloads](https://dev.mysql.com/downloads/mysql/)
- IDE (Entorno de desenvolvimento integrado) IntelliJ IDEA- [Descargar IntelliJ IDEA: el IDE líder para Java y Kotlin](https://www.jetbrains.com/es-es/idea/download/?section=windows)

Configuración al crear el proyecto en [Spring Initializr](https://start.spring.io/):

- Java (versión 17 en adelante)
- Maven (Initializr utiliza la versión 4)
- Spring Boot (versión 3.3.1)
- Proyecto en JAR
  
Dependencias para agregar al crear el proyecto en [Spring Initializr](https://start.spring.io/):

- Lombok
- Spring Web
- Spring Boot DevTools
- Spring Data JPA
- Flyway Migration
- MySQL Driver
- Validation
- Spring Security

Dependencia adicional a agregar para Autenticacion:
- [JWT](https://github.com/auth0/java-jwt)

## Para sy ejecucion

1. Primero crearemos la base de datos con el nombre 'foro_hub' en MySQL
2. Seguidamente configuramos el archivo 'application.properties' para conectarnos a la base de datos:
    ```java
    spring.datasource.url=jdbc:mysql://${DB_HOST}/foro_hub
    spring.datasource.username=root
    spring.datasource.password=${DB_PASSWORD}
    ```
    El campo ${DB_HOST} se debe reemplazar con la direccion del servidor al igual que ${DB_PASSWORD} indica la contrasena de la BD, FlyWay generara automaticamente las tablas necesarias en BD.
3. Luego seteamos un usuario y contrasenha en la tabla 'usuarios' (La contrasenha debe estar encriptada con [Bcrypt hash](https://bcrypt-generator.com/))
![image](https://github.com/user-attachments/assets/6db267dc-a87e-4b43-b0f2-e2a2d2ffaf73)
5. Finalmente para poder realizar los test desde Postman, es necesario Generar un Token de autenticacion de tipo 'Bearer token' con el usuario y contrasenha.
![image](https://github.com/user-attachments/assets/9c9ce093-2b5f-41d1-b322-c445f67de556)
**Nota**: Los test en Postman, solo se podran realizar utilizando la clave jwtToken.
6. Tests en Postman

- Test listar Topicos
![image](https://github.com/user-attachments/assets/7c0b68de-2ed0-4c70-a0ed-cfeab19e42b6)

- Registrar topico
![image](https://github.com/user-attachments/assets/10db395a-648e-4815-8983-a3c783c3ef53)

## Roadmap

Este proyecto tendra mejoras a futuro con las especificaciones mencionadas:

* Para nuestro foro estar completo deberíamos tener otras rutas o endopints que nos permitirán crear, listar, actualizar y eliminar otras informaciones además de los tópicos como:
  /usuario
  /respuestas
* Documentar la API con SpringFox Swagger, ya que ofrece una interfaz amigable y accesible, así como una forma de documentación automática generada simultáneamente con el desarrollo de la API.

it](https://git-scm.com) para el control de versiones.

