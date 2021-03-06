# docker-web-app

Multi-stage Dockerization of a web application based on Angular Client and a Java Server. Both client and server Dockerfiles execute some building process in development environments (nodejs for client and maven for server) previous to deploy both artifacts in nginx and tomcat respectively.

**Need to change**
- Server context in the [reverse-proxy config](https://github.com/cbelda/docker-web-app/blob/master/reverse-proxy/nginx.conf#L10)
- Server path (and name) in the [server Dockerfile](https://github.com/cbelda/docker-web-app/blob/master/java/Dockerfile#L11)

Once configured, run `docker-compose up` and go to `http://dockerhost:8080`.

![](https://user-images.githubusercontent.com/20857839/36028242-8998f41c-0d9e-11e8-93b3-6bfe50152bf8.png)
