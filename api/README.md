## Docker

Sigue los siguientes pasos para correr el proyecto en tu máquina local.

**Paso 1.** Descargar y clonar el repositorio en la rama _master_.

**Paso 2.** Ejecutar _docker-compose up -d webserver php-fpm mysql_ para descargar las imágenes y crear los contenedores.

**Paso 3.** Hacer una copia del archivo _.env_ con el nombre _.env.local_ para agregar tu configuración.

**Paso 4.** Modificar el archivo _.env.local_ con los datos de conexión de la base de datos:

```bash
DATABASE_URL=mysql://demo:demo@mysql:3306/symfony_api_platform
```

**Paso 5.** Correr _docker exec -it symfony-api-platform-php-fpm composer install_ para instalar las librerías.

**Paso 6.** Correr _docker exec -it symfony-api-platform-fpm php bin/console doctrine:schema:update --force_ para crear la tablas en la base de datos.

**Listo.** Ahora puedes ingresar desde tu navegador [http://localhost:14000](http://localhost:14000).