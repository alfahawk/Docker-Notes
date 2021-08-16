# Docker-Notes
Amigos Code Docker Notes

Docker Amigoscode Tutorial Notes

Docker run nginx:latest

Runs the nginx image of the latest tag

Docker run -d nginx:latest

Runs the nginx image of the latest tag in detach mode

Docker run -p 8080:80 nginx:latest

Runs the nginx image of latest tag from the 8080:80 port

8080:host port
80 container port

Docker run -d -p 8080:80 -p 3000:80 nginx:latest

Runs the nginx image of latest tag from the 8080:80, 3000:80 ports (Multiple Ports)

Docker stop mystifying_diffie

Stops the container named  mystifying_diffie

Docker start mystifying_diffie

Starts the container named  mystifying_diffie

Docker stop 6161fef37ad5 

Stops container for 6161fef37ad5 id

Docker ps -a 

Show all container 

docker rm aba0b62f936b

Removes the container for 6161fef37ad5 id 

docker ps -aq

List all container id 

docker rm $(docker ps -aq)

Remove all containers

docker rm -f $(docker ps -aq)

Removes all containers forcely even running containers

docker run --name website -d -p 8080:80 -p 3000:80 nginx:latest

Change container name to website 

export FORMAT="ID\t{{.ID}}\nNAME\t{{.Names}}\nIMAGE\t{{.Image}}\nPORTS\t{{.Ports}}\nCOMMAND\t{{.Command}}\nCREATED\t{{.CreatedAt}}\nSTATUS\t{{.Status}}\n"

Docker format

docker ps --format=$FORMAT

docker run -d -p 9090:80 -v $(pwd):/usr/share/nginx/html:ro  nginx

Volume example... change default nginx landing page

Mounted read only. you can not change from container side.. container read only.

docker run --name website-copy --volumes-from laughing_roentgen -d -p 8081:80 nginx

Volumes between containers example

Docker build --tag website:latest .

Build from docker file command with tag


docker tag landing:latest landing:v2

Create new tag from old image(change the tag)

docker tag website:latest 151501014/website:latest

Docker tag name for pushing to hub

docker push 151501014/website:v2

docker push 151501014/website:latest

Docker push command



