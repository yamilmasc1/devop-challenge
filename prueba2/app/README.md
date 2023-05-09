<h1>Para compilar y desplegar la aplicacion entregada en una PC local es necesario:</h1>

1) Descargar los archivos de la carpeta prueba2 brindada en este repositorio:
2) Una vez descargados es necesario extraerlos en la pc en la que se va a realizar el despliegue.
3) Si ha extraido correctamente, deberia contar con una carpeta llamada app, la cual dentro incluye 2 subdirectorios: backend y frontend.
4) El paso siguiente es iniciar docker desktop si esta en un entorno windows, o descargar los paquetes de requisitos previos de linux y luego agregar los repositorios de docker.
5) Una vez que docker se encuentra corriendo en el ordenador se debe hacer lo siguiente.
6) Desde la terminal del dispositivo, debemos situarnos en el directorio en el que poseemos los archivos de la aplicacion.
7) Lo primero que haremos es ubicarnos en el subdirectorio llamado frontend y procederemos a crear la imagen del mismo:
    Para crear una imagen debemos de utilizar el siguiente comando: <b>docker build -t <nombre-de-la-imagen> .</b>
8) Luego procederemos a realizar la misma accion, pero crearemos la imagen de nuestro backend.
9) Una vez creada ambas imagenes procederemos a realizar el despliegue de nuestro docker-compose.
  Nos situaremos en la carpeta raiz que contiene el directorio frontend y backend, y desde la terminal digitaremos el siguiente comando:
    <b>docker-compose up</b>
10)Una vez que los servicios esten en ejecucion, se puede verificar la funcionalidad de la aplicacion accediendo a la direccion URL http://localhost:3000 .
  
 La aplicacion deberia estar disponible y funcionando correctamente.

<h2>Para desplegar la aplicacion en la nube (AWS) es necesario:</h2>
    
1)Para desplegar un docker-compose en AWS es necesario crear una instancia de Amazon EC2. Esto se puede hacer desde la consola AWS o mediante herramientas como AWS CLI.

2) Conectarse a la instancia mediante SSH. Se debe hacer utilizando la clave de acceso que se proporciona cuando se crea la instancia.

3)Instalar docker en la instancia de EC2. Esto se puede hacer mediante el uso de los siguientes comandos:
   <b> sudo yum update -y
    sudo amazon-linux-extras install docker -y
    sudo service docker start
    sudo usermod -a -G docker ec2-user </b>
 
4)Descargar los archivos en donde se encuentra el docker-compose.yaml en la instancia. Esto se puede hacer mediante el uso del comando wget o curl.

5)Ejecutar el comando <b> docker-compose up -d</b> para iniciar los contenedores. Tene en cuenta que debes encontrarte en el mismo directorio que el archivo docker-compose.yaml antes de ejecutar el comando.

6) Una vez completados estos pasos, la aplicacion deberia estar en ejecucion en la instancia de EC2 y se deberia poder acceder a ella desde la direccion IP publica de la instancia.
    
