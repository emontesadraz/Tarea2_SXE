# DOCKER
*Esteban Miguel Montes Adraz* - *2 DAM* - *SXE*


## 1. Descarga la imagen "alpine" sin arrancarla y comprueba que está en tu equipo

Primero descargamos el alpine
```
docker pull alpine
```
Para verificar que se ha descargado
```
docker images
```

## 2. Crea un contenedor sin ponerle nombre. ¿Está arrancado? Obtén el nombre.
Creamos un contenedor con la imagen Alpine, pero sin especificar un nombre para él.
```
docker run -d alpine
```
Para verificar que está arrancado utilizamos este comando
```
docker ps -a
```
## 3. Crea un contenedor con el nombre 'dam_alp1'. ¿Cómo puedes acceder a él?
Para crear un contenedor con nombre
```
docker run -it -d --name dam_alp1 alpine
```
Para acceder al contendor utilizamos este comando
```
docker exec -it dam_alp1 sh
```
## 4. Comprueba que ip tiene y si puedes hacer un ping a google.com

Para ver la ip de nuestro archivo utilizamos este comando
```
docker inspect dam_alp1 | grep "IPAddress"
```

Para ver si podemos hacer ping desde dentro del fichero
```
ping google.com
```




