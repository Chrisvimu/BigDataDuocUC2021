# BigDataDuocUC2021
All of the course materials will be put here.

## Contents for this docker env:

 - Hyper-v
 - Docker
 - VSCode or other text editor of choice.
 - Cloudera


 ## Setting up the Env:

    - Install your code editor of choice.
    - Install [Hyper-V](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/enable-hyper-v)

 ### Instaling Docker:

* [Download](https://docs.docker.com/get-docker/)
* [Follow the Hands-on tutorial](https://docs.docker.com/get-started/) *Optional*
* Config your docker for the cloudera img using Hyper-V and at least 10GB of Ram and 2 Virtual GPU.

### Instaling Cloudera

* Follow the oficial [documentation](https://medium.com/@dataakkadian/how-to-install-and-running-cloudera-docker-container-on-ubuntu-b7c77f147e03) here about how to do it.

TLDR, Execute this steps:
1. ` $  docker pull cloudera/quickstart:latest `
2. ` $  docker images `
    - You should be able to see *"cloudera/quickstart  latest  __ID__"* inside your images.
3. ` $  docker run --hostname=quickstart.cloudera --privileged=true -it -p 7180:7180 cloudera/quickstart /usr/bin/docker-quickstart `
    - You should have an active conection to root for the container, open a new terminal and run the following step.
4.  `$  docker ps`
    - You should see your cloudera container, if not try adding *-a* to the command.
5. Execute this on the cloudera terminal: `$  sudo /home/cloudera/cloudera-manager --express`
    - 