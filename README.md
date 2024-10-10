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
## 5. Crea un contenedor con el nombre 'dam_alp2'. ¿Puedes hacer ping entre los contenedores?

Para crear el contenedor hacemos
```
docker run -it -d --name dam_alp2 alpine
```
Ahora vemos la ip del contenedor
```
docker inspect dam_alp2 | grep "IPAddress"
```
Entramos en el archivo dam_alp1 y ponemos la IP del dam_alp2
```
docker exec -it dam_alp1 sh
ping Ip dam_alp2
```
## 6.  Sal del terminal, ¿qué ocurrió con el contenedor?

Salimos de la terminal y vemos el contenedor
```
exit
docker ps -a
```

Lo que pasa es que siguen ejecutándose después de salir

## 7. ¿Cuanta memoria en el disco duro ocupaste?
Para ver la memoria que ha utilizado
```
docker system df
```




