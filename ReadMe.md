## Introduction

### Why container?
1. They are light wait and don't need much resources.

### Getting Started
1. Install Docker(Continer Engine) on your system.
2. Check the version using the below commands
    ``` 
    $ docker --version
    Docker version 17.12, build c97c6d6

    $ docker-compose --version
    docker-compose version 1.20.0, build 8dd22a9

    $ docker-machine --version
    docker-machine version 0.14.0, build 9ba6da9 
    ```
3. Open a command-line terminal and test that your installation works by running the simple Docker image, hello-world:
    ```
    $ docker run hello-world

    Unable to find image 'hello-world:latest' locally
    latest: Pulling from library/hello-world
    ca4f61b1923c: Pull complete
    Digest:     sha256:ca0eeb6fb05351dfc8759c20733c91def84cb8007aa89a5bf606bc8b3    15b9fc7
    Status: Downloaded newer image for hello-world:latest

    Hello from Docker!
    This message shows that your installation appears to be working     correctly.
    ...

    ```
4. Start a Dockerized web server. Like the hello-world image above, if the image is not found locally, Docker pulls it from Docker Hub.
    ```
    $ docker run -d -p 80:80 --name webserver nginx
    ```
5. In a web browser, go to http://localhost/ to view the nginx homepage. Because we specified the default HTTP port, it isn’t necessary to append :80 at the end of the URL.
6. Use the below commands to list,stop container and list,remove images.
    ```
    $ docker container ls
    $ docker container stop webserver
    $ docker container ls -a
    $ docker container rm webserver
    $ docker image ls
    $ docker image rm nginx
    ```
