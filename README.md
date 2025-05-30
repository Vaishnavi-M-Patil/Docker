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

### Comparison between Virtualization and Containerization:
#### Virtualization:
- A VM is like a computer inside a computer, running its own OS and apps, but using shared physical resources.
- Requires a hypervisor to manage and allocate resources to the VMs.
- VMs consume more resources than containers, requiring more memory and CPU.
- VMs offer high isolation, making them suitable for security-sensitive applications and legacy systems.
- VMs take longer to boot up compared to containers.
#### Containerization:
- Containers share the host operating system.
- Containers are smaller and lightweight than VMs.
- Containers starts quickly because they don't require a full operating system.
- Containers are portable and can be easily deployed on different environments.
- Containers may not provide the same level of isolation as VMs.
  ![docker](https://github.com/Vaishnavi-M-Patil/Docker/blob/main/assets/docker.jpg)
  ![bare-metal](https://github.com/Vaishnavi-M-Patil/Docker/blob/main/assets/bare%20metal.jpg)
