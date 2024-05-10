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

5. Para verificar que el servicio de Moodle está activo usamos el siguiente comando:
```
$ docker ps
```
![Comprobar servicio de Moodle activo](https://github.com/AlexMzta20/DevOps_Tarea-2.4_Despliegue-de-un-Sistema-LMS-Moodle-en-una-MAC-Pro-2019/assets/105833304/90824487-10ef-4f5b-bf0c-a0d5153eb33d)
>**Nota:** _Este paso se realiza para verificar que el contenedor de nuestro servicio de Moodle si se haya creado correctamente y este funcionado sin problemas._

6. Debemos ir al navegador y si colocamos "_localhost_" deberíamos visualizar la página de inicio de Moodle.

![Verificando que funciona el Moodle](https://github.com/AlexMzta20/DevOps_Tarea-2.4_Despliegue-de-un-Sistema-LMS-Moodle-en-una-MAC-Pro-2019/assets/105833304/7d7bb899-8cc1-4dd6-8c73-80d0401b85f5)

## Configuración de Moodle

1. Usando el usuario y contraseña que nos proporciona Moodle tenemos acceso al login e iniciamos sesión. Hacemos clic en la opción "***Log In***" de la parte superior derecha. Se nos proporcionan las credenciales por defecto y son las siguientes:
- **Usuario:** user
- **Contraseña:** bitnami

![Usuario y contraseña](https://github.com/AlexMzta20/DevOps_Tarea-2.4_Despliegue-de-un-Sistema-LMS-Moodle-en-una-MAC-Pro-2019/assets/105833304/6bbacb24-3f70-44b1-9122-4d28d3dfb452)
>**Nota:** _Usuario y contraseña que debemos ingresar para tener acceso._

![Acceso al login](https://github.com/AlexMzta20/DevOps_Tarea-2.4_Despliegue-de-un-Sistema-LMS-Moodle-en-una-MAC-Pro-2019/assets/105833304/9299af7d-b7c1-44c3-868b-76c6cddd6c3d)

![Inicio del Moodle](https://github.com/AlexMzta20/DevOps_Tarea-2.4_Despliegue-de-un-Sistema-LMS-Moodle-en-una-MAC-Pro-2019/assets/105833304/27c14457-f0ea-4af2-b4ed-96bc1492ac66)
>**Nota:** _La anterior imagen muestra la página de inicio del administrador._

## Poner Moodle en marcha para la configuración anterior
1. Después de la configuración anterior, hay que crear un curso llamado “**Curso 1**”. Para ello vamos al apartado de ***My courses*** y agregamos un nuevo curso, el cual tendrá el nombre antes mencionado.

![Home](https://github.com/AlexMzta20/DevOps_Tarea-2.4_Despliegue-de-un-Sistema-LMS-Moodle-en-una-MAC-Pro-2019/assets/105833304/1030fb9a-04c2-44cc-9ebb-f5bf7cade80f)

2. Nos mostrará la siguiente ventana en donde podremos añadir el nombre del curso, colocamos su nombre corto del curso y le asignamos una categoría. Finalmente, solo le damos a crear.

![Crear curso llamado Curso 1](https://github.com/AlexMzta20/DevOps_Tarea-2.4_Despliegue-de-un-Sistema-LMS-Moodle-en-una-MAC-Pro-2019/assets/105833304/544787dc-dcb0-4cc5-9a23-f28bc91b5f07)

3. Después de lo anterior, si lo hicimos correctamente podremos observar la pantalla del curso creado.

![Pantalla del curso creado](https://github.com/AlexMzta20/DevOps_Tarea-2.4_Despliegue-de-un-Sistema-LMS-Moodle-en-una-MAC-Pro-2019/assets/105833304/822581b6-40d6-4e4a-97ed-7aef6f6ad681)

4. Como siguiente punto hay que crear los siguientes Roles/Usuarios. Para ello vamos al apartado de ***/Site administration/Users/Add a new user*** y añadimos nuevos roles/usuarios:
- Como **administrador** del Moodle, alguno del Equipo.
- Como **profesor**, otro integrante del equipo.
- Todos los integrantes del equipo deben estar como **estudiantes**.

![Ir a crear usuario](https://github.com/AlexMzta20/DevOps_Tarea-2.4_Despliegue-de-un-Sistema-LMS-Moodle-en-una-MAC-Pro-2019/assets/105833304/913a08b1-b07f-44be-a586-a1c3da037590)

5. Creamos el primer usuario llamado "**Raúl Cáceres Escalante**" junto con su correo y contraseña correspondientes para poder accesar a su perfil.
- **Usuario:** _raul_
- **Contraseña:** _E5un53cret0!_
- **Nombre completo:** _Raúl Cáceres Escalante_
- **Dirección de correo:** _raul.ca@merida.tecnm..mx_

![Primer usuario](https://github.com/AlexMzta20/DevOps_Tarea-2.4_Despliegue-de-un-Sistema-LMS-Moodle-en-una-MAC-Pro-2019/assets/105833304/e40245bd-b55a-4641-b2e8-d25a75dec016)

6. Creamos el segundo usuario llamado "**Nury Colorado Pat**" junto con su correo y contraseña correspondientes para poder accesar a su perfil.
- **Usuario:** _nury_
- **Contraseña:** _E5un53cret0!_
- **Nombre completo:** _Nury Colorado Pat_
- **Dirección de correo:** _nury.co@merida.tecnm..mx_

![Segundo usuario](https://github.com/AlexMzta20/DevOps_Tarea-2.4_Despliegue-de-un-Sistema-LMS-Moodle-en-una-MAC-Pro-2019/assets/105833304/7c4b863b-81cd-4db2-b4b1-663ebd56daa1)

7. Creamos el tercer usuario llamado "**Angel Raymundo Can Aguilar**" junto con su correo y contraseña correspondientes para poder accesar a su perfil.
- **Usuario:** _raul_
- **Contraseña:** _E5un53cret0!_
- **Nombre completo:** _Angel Raymundo Can Aguilar_
- **Dirección de correo:** _angel.ca@merida.tecnm..mx_

![Tercer usuario](https://github.com/AlexMzta20/DevOps_Tarea-2.4_Despliegue-de-un-Sistema-LMS-Moodle-en-una-MAC-Pro-2019/assets/105833304/bbb2bfa6-53c5-41c5-983e-d02ab6e8d27d)

5. Creamos el cuarto usuario llamado "Enrique Alejandro Chuc Mezeta" junto con su correo y contraseña correspondientes para poder accesar a su perfil.
- **Usuario:** _enrique_
- **Contraseña:** _E5un53cret0!_
- **Nombre completo:** _Enrique Alejandro Chuc Mezeta_
- **Dirección de correo:** _enrique.ch@merida.tecnm..mx_

![Cuarto usuario](https://github.com/AlexMzta20/DevOps_Tarea-2.4_Despliegue-de-un-Sistema-LMS-Moodle-en-una-MAC-Pro-2019/assets/105833304/da0aecf3-ecd8-4003-8a6a-6690cc70bc7f)

6. Si todo lo hicimos correctamente, podremos visualizar todos los usuarios creados anteriormente al guardar los cambios. Como en la siguiente captura se aprecia:

![Visualización de usuarios](https://github.com/AlexMzta20/DevOps_Tarea-2.4_Despliegue-de-un-Sistema-LMS-Moodle-en-una-MAC-Pro-2019/assets/105833304/9f01e634-4d07-4df1-a599-52593f715b0f)

7. 
