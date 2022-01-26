#Informacion del examen

Puertos utilizados:
  - *web*: 4000
  - *api1*: 3000
  - *api2*: 3000
  - *proxy*: 80

1.- **Para arrancar las aplicaciones directamente (webserver.js y apiserver.js)**

Con esto ejecutamos directamente las aplicaciones.

node webserver.js

node apiserver.js

2.- **Para arrancar aplicaciones con docker run**

%CD% Esto es el path del directorio actual.

Docker run –it –v %CD%: /app –w /app node node webserver.js

3.- **Para arrancar aplicaciones orquestadas**

Teniendo el docker-compose hecho lo construimos y despuÈs lo levantamos.

Docker-compose build

Docker-compose up

Link del Github
https://github.com/AnderGamer10/Examen-docker 
