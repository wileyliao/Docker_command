# Docker_command

## Build Image
`docker build -t <image_name>:<image_label> .` 
</br>
>- `-t`: asign the tag of this image
>- `<image_name>`: name of this image
>- `<image_label>`: version, default = 'latest'
>- `.`: current folder

## Container
>- Run(build)
`docker run --name <container_name> -p port_1:port_2 <image name>:<image_label>`

>- Run existing container
`docker start <container_name>`

## Network
>- List all network: </br>
`docker network ls` </br>
>- Create new network: </br>
`docker network create <network_name>` </br>
>- Dekete exist network: </br>
`docker network rm <network_name>` </br>
>- Check detail of a network: </br>
`docker network inspect <network_name>` </br>
