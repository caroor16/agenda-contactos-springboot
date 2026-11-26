# Agenda de Contactos - Spring Boot & Thymeleaf

Aplicación web full-stack para la gestión de contactos (CRUD completo) desarrollada con Java, Spring Boot, Thymeleaf y MySQL siguiendo el patrón arquitectónico MVC.

## Funcionalidades

- **Listar contactos:** Visualización en tabla dinámica de todos los registros almacenados en la base de datos.
- **Agregar contacto:** Formulario de alta con validación de campos obligatorios (`nombre`, `celular`, `email`).
- **Editar contacto:** Precarga de datos existentes mediante identificador único y actualización en base de datos.
- **Eliminar contacto:** Borrado directo de registros desde la vista principal.

## Tecnologías Utilizadas

- **Backend:** Java 21, Spring Boot 3.3.5 (Spring Web, Spring Data JPA)
- **Frontend:** Thymeleaf (plantillas y fragmentos reutilizables), Bootstrap 5.3.3
- **Base de Datos:** MySQL
- **Herramientas:** Maven, Lombok, IntelliJ IDEA

## Requisitos Previos

- JDK 21 o superior
- MySQL Server activo
- Maven

## Configuración y Ejecución

1. **Clonar el repositorio:**
   git clone https://github.com/tu-usuario/agenda-contactos-springboot.git
   cd agenda-contactos-springboot

2. **Configurar la base de datos:**
   Crea una base de datos vacía en MySQL llamada `contactos_db` (Hibernate generará automáticamente la tabla `contacto` al iniciar la aplicación):
   CREATE DATABASE contactos_db;

3. **Configurar credenciales:**
   En `src/main/resources/application.properties`, ajusta tu usuario y contraseña de MySQL:
   spring.datasource.url=jdbc:mysql://localhost:3306/contactos_db?createDatabaseIfNotExist=true
   spring.datasource.username=root
   spring.datasource.password=tu_password

4. **Ejecutar la aplicación:**
   mvn spring-boot:run
   Una vez iniciada, abre tu navegador en http://localhost:8080/