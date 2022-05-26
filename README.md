# Nginx-Doker

1.En primer lugar, nos dirigimos a la web Docker hub y filtramos por nginx
![image](https://user-images.githubusercontent.com/91616284/170467200-63ed2f47-8bc5-4f5a-ae0e-c7d844c466d6.png)

2.Realizamos el pull sudo docker pull nginx
![image](https://user-images.githubusercontent.com/91616284/170467303-f909bbb1-a294-4b3a-9504-8e33947f3bbf.png)

3.Levantamos el contenedor que alberga el servicio nginx ejecutando el siguiente comando docker run --rm -d -p 8080:80 --name web nginx
![image](https://user-images.githubusercontent.com/91616284/170467574-19c2ee22-4c26-4e04-962b-788800b4e967.png)

4.Como podemos observar, si nos dirigimos al localhots:8080, nos encontraremos con la página default de nginx
![image](https://user-images.githubusercontent.com/91616284/170467693-49be8428-b98b-48c3-9889-656500ff8ccd.png)

5.A continuación, finalizamos o "matamos" al contenedor sudo docker stop web
![image](https://user-images.githubusercontent.com/91616284/170467835-69604d6b-bf3e-47c9-8cea-c702d904dd19.png)

6.Procedemos a crear el index.html que emplearemos en nuestro nginx
![image](https://user-images.githubusercontent.com/91616284/170468196-2f07806d-61a1-4dbc-b56a-b6a0c703371d.png)

![image](https://user-images.githubusercontent.com/91616284/170468136-611bb0b8-25bd-457b-971a-de80b3caf369.png)

7.Mapeamos el volumen para poder pasar ese index.html e implementarlo docker run --rm -d -p 8080:80 --name web -v ~/Home:/usr/share/nginx/html nginx
![image](https://user-images.githubusercontent.com/91616284/170468686-3ce46d9d-271d-44c6-a66d-924cd0b2d09e.png)

8.Como podemos observar, ahora si accedemos a nuestro hostlocal:8080, nos encontraremos con el index.html definido previamente.
![image](https://user-images.githubusercontent.com/91616284/170468731-767338ad-56fb-40a9-9c4a-d8a60539d0c3.png)
