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


