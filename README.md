# Docker-commands :whale:

## Comandos para docker:

#### - Ver la versión de docker que tenemos instalada en nuestra máquina.
```docker --version```

## Imágenes

#### - Como descargar la imagen desde Dockerhub.
```docker pull [nombre de la imagen]```
Ejemplo: ```docker pull mongo``` si no especificamos la versión que deseamos de usar se nos descargará siempre la última versión de la imagen.

Si deseamos descargar una versión en específico de la imagen deberemos de usar el siguiente comando ```docker pull [nombre de la imagen]:[versión]```
Ejemplo: ```docker pull mongo:4.2```

#### Comando para construir una imagen desde un dockerfile.
```docker image build```

#### - Comando para eliminar imágenes.
```docker rmi [nombre o id de la imágen]```
Ejemplo: ```docker rmi mongo```

#### - Comando para ver las imágenes que tenemos instaladas en nuestra máquina.
```docker images```

## Contenedores

#### - Comando para descargar y correr el contenedor con las imagenes de Dockerhub.
```docker run [nombre de la imagen]``` 
Ejemplo: ```docker run mongo```

#### - Comando para crear un contendor desde una imagen.
```docker create [nombre de la imagen o id]``` Ejemplo: ```docker create mongo```

#### - Comando para crear contenedores asignando un nombre en específico.
```docker create --name [nombre que queramos ponerle] [nombre o id de la imagen]```
Ejemplo: ```docker create --name my.name mongo```

#### - Comando para iniciar un contenedor.
```docker start [nombre o id del contenedor]```
Ejemplo: ```docker start mongo```

#### - Comando para ver los contenedores que estan corriendo.
```docker ps```

#### - Comando para parar un contenedor.
```docker stop [nombre o id del contenedor]```
Ejemplo: ```docker stop mongo```

#### - Comando para ver los contenedores que no estan corriendo.
```docker ps -a```

#### - Comando para eliminar un contenedor.
```docker rm [nombre o id del contenedor]```
Ejemplo: ```docker rm my.name```

## Network

#### Comando para crear una network.
```docker network create [opción de la red que deseamos crear] [nombre que le queramos poner a la network]```
Ejemplo: ```docker network create bridge my.network```










