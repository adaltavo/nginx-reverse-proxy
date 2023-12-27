# nginx-reverse-proxy

This repo serves as a bare start point for a nginx reverse proxy server.
The idea behind this is being able to manage multiple web apps withing the same server using Docker containers. Nginx will take
all the http requests and will redirect them to their corresponding web app container.

You need to configure nginx putting your config files within the `conf` directory. After that, you may use `docker compose up -d` to 
start the nginx reverse proxy container and start redirecting the request. A network called `nginx-proxy` is also created for you to 
add more containers for redirections. Remember, when you add a container to a network you may communicate with it using it's container or service name (make sure to use `--name` parameter when running `docker run`).
