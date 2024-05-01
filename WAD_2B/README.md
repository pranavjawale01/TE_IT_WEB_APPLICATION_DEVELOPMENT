To create a Docker container environment using NVIDIA Docker or any other Docker runtime, you can follow these steps:

1. **Install Docker**: Make sure Docker is installed on your system. You can download and install Docker Desktop from the official Docker website: [https://www.docker.com/products/docker-desktop](https://www.docker.com/products/docker-desktop).

2. **Create Dockerfile**: Create a file named `Dockerfile` in your project directory with the following content:

    ```Dockerfile
    FROM node:alpine
    COPY . /test
    CMD ["node", "/test/test.js"]
    ```

    This Dockerfile specifies a Node.js Alpine image as the base, copies the contents of your project directory into a directory named `test` inside the container, and then runs the `test.js` file using Node.js when the container starts.

3. **Steps**: To execute docker
    PS C:\Users\HP\OneDrive\Desktop\PRACTICAL\WAD\WAD_2B\test> docker --version   
    Docker version 26.0.0, build 2ae903e
    PS C:\Users\HP\OneDrive\Desktop\PRACTICAL\WAD\WAD_2B\test> node --version     
    v20.11.0
    PS C:\Users\HP\OneDrive\Desktop\PRACTICAL\WAD\WAD_2B\test> node test.js       
    Hello, Welcome to the Docker!
    PS C:\Users\HP\OneDrive\Desktop\PRACTICAL\WAD\WAD_2B\test> docker build -t test .
    [+] Building 0.0s (0/0)  docker:default
    2024/05/02 01:18:15 http2: server: error reading preface from client //./pipe/[+] Building 0.0s (0/0)  docker:defaultosed
    2024/05/02 01:18:16 http2: server: error reading preface from client //./pipe/[+] Building 4.0s (7/7) FINISHED                               docker:default
    => [internal] load build definition from Dockerfile                     0.1s
    => => transferring dockerfile: 91B                                      0.0s
    => [internal] load metadata for docker.io/library/node:alpine           3.6s
    => [internal] load .dockerignore                                        0.0s
    => => transferring context: 2B                                          0.0s
    => [1/2] FROM docker.io/library/node:alpine@sha256:848e91dcc2e9af8fd40  0.0s
    => [internal] load build context                                        0.0s
    => => transferring context: 57B                                         0.0s
    => CACHED [2/2] COPY . /test                                            0.0s 
    => exporting to image                                                   0.1s
    => => exporting layers                                                  0.0s 
    => => writing image sha256:c8d07391aaf793b41941c7363c6e5f9ff20e7b2f3f5  0.0s 
    => => naming to docker.io/library/test                                  0.0s 

    What's Next?
    View a summary of image vulnerabilities and recommendations → docker scout quickview
    PS C:\Users\HP\OneDrive\Desktop\PRACTICAL\WAD\WAD_2B\test> docker images
    REPOSITORY   TAG       IMAGE ID       CREATED         SIZE
    test         latest    c8d07391aaf7   9 minutes ago   148MB
    PS C:\Users\HP\OneDrive\Desktop\PRACTICAL\WAD\WAD_2B\test> docker ps
    CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
    PS C:\Users\HP\OneDrive\Desktop\PRACTICAL\WAD\WAD_2B\test> 