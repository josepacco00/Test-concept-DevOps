my-app/
├── src/
│   ├── App.js
│   ├── index.js
│   ├── index.css
├── public/
│   └── index.html
├── tailwind.config.js
├── postcss.config.js
├── package.json
├── Dockerfile
├── nginx.conf



prueba de concepto devops - front

docker build -t my-app . --> construir la imagen
docker builder prune -f --> borrar cache si hay error en la construcción de la imagen
docker run -d -p 80:80 my-app en local --> levantar el contenedor+

******************

docker exec -it <container_id> /bin/sh --> entrar al contenedor
~ # cd /usr/share/nginx/html --> entrar al directorio donde se encuentran los archivos compilados