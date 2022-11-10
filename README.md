# tomcat-docker-compose

```
version: "3.9"

services:
 nginx:
   image: nginx:alpine
   ports:
    - "80:80"
   restart: always

 tomcat:
   depends_on:
     - nginx
   image: tomcat:8
   ports:
     - "8080:8080"
   restart: always
````
