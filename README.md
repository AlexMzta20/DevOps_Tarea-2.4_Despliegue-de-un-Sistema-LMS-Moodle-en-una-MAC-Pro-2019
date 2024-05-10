# Despliegue de un Sistema LMS Moodle con GitHub/Docker en una Mac Pro 2019
## Instalar y ejecutar Moodle como contenedor
Como **buena práctica** primero debemos iniciar creando una carpeta en donde desarrollaremos todo el proyecto.
1. Crear una carpeta con el nombre que deseemos, en este caso la carpeta se llamará "**Moodle**". Usamos el siguiente
comando para crear carpetas en ***Linux***:
```
$ mkdir Moodle
```
2. Nos pasamos a la carpeta Moodle\ en donde realizaremos toda la actividad, usando el siguiente comando:
```
$ cd Moodle\
```
![Creación de la carpeta](https://github.com/AlexMzta20/DevOps_Tarea-2.4_Despliegue-de-un-Sistema-LMS-Moodle-en-una-MAC-Pro-2019/assets/105833304/d6dc3721-f9ee-4098-a77f-fa75adba9028)

3. Tenemos que correr la aplicación para obtener la aplicación de Moodle y la base de datos, usamos el archivo docker.yml. 
Usamos el siguiente comando:
```
$ url -sSL https://raw.githubusercontent.com/bitnami/containers/main/bitnami/moodle/dockercompose.yml > docker-compose.yml
```
4. Luego, para levantar el repositorio, hay que poner el siguiente comando:
```
$ docker compose up
```
![Levantamos el Moodle](https://github.com/AlexMzta20/DevOps_Tarea-2.4_Despliegue-de-un-Sistema-LMS-Moodle-en-una-MAC-Pro-2019/assets/105833304/e3bc09e3-0fbd-4f2b-bd3b-87b1cc5da133)

![Ejecutando el comando](https://github.com/AlexMzta20/DevOps_Tarea-2.4_Despliegue-de-un-Sistema-LMS-Moodle-en-una-MAC-Pro-2019/assets/105833304/c39ff6b1-46d4-4aad-8517-e3bfbb464735)

![Finalización del comando](https://github.com/AlexMzta20/DevOps_Tarea-2.4_Despliegue-de-un-Sistema-LMS-Moodle-en-una-MAC-Pro-2019/assets/105833304/dbab5658-db55-4b83-876f-cf7ec283c5a3)

5. Debemos ir al navegador y si colocamos "_localhost_" deberíamos visualizar la página de inicio de Moodle.

![Verificando que funciona el Moodle](https://github.com/AlexMzta20/DevOps_Tarea-2.4_Despliegue-de-un-Sistema-LMS-Moodle-en-una-MAC-Pro-2019/assets/105833304/7d7bb899-8cc1-4dd6-8c73-80d0401b85f5)

6. Usando el usuario y contraseña que nos proporciona Moodle tenemos acceso al login e iniciamos sesión.

![Usuario y contraseña](https://github.com/AlexMzta20/DevOps_Tarea-2.4_Despliegue-de-un-Sistema-LMS-Moodle-en-una-MAC-Pro-2019/assets/105833304/6bbacb24-3f70-44b1-9122-4d28d3dfb452)
>**Nota:** _Usuario y contraseña que debemos ingresar para tener acceso._

![Acceso al login](https://github.com/AlexMzta20/DevOps_Tarea-2.4_Despliegue-de-un-Sistema-LMS-Moodle-en-una-MAC-Pro-2019/assets/105833304/9299af7d-b7c1-44c3-868b-76c6cddd6c3d)

![Inicio del Moodle](https://github.com/AlexMzta20/DevOps_Tarea-2.4_Despliegue-de-un-Sistema-LMS-Moodle-en-una-MAC-Pro-2019/assets/105833304/27c14457-f0ea-4af2-b4ed-96bc1492ac66)
>**Nota:** _La siguiente imagen muestra la pagina de inicio del administrador._

7. 
