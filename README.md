# Entorno PHP para clase

Entorno mínimo para aprender PHP con Docker:

- PHP + Apache
- MySQL
- phpMyAdmin
- MySQL accesible desde el ordenador anfitrión

## Arrancar

```bash
docker compose up -d --build
```

## Direcciones

- PHP: http://localhost:8080
- phpMyAdmin: http://localhost:8081

## Acceso MySQL desde fuera de Docker

Usa estos datos en DBeaver, MySQL Workbench, DataGrip, etc.:

- Host: `localhost`
- Puerto: `3307`
- Base de datos: `clase`
- Usuario: `alumno`
- Contraseña: `alumno`

Dentro de Docker, PHP no usa `localhost:3307`. Usa:

- Host: `mysql`
- Puerto: `3306`

## Parar

```bash
docker compose down
```

Los datos de MySQL se conservan en el volumen `mysql_data`.

Para borrar también la base de datos:

```bash
docker compose down -v
```
