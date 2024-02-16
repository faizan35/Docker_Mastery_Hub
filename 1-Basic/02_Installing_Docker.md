# 2. Installing Docker

In this section, we will guide you through the process of installing Docker.

## 2.1 Installing Docker

To get started with Docker, follow these steps:

1. Visit the [official Docker website](https://www.docker.com/) and download the appropriate version for your operating system.
2. Install Docker following the provided instructions.
3. Verify the installation using the `docker --version` command.

For **Debian-based Linux distribution**

```bash
sudo apt install docker.io
```

This creates a docker group.
Add your user to this group, to avoid using `sudo` everytime.

```bash
sudo usermod -aG docker <your user name>
```

```bash
docker --version
```

---

## 2.2 Basic Docker commands and CLI usage

#### 1. Images:

- `docker images` or `docker image ls`: List all Docker images on your machine.
- `docker pull image_name:tag`: Download a Docker image from a registry.

#### 2. Containers:

- `docker ps`: List all running containers.
- `docker ps -a`: List all containers (both running and stopped).
- `docker run image_name:tag`: Run a container based on a specific image.
- `docker stop container_id_or_name`: Stop a running container.
- `docker start container_id_or_name`: Start a stopped container.
- `docker restart container_id_or_name`: Restart a container.
- `docker rm container_id_or_name`: Remove a stopped container.

#### 3. Logs:

- `docker logs container_id_or_name`: View the logs of a container.

#### 4. Exec:

- `docker exec -it container_id_or_name /bin/bash`: Open a terminal inside a running container.

#### 5. Networking:

- `docker network ls`: List Docker networks.
- `docker network inspect network_name`: Inspect a specific Docker network.

#### 6. Volumes:

- `docker volume ls`: List Docker volumes.
- `docker volume create volume_name`: Create a Docker volume.

#### 7. Build:

- `docker build -t image_name:tag .` : Build a Docker image from a Dockerfile.

#### 8. Registry:

- `docker login`: Log in to a Docker registry.
- `docker push image_name:tag`: Push an image to a Docker registry.

#### 9. Info:

- `docker info` : Display system-wide information about Docker.

#### 10. Cleanup:

- `docker system prune` : Remove all stopped containers, unused networks, and dangling images.

[← Previous] || [Index](../README.md) || [Next→]
