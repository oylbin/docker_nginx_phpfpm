This project demonstrates how to use docker image to start a nginx + phpfpm 
application.

# Usage

1. start app stack

        docker stack deploy -c docker-compose.yml app

1. check status

        docker stack ls

        docker service ls

        docker container ls

1. connect shell in a running container ( alpine image only has /bin/sh )

        docker exec -i $container_id /bin/sh

1. remove app stack

        docker stack rm app

