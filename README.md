<p style="text-align: center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p style="text-align: center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

# Proyecto empresas

## Inicialización del proyecto

Creación del proyecto
```shell
laravel new Empresas
cd Empresas
```

Instalación de Breeze
```shell
composer require "laravel/breeze"
php artisan breeze:install
```

Instalación de dependencias
```shell
npm install
```

## Poner en servicio la base de datos

### Usaremos un contenedor Docker

[Docker mysql con phpmyadmin](./docker-compose.yml)

Para ello lo levantamos
```shell
docker compose up -d
```
### Configuramos el archivo '.env'
Para ello añadimos los valores necesarios para conectar con la base de datos
```
DB_CONNECTION=mysql <nomv¡bre del servicio>
DB_HOST=127.0.0.1
DB_PORT=3306 <puerto que usemos>
DB_DATABASE=empresas <nombre de la base de datos>
DB_USERNAME=<usuariio>
DB_PASSWORD=<password>
```
En el [archivo](./.env) mencionado.

### Generamos las tablas necesarias en la base de datos

Se ejecuta
```shell
php artisan migrate
```
## Lanzamos el servidor de laravel

Para comprobar que todo funciona lanzamos el servidoer de laravel

```shell
php artisan serve &
```
