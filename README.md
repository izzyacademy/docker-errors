

## Common Docker Errors and How to Resolve Them

Example 1: Got permission denied while trying to connect to the Docker daemon socket

````bash
sudo chmod 666 /var/run/docker.sock
````

Example 2: Server: ERROR: Got permission denied while trying to connect to the Docker daemon socket

````bash
sudo newgroup docker
sudo chmod 666 /var/run/docker.sock
sudo usermod -aG docker ${USER}
````

Example 3: dial unix /var/run/docker.sock: connect: permission denied

````bash
sudo setfacl --modify user:<user name or ID>:rw /var/run/docker.sock
````
Example 4: Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock:

````bash
newgrp docker
````

Retrieved from:

https://newbedev.com/shell-got-permission-denied-while-trying-to-connect-to-the-docker-daemon-socket-at-unix-var-run-docker-sock-get-http-2fvar-2frun-2fdocker-sock-v1-24-containers-json-all-1-dial-unix-var-run-docker-sock-connect-permission-denied-code-example
