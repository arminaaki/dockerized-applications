### Dockerized spotify
Spotify is now packaged in a **Docker** container 

### Usability
The spotify script mounts the X11 and pulseaudio sockets in the launcher container to the host. This allows the video/audio output to be rendered.



```sh
docker build -t spotify .
```
This will create the spotify image and install the required dependencies.
Once the image is ready, run the follwowing:

```sh
./spotify
```
