# Sistema de Gestión de Contactos

## Descripción del proyecto

Este proyecto es una aplicación web desarrollada en PHP que permite a los usuarios gestionar contactos. El sistema incluye funcionalidades de registro, inicio de sesión y un panel guardar mensajes enviados a los contactos almacenados.

## Características principales

- Registro de usuarios e inicio de sesión
- Agregar y mostrar contactos
- Búsqueda de usuarios a partir del nombre

### Tecnologías utilizadas

- PHP
- MySQL
- HTML5
- CSS3

## Instalación y configuración

1. Clonar el repositorio
2. Configurar el archivo `conexion.php` con los datos de conexión a la base de datos:

    ```php
    <?php
    define('DB_SERVER', 'localhost');
    define('DB_USERNAME', 'tu_usuario');
    define('DB_PASSWORD', 'tu_contraseña');
    define('DB_NAME', 'nombre_db');
    ?>
    ```

3. Acceder a la aplicación a través del navegador


## Estructura del proyecto

| Directorio/Archivo | Descripción |
|--------------------|-------------|
| `index.php`        | Página principal para mostrar la información de los contactos del usuario |
| `login.php`        | Página de inicio de sesión |
| `register.php`     | Página de registro de usuario |
| `details.php?id=1` | Muestra el historial de mensajes de un contacto en función de la ID |


## Ejemplo de código: Conexión a la base de datos

```php
<?php
require_once 'config.php';

function conexionDB() {
    $conexion = new mysqli(DB_SERVER, DB_USERNAME, DB_PASSWORD, DB_NAME);
    
    if ($conn->connect_error) {
        die("Algo ha salido mal");
    }
    
    return $conexion;
}
?>
```
## Enlaces útiles

- [Documentación para usar MySQLi](https://www.php.net/manual/es/book.mysqli.php)
- [![Logo MYSQL](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTRCxvAI4YVRO6t5pEgOyjNMBhRmLhlcQA5Fg&s)](https://www.php.net/manual/es/book.mysqli.php)
