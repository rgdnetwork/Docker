## :whale: Docker
### :rocket: Puesta en marcha y uso
#### Servicio :battery:
*Iniciar Docker Desktop*
~~~
systemctl --user start docker-desktop
~~~

*Habilitar que se inicie Docker Desktop al iniciar sesión*
~~~
systemctl --user enable docker-desktop
~~~

*Detener Docker Desktop*
~~~
systemctl --user stop docker-desktop
~~~

*Comprobar estado (Funcionamiento) Docker Desktop*
~~~
systemctl --user status docker-desktop
~~~
#### Images :cd:
~~~
docker images
~~~
~~~
docker pull image_name
~~~
~~~
docker image rm image_name:version_name/tag
~~~
#### Containers :railway_car:
Es necesario tener una imagen descargada, que sirva de base para la creación del contenedor.
~~~
docker create base_image

or

docker container create base_image

// 1b7115454b0dbac035f8703cee028869779dbd923101b62041007eae354e4dee
// Devolverá una línea de caracteres -> Se trata del identificador del contenedor creado
~~~
~~~
docker start container_id
~~~
~~~
docker ps
~~~
~~~
docker stop container_id
~~~
~~~
docker rm container_name
~~~
~~~
docker create --name container_name base_image
~~~

:electric_plug: Concepto de ***Port Mapping*** en contenedores :electric_plug:
~~~
docker create -p27017:27017 --name container_name image_name
// host_port:container_port
~~~
~~~
docker create -p27017 --name container_name image_name
// ...:container_port -> de esta forma, es docker quién establece el puerto del host para el mapeo
~~~
~~~
docker logs container_name

or

docker logs container_id

// Comprobar si nuestro servidor de mongo se ha ejecutado de forma correcta
~~~
~~~
docker logs --follow container_name

or

docker logs --follow container_id

// Comprobar si nuestro servidor de mongo se ha ejecutado de forma correcta - Mongo se queda escuchando los logs (tiempo real)
~~~
:cyclone: El comando ***docker run*** :cyclone:
> :books: **Checks or steps:**
- Comprueba si se encuentra la imagen y, si no existe, la descarga
- Crea un contenedor usando la imagen anterior
- Inicia dicho contenedor
~~~
docker run image_name
// Al no encontrar la imagen, pasa a descargarla
// Inmediatamente después, mongo se pone a la escucha de logs
~~~
~~~
docker run -d image_name
// La opción dettached, evita que el servicio se ponga a la escucha de logs
~~~
- Se pueden aplicar todas las opciones anteriores (aplicadas a comandos individuales) al comando *docker run*
~~~
docker run --name container_name -phost_port:container_port -d image_name
// Ejemplo: docker run --name monguito -p27017:27017 -d mongo
~~~
