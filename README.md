# Docker Command Reference

### before
wsl --install ubuntu

## Build Image
`docker build -t <image_name>:<image_label> .` 
</br>
>- `-t`: asign the tag of this image
>- `<image_name>`: name of this image
>- `<image_label>`: version, default = 'latest'
>- `.`: current folder of Dockerfile

## Push/Pull Image
`docker login` </br>
`docker tag <local ImageName>:<local ImageTag> username/<remote ImageName>:<Remote ImageTag>` </br>
>- or change `<local ImageName>:<local ImageTag>` to `<ImageID>` </br>

`docker push username/<remote ImageName>:<Remote ImageTag>` </br>
`docker pull username/<remote ImageName>:<Remote ImageTag>`

## Manage Container
>- Run(create and start) a container </br>
`docker run --gpus all --name <container_name> --net <network_name> -p port_1:port_2 <image name>:<image_label>`
>- `--gpus all`: available GPU usage
>- `--name`: name of this container
>- `--net`: adding this container to an existing network
>- `-p port_1:port_2`: Network port mapping(port_1 -> Host, port_2 -> Container)

>- Start/Stop existing container </br>
`docker start <container_name>` </br>
`docker stop <container_name>`

## Network
>- List all network: </br>
`docker network ls` </br>
>- Create a new network: </br>
`docker network create <network_name>` </br>
>- Delete an existing network: </br>
`docker network rm <network_name>` </br>
>- Check detail of a network: </br>
`docker network inspect <network_name>` </br>

## Clean up
>- Remove a container: </br>
`docker rm <container_name>`
>- Remove an image: </br>
`docker rmi <image_name>:<image_label>`
>- Remove all unused resources: </br>
`docker system prune`
