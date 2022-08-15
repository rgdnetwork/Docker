# Guía de instalacion de Docker

## Índice: 
- [Guía de instalación](https://github.com/rgdnetwork/Docker#para-ello-es-importante-saber-que-tenemos-que-ser-root-para-poder-instalar-docker-en-nuestra-m%C3%A1quina-de-forma-sencilla)
- [Comandos de Docker](https://github.com/rgdnetwork/Docker/blob/Docker/Comandos.md)
- [Licencia](https://github.com/rgdnetwork/Docker/blob/Docker/LICENSE)

## ¡Para ello es importante saber que tenemos que ser root para poder instalar docker en nuestra máquina de forma sencilla!

El primer paso y más importante es instalar git en nuestra máquina, para ello usaremos el siguiente comando: ```apt install git -y```

Cuando el proceso haya finalizado deberemos de clonar el repositorio, para ello os dejo aquí el comando al completo con el enlace del repositorio. ```git clone https://github.com/rgdnetwork/Docker.git```

Si ejecutamos el comando ```ls``` observaremos que se nos ha añadido una carpeta que se llama ```Docker```, para acceder a la carpeta ejecutamos el siguiente comando, ```cd Docker/```

Dentro de la carpeta Docker ejecutaremos el comando ```ls``` y vemos que tenemos varios archivos pero el que mas nos interesa es el que se llama ```docker_install.sh```, para ejecutar el instalador usaremos el siguiente comando, ```sh docker_install.sh```

## Y ya tendriamos docker instalado pero para comprobarlo usaremos el comando ```docker --version```.

