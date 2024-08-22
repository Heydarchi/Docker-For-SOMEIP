# Docker-For-SOMEIP
This docker file can be use to build SOMEIP source code or SOMEIP based projects 

# Ubuntu 22.04 Docker Image for SOME/IP Development

This Dockerfile sets up a development environment based on Ubuntu 22.04 with the necessary tools to build and work with SOME/IP. The image includes `g++-11`, `gcc-11`, `cmake`, `Boost`, and other useful documentation tools.

## Tools Installed
- **g++**: Version 11
- **gcc**: Version 11
- **cmake**: Version 3.22.1
- **Boost Libraries**: Version 1.74
- **asciidoc**
- **source-highlight**
- **doxygen**
- **graphviz**

## How to Build the Docker Image

To build the Docker image, run the following command:

```bash
docker build --no-cache --file Dockerfile_SomeIP --tag "docker_for_someip" .
```

## Troubleshooting Network Issues
If you encounter network issues during the build process (e.g., due to proxy settings), you can build the image with the host network configuration:
```
docker run -it -v /home:/home -v /mnt:/mnt docker_for_someip
```

Troubleshooting Network Issues When Running
If you experience network issues during runtime (e.g., unable to access the internet from within the container), you can run the container with the host network configuration:
```
docker run -it --network=host -v /home:/home -v /mnt:/mnt docker_for_someip
```

## License
This project is licensed under the MIT License - see the LICENSE file for details.


### **DockerHub:**
- **Docker Hub Instructions**: Added instructions on how to pull the pre-built Docker image from Docker Hub.
- **Link to Docker Hub**: [https://hub.docker.com/r/mhheydarchi/docker_for_someip]
