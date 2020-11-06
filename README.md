# projectjsf
 proyecto documentos


# Instalación
requiere [docker](https://www.docker.com/) to run.

en la raiz del proyecto:

# opcion 1
el proyecto ya tiene el arhivo war en el ./target, por tanto se puede desplegar con docker

```sh
$ docker-compose up --build
```
-debe estar libre el puerto 8080 para tomcat y 5432 para el servicio de postgresql. automaticamente creará la base de datos y desplegará el proyecto en tomcat ir a la url http://localhost:8080/app/


# opcion2
si se descarga se puede construir el proyecto con maven y desplegar con docker
```sh
$ mvn install
$ docker-compose up --build
```
-ir a la url http://localhost:8080/documento/

# NOTA
-en hibernate.cfg.xhtml se cambio la url jdbc:postgresql://postgresdb:5432/documento para que se conecte con el servicio de postgresql en docker-compose
si se desea probar sin docker, cambiar la linea a jdbc:postgresql://localhost:5432/documento y ejecutar el script int.sql para crear las tablas en la base de datos local

