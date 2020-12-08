# DOCKER-COMPOSE-LAMP ES UN MARCO DE TRABAJO  DE LINUX APACHE  MYSQL Y PHP

éste repositorio contienen cambios en el Dockerfile del php71 en donde se le configuró el drivers extension SQLSRV

## Repositorio Original
 
 Url : https://github.com/sprintcube/docker-compose-lamp 

##  Instalación
 
* Clone el repositorio en su local
* Configure el .env requerido con el sample.env de base
* Run the `docker-compose up -d`.

```shell
git clone https://github.com/juanlll/docker-compose-lamp-php71sqlsrv
cd docker-compose-lamp/
cp sample.env .env
// modify sample.env as needed
docker-compose up -d
// visit localhost
```

##  Cambios realizados en el Dockerfile de php71

  ruta: docker-compose-lamp/bin/php71/Dockerfile
  
  ```shell
    RUN apt-get -y install unixodbc-dev
    RUN pecl install sqlsrv-4.1.6.1 pdo_sqlsrv-4.1.6.1
  ```
  ##  Cambios realizados en el php.ini 
  
  ruta: docker-compose-lamp/config/php/php.ini
  
  ```shell
    extension = sqlsrv.so
    extension = pdo_sqlsrv.so
  ```
  
  ## Agradecimientos 
 a https://www.facebook.com/groups/docker.es/ 
 
