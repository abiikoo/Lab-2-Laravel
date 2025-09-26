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
  

## Learning Laravel

Laravel has the most extensive and thorough [documentation](https://laravel.com/docs) and video tutorial library of all modern web application frameworks, making it a breeze to get started with the framework.

You may also try the [Laravel Bootcamp](https://bootcamp.laravel.com), where you will be guided through building a modern Laravel application from scratch.

If you don't feel like reading, [Laracasts](https://laracasts.com) can help. Laracasts contains thousands of video tutorials on a range of topics including Laravel, modern PHP, unit testing, and JavaScript. Boost your skills by digging into our comprehensive video library.

## Laravel Sponsors

We would like to extend our thanks to the following sponsors for funding Laravel development. If you are interested in becoming a sponsor, please visit the [Laravel Partners program](https://partners.laravel.com).

### Premium Partners

- **[Vehikl](https://vehikl.com)**
- **[Tighten Co.](https://tighten.co)**
- **[Kirschbaum Development Group](https://kirschbaumdevelopment.com)**
- **[64 Robots](https://64robots.com)**
- **[Curotec](https://www.curotec.com/services/technologies/laravel)**
- **[DevSquad](https://devsquad.com/hire-laravel-developers)**
- **[Redberry](https://redberry.international/laravel-development)**
- **[Active Logic](https://activelogic.com)**

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
