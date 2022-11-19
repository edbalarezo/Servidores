# Servidores
Servidor postgresql y pgamin

>> Postgresql

- docker run -d --name dbpsql -e POSTGRES_PASSWORD=admin  -p 5432:5432 postgres

![image](https://user-images.githubusercontent.com/91167211/200640495-e8994bc9-b8d2-480a-b2a3-16acea4cc49e.png)

>>PGadmin

- docker run -d --name pgadmin -p 8090:80 -e PGADMIN_DEFAULT_EMAIL=edbalarezo@sudamericano.edu.ec -e PGADMIN_DEFAULT_PASSWORD=admin dpage/pgadmin4

![image](https://user-images.githubusercontent.com/91167211/200640970-cf3c4f20-a9a3-47c6-90e3-fffffc9ab277.png)

>> Creamos una red (redsuda)

- docker network create --attachable redsuda

![image](https://user-images.githubusercontent.com/91167211/200641329-3c5328aa-f684-43ad-920e-1336ba5cd6f6.png)

>>Agregamos contenedores a la red 

- Contenedor de postgresql: docker network connect redsuda dbpsql
- Contenedor de pagadmin: docker network connect redsuda pgadmin

![image](https://user-images.githubusercontent.com/91167211/200641456-1cdfc67e-9a76-409e-9b16-aad049e11f89.png)

>> Verificamos contenedores conectados a la red

docker inspect redsuda

![image](https://user-images.githubusercontent.com/91167211/200641670-486332f7-4a9d-4286-a9aa-3b665009b489.png)

![image](https://user-images.githubusercontent.com/91167211/200641708-acab6992-4316-4f0d-a11b-3a4b9f4cc910.png)

![image](https://user-images.githubusercontent.com/91167211/200641749-1290e6ea-652c-4f2c-a2b8-14fec0f660b4.png)

>> Abrimos el puerto 8090 e iniciamos sesión 

![image](https://user-images.githubusercontent.com/91167211/200642049-dd12da4d-2643-45b8-814c-fd6cb87fe252.png)

- Creamos una base de datos

![image](https://user-images.githubusercontent.com/91167211/202855503-458087ad-bbff-4edc-a16a-82e1beb6282f.png)
