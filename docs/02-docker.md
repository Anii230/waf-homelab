# Docker

## Objective

Install Docker Engine on the Ubuntu Server to provide an isolated, reproducible environment for deploying the vulnerable web application and supporting security services.

---

## Why Docker?

Docker was chosen because it allows applications to run in isolated containers without affecting the host operating system. Containers are lightweight, reproducible, and can be easily recreated if they become corrupted or misconfigured.

Advantages include:

- Application isolation
- Reproducible environments
- Easy deployment and removal
- Simplified dependency management
- Support for multi-container applications

---

## Installation

Docker CE was installed from Docker's official repository instead of Ubuntu's default repository.

This approach ensures:

- Officially supported packages
- Faster access to new releases
- Consistency with Docker's documentation

---

## Components Installed

- Docker Engine
- Docker CLI
- containerd
- Docker Compose
- Buildx

---

## Key Concepts

### Image

A read-only template containing everything required to run an application.

One image can be used to create multiple containers.

### Container

A running instance of an image.

Containers are isolated from each other while sharing the host's Linux kernel.

### Docker Hub

Docker's public registry from which container images are downloaded.

---

## Verification

Docker was verified using:

```bash
docker --version
docker compose version
docker info
docker run hello-world
```

The `hello-world` container successfully downloaded its image from Docker Hub, executed its main process, printed a confirmation message, and exited normally.

---

## Lessons Learned

- Docker images act as templates.
- Containers are running instances of images.
- Docker automatically downloads images if they are not available locally.
- Containers stop when their main process exits.
- Docker caches downloaded images locally for future use.
