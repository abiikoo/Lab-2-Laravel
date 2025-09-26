<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## Requisitos Previos
![PHP](https://img.shields.io/badge/PHP-8.0-blue?logo=php) ![Composer](https://img.shields.io/badge/Composer-latest-orange?logo=composer) ![Laravel](https://img.shields.io/badge/Laravel-10.x-red?logo=laravel) ![MySQL](https://img.shields.io/badge/MySQL-8.0-blue?logo=mysql) ![Node.js](https://img.shields.io/badge/Node.js-18-green?logo=nodedotjs) ![VS Code](https://img.shields.io/badge/Editor-VS%20Code-blue?logo=visualstudiocode) 
- PHP ≥ versión 8.0 
- Composer última versión estable.
- Laravel Installer o crear proyecto con laravel new /
composer create-project.
- Paquete de servidor web local: XAMPP / WampServer / Laragon (con Apache/Nginx y MySQL/MariaDB)
- Node.js y npm
- Editor de código (Visual Studio Code recomendado).

## Comandos de Instalación y Flujo de Trabajo

#### 1. Instalación de Laravel y Autenticación

- **Instalar Laravel UI para autenticación de usuario**:
   ```bash
   composer require laravel/ui
   php artisan ui bootstrap --auth
   npm install && npm run dev
 #### 2. Migración de Base de Datos
- **Ejecutar las migraciones para crear las tablas necesarias en la base de datos:**
  ```bash
   php artisan migrate
#### 3. Instalación de Dependencias
- **Instalar todas las dependencias necesarias:**
  ```bash
  composer install

## Introducción a la Arquitectura MVC

Laravel sigue el patrón de arquitectura Modelo-Vista-Controlador (MVC). A continuación, se describe la función de las principales carpetas en este patrón:

- **Carpeta `app/`:** Contiene los **Modelos** y **Controladores**.
  - **Modelo:** Los modelos gestionan la lógica de la aplicación, por ejemplo, `User.php` maneja los datos del usuario.
  - **Controlador:** Los controladores controlan el flujo de datos entre los modelos y las vistas, por ejemplo, `AuthController.php`.

- **Carpeta `routes/`:** Define las **rutas** de la aplicación.
  - **`web.php`**: Contiene las rutas para la interfaz web (páginas y vistas).

- **Carpeta `resources/views/`:** Contiene las **Vistas**, es decir, los archivos Blade que se renderizan en el navegador.
  - **`login.blade.php`**: Vista de la página de inicio de sesión.

- **Carpeta `database/migrations/`:** Contiene los archivos de **migración**, que definen la estructura de las tablas en la base de datos.
  - **`create_users_table.php`**: Archivo de migración que crea la tabla `users`.

Esta estructura permite mantener el código limpio y organizado.

## Base de Datos

Laravel utiliza archivos de **migración** para definir la estructura de la base de datos. Los archivos de migración se encuentran en la carpeta `database/migrations/`. A continuación se describen los pasos seguidos para trabajar con la base de datos:

1. **Configuración del archivo `.env`:**  
- Asegúrate de que la base de datos esté correctamente configurada en el archivo `.env`. Por ejemplo:
   ```env
   DB_CONNECTION=mysql
   DB_HOST=127.0.0.1
   DB_PORT=3306
   DB_DATABASE=nombre_de_tu_base_de_datos
   DB_USERNAME=tu_usuario
   DB_PASSWORD=tu_contraseña
2. **Migración de Base de Datos:**
- Ejecuta el siguiente comando para crear las tablas necesarias en la base de datos:
   ```bash
   php artisan migrate

3. **Backup de la Base de Datos:**
- Después de ejecutar las migraciones, puedes realizar un respaldo de la base de datos para mantener una copia segura de la estructura y los datos:
  ```bash
  mysqldump -u root -p nombre_de_tu_base_de_datos > backup.sql

## 4. **Resultado Visible**

- A continuación, se muestra cómo se ve la pantalla de login tras implementar la autenticación en Laravel:
  <img width="1920" height="834" alt="Image" src="https://github.com/user-attachments/assets/e9101c67-fee7-4108-be9b-831611822ac6" />

- Aquí tenemos el Dashboard una vez iniciamos sesión:
  <img width="1919" height="786" alt="Image" src="https://github.com/user-attachments/assets/41a2948d-b977-4562-af21-fb33182322f8" />

## Dificultades y Soluciones

- **Problema:** Problemas con la versión de PHP y la compatibilidad de Laravel.
  - **Solución:** Se actualizó la versión de PHP a 8.2 en XAMPP, lo que permitió instalar y correr Laravel 12 sin errores de compatibilidad.

- **Problema:** Confusión entre WAMP y XAMPP al momento de ejecutar PHP.
  - **Solución:** Se ajustaron las variables de entorno de Windows para que la terminal reconociera el PHP de XAMPP y no el de WAMP.

- **Problema:** Error al cargar la base de datos en phpMyAdmin.
  - **Solución:** Se inició correctamente el servicio de MySQL en XAMPP y se creó la base de datos lab2laravel con lo recomendado utf8mb4_general_ci.
 
- **Problema:**  Pantalla inicial de Laravel aparecía sin estilos (CSS en blanco).
  - **Solución:** Se instaló e inició el proceso de Vite con npm run dev, asegurando la correcta carga de los estilos y scripts en las vistas Blade.

## Referencias

[1] [Documentación oficial de Laravel](https://laravel.com/docs) <br>
[2] [Laravel Breeze Installation Guide](https://laravel.com/docs/8.x/breeze) <br>
[3] [StackOverflow: Error de migración en Laravel](https://stackoverflow.com/questions/xxxxx)<br>
[4] [Laracasts: Laravel Authentication](https://laracasts.com/series/laravel-8-from-scratch/episodes/10)<br>
[5] [GitHub: Laravel UI](https://github.com/laravel/ui)

---
Este laboratorio ha sido desarrollado por la estudiante de la Universidad Tecnológica de Panamá:  
**Nombre:** Abigail Koo  
**Correo:** abigail.koo@utp.ac.pa  
**Curso:** Ingeniería Web  
**Instructor:** Ing. Irina Fong <br>
**Fecha de Ejecución:** 26 de Septiembre de 2025
