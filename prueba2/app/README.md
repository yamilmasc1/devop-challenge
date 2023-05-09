<h1>Para compilar y desplegar la aplicacion entregada en una PC local es necesario:</h1>

1) Descargar los archivos de la carpeta prueba2 brindada en este repositorio:
2) Una vez descargados es necesario extraerlos en la pc en la que se va a realizar el despliegue.
3) Si ha extraido correctamente, deberia contar con una carpeta llamada app, la cual dentro incluye 2 subdirectorios: backend y frontend.
4) El paso siguiente es iniciar docker desktop si esta en un entorno windows, o descargar los paquetes de requisitos previos de linux y luego agregar los repositorios de docker.
5) Una vez que docker se encuentra corriendo en el ordenador se debe hacer lo siguiente.
6) Desde la terminal del dispositivo, debemos situarnos en el directorio en el que poseemos los archivos de la aplicacion.
7) Lo primero que haremos es ubicarnos en el subdirectorio llamado frontend y procederemos a crear la imagen del mismo:
    Para crear una imagen debemos de utilizar el siguiente comando: docker build -t <nombre-de-la-imagen> .
8) Luego procederemos a realizar la misma accion, pero crearemos la imagen de nuestro backend.
9) Una vez creada ambas imagenes procederemos a realizar el despliegue de nuestro docker-compose.
  Nos situaremos en la carpeta raiz que contiene el directorio frontend y backend, y desde la terminal digitaremos el siguiente comando:
    docker-compose up
10)Una vez que los servicios esten en ejecucion, se puede verificar la funcionalidad de la aplicacion accediendo a la direccion URL http://localhost:3000 .
  La aplicacion deberia estar disponible y funcionando correctamente.

    
