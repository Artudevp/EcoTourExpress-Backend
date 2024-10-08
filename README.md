# EcoTourExpress - Backend

## Descripción

**EcoTourExpress** es un sistema de gestión para una empresa de ecoturismo. El proyecto tiene como objetivo facilitar la administración de clientes, actividades, rutas, hospedajes y productos, ofreciendo funcionalidades tanto para usuarios administradores como clientes. Incluye una API RESTful desarrollada con **Java** y **Spring Boot**, con seguridad implementada mediante **JWT (JSON Web Tokens)** y roles de usuario.

## Funcionalidades

- Gestión de usuarios (Clientes, Administradores).
- CRUD para entidades:
  - **Usuario**: Nombre, Email, Contraseña, Rol.
  - **Cliente**: Información personal y de contacto.
  - **Producto**: Nombre, Categoría, Cantidad disponible, Precio.
  - **Actividad**: Nombre, Duración, Capacidad.
  - **Ruta**: Conjunto de actividades, Capacidad dependiente de las actividades.
  - **Hospedaje**: Tipos de habitación, Capacidad, Precio.
- Validaciones de datos para evitar inconsistencias en las entradas de la base de datos.
- Actualización automática de disponibilidad de productos y servicios.
- Autenticación y autorización con JWT.
- Control de acceso basado en roles (Admin, Cliente).
- API REST para interactuar con el sistema desde un frontend o cliente externo.

## Tecnologías Utilizadas

- **Java 17**
- **Spring Boot**
- **Spring Security** (para la autenticación y autorización)
- **JWT** (para la autenticación con tokens)
- **JPA** (para el manejo de la persistencia de datos)
- **Hibernate** (ORM para las entidades)
- **Lombok** (para evitar código repetitivo como getters y setters)
- **MySQL** (Base de datos relacional)
- **Maven** (para la gestión de dependencias)

## Entidades Principales

- **Usuario**:
  - `nombre`: Nombre del usuario.
  - `email`: Dirección de correo electrónico.
  - `contraseña`: Contraseña del usuario.
  - `rol`: Rol del usuario (admin, cliente).
  
- **Cliente**:
  - `nombre`, `id_cliente`, `cedula`, `edad`, `genero`.
  - Relaciones con otras entidades como **Hospedaje**, **Producto**, **Actividad** y **Ruta**.

- **Producto**:
  - `id_producto`, `nombre`, `categoria`, `cantidad_disponible`, `precio`.
  
- **Actividad**:
  - `nombre`, `duración`, `capacidad`.
  
- **Ruta**:
  - Conjunto de actividades, capacidad dependiente de las actividades.
  
- **Hospedaje**:
  - `tipo_habitación`, `capacidad`, `precio`, `disponibilidad`.

## Instalación y Configuración

1. Clonar el repositorio:

   ```bash
   git clone https://github.com/usuario/ecotour-express-backend.git
