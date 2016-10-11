# Feed-The-Beast Departed (Minecraft 1.7.10) in a Docker Container
To pull the image:
```
docker pull audiohacked/ftb_departed:1.4.0
```
*Optional*: Run data container:
```
docker run --name ftb_cloud9_data audiohacked/ftb_departed:1.4.0 true
```

Then, run the server container:
```
docker run --detach --interactive --tty \
    --name ftb_departed \
    --volumes-from ftb_departed_data \
    -p 25565:25565 \
    -e EULA=TRUE \
    audiohacked/ftb_departed:1.4.0
```
