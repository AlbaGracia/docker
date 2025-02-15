# Documento técnico Despliegue de Wordpress

Descripción de la arquitectura y configuración de los servicios desplegados mediante Docker y Docker Compose.
Se han creado 3 contenedores: MySQL, WordPress y PhpMyAdmin, creando un entorno de desarrollo para una aplicación de WordPress con una base de datos MySQL.

## Arquitectura

Arquitectura basada en **Docker** con diferentes servicios alojados en contenedores, y estos estan conectados entre sí mediante diferentes redes privadas.
Toda la arquitectura está definida en el archivo [docker-compose.yml](./docker-compose.yml).

Se han configurados dos redes, `backend-network` a la que no se tiene acceso desde fuera pero todos los contenedores estarán configurados dentro de la misma, principalmente se encuentra el contenedor de *mysql* y `frontend-network` la cuál es accesible desde fuera pero solo perteneceran los contenedores de *wordpress* y *phpmyadmin*.

