# Docker
## What is Docker?
Docker is an open source platform that enables developers to package applications along with all their dependencies into containers.

#### Containers:
- A Docker Container is a running instance of an image.
- A container is a lightweight, standalone, and executable package that contains everything needed to run an application.
- Containers are created form images.
- Containers are isolated from each other and the host system.
#### Images:
- A Docker Image is a read-only template that contains the application code, libraries, and dependencies.
- Images are usually built from a **Dockerfile**.
#### Dockerfile:
A text file with instructions for building a Docker image. 
#### Docker Engine:
The core of docker, which creates and runs containers on the host operating system.
#### Docker Hub:
A repository where developers can pull images from and push custom images to share them.

---

## Virtualization VS Containerization:
- `Virtualization` uses a hypervisor to create virtual machines (VMs), each with its own operating system, offering high isolation and compatibility with legacy applications but requiring more resources. 

- `Containerization` uses lightweight containers that share the host operating system kernel, resulting in faster start-up times, better resource utilization, and ease of deployment. 

### What is hypervisor and types of hypervisor:
- A hypervisor is software that allows you to create and manage virtual machines (VMs) by abstracting and dividing the physical hardware.  
- It enables multiple operating systems to run simultaneously on a single physical machine by virtualizing CPU, memory, storage, and networking.
#### There are two main types:
1. Type 1 Hypervisor (Bare-metal):
  **Definition:** `Runs directly on physical hardware (no host OS)`. It manages guest operating systems natively.
   **Examples:**
      - VMware ESXi
      - Microsoft Hyper-V (on Windows Server)
      - KVM (Kernel-based Virtual Machine)
      - Xen
        
2. Type 2 Hypervisor (Hosted):
  **Definition:** `Runs on top of a host operating system (like an app)` and uses it to manage hardware resources.
   **Examples:**
      - Oracle VirtualBox
      - VMware Workstation
      - VMware Fusion (macOS)
      - Parallels Desktop (macOS)


### Comparison between Virtualization and Containerization:
#### Virtualization:
- A VM is like a computer inside a computer, running its own OS and apps, but using shared physical resources.
- Requires a hypervisor to manage and allocate resources to the VMs.
- VMs consume more resources than containers, requiring more memory and CPU.
- VMs offer high isolation, making them suitable for security-sensitive applications and legacy systems.
- VMs take longer to boot up compared to containers.
- It is Hardware-level virtualization.
  
#### Containerization:
- Containers share the host operating system.
- Containers are smaller and lightweight than VMs.
- Containers starts quickly because they don't require a full operating system.
- Containers are portable and can be easily deployed on different environments.
- Containers may not provide the same level of isolation as VMs.
- It is OS-level virtualization.

  ![docker](https://github.com/Vaishnavi-M-Patil/Docker/blob/main/assets/docker.jpg)
  ![bare-metal](https://github.com/Vaishnavi-M-Patil/Docker/blob/main/assets/bare%20metal.jpg)

| Can a .sh (shell script) file be executed in Ubuntu without giving it execute permissions, and how? |
| ---------------------------------------------------------------------------------------------------- |
| When you run `bash script.sh`, you are passing the file as an argument to the bash program, which reads and runs it — the file itself does not need to be executable.
It will not work if you try to run it directly like: `./script.sh`
unless you give it execute permission with: `chmod +x script.sh` |

--- 

## Docker Commands:
| command            | Description |
|------------------- | ----------- |
| docker pull nginx:latest | Downloads the latest nginx image from Docker Hub. |
| docker images | Lists all Docker images available locally. |
| docker run -d --name nginx_container -p 80:80 spider nginx:latest | Runs an nginx container in detached mode, maps host port 80 to container port 80, and names it nginx_container. |
| docker ps | Lists running containers. |
| docker ps -a | Lists all containers, including stopped ones. |
| docker kill containerID/name | Forcefully stops a running container immediately. |
| docker inspect containerID/name | Displays detailed information about a container. |
| docker exec -it containerID/name bash | Opens an interactive Bash shell inside a running container. |
| docker rm -f containerID/name | Removes a container (even if it's running, due to -f). |
| docker ps -a -q | Lists only the container IDs of all containers. |
| docker stop containerID/name | stops a running container. |
| docker start containerID/name | Starts a stopped container. |
| docker container prune | Removes all stopped containers. |
| docker image prune | Removes unused images. |
| docker commit containerID/name | Creates a new image from a container’s current state. |
| docker tag containerID/name imgName:tag | Tags an image with a new name and tag. |
| docker login | Logs into Docker Hub  |
| docker push imgName:tag | Pushes a tagged image to Docker Hub |


```
docker run -d --name httpd_container -p 80:80 httpd
```
| Part |	Description |
| ------ | ---------- |
| docker run	| Runs a new container |
| -d	| Detached mode – runs the container in the background |
| --name httpd_container |	Names the container httpd_container |
| -p 80:80 |	Maps port 80 of the host to port 80 of the container (HTTP traffic) |
| httpd |	docker image httpd from dockerhub |
#### What It Does:
- Starts httpd inside a Docker container.
- Makes the server accessible on your local machine via http://localhost.





