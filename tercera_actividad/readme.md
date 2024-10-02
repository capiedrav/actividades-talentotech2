# TalentoTech - Tercera Actividad - Seguridad en Contenedores

## Aplicación Basada en el Django REST Framework (DRF) [Quickstart Guide](https://www.django-rest-framework.org/tutorial/quickstart/)

### Como ejecutar

1. Crear la imagen: ```docker image build -t tercera_actividad_img .```
2. Crear el contenedor: ```docker container run -d -p 8000:8000 --memory=256m --cpus=0.5 --name tercera_actividad_ctr tercera_actividad_img```
3. Para acceder a la terminal del contenedor de forma interactiva: ```docker container exec -it tercera_actividad_ctr  /bin/bash```
4. Acceder a la aplicación: ```http://127.0.0.1:8000/``` o ```http://localhost:8000/```
5. Para detener el contenedor: ```docker container stop tercera_actividad_ctr```
6. Para eliminar el contenedor: ```docker container rm tercera_actividad_ctr```
7. Para eliminar la imagen: ```docker image rm tercera_actividad_img:latest```
