# Nginx Website Template

This repository provides a template for an Nginx-based website. Follow the steps below to download, set up, compile, and push the Docker image.

## Prerequisites

* Docker installed on your system.
* A GitHub account.
* Docker Hub account for pushing images.

## Downloading the Repository

```
curl -L -o nginx-website-template.zip https://github.com/ryderhutchings/nginx-website-template/archive/refs/heads/main.zip

unzip nginx-website-template.zip
```

## Setting Up the Environment

```
cd nginx-website-template-main
```

## Building the Docker Image

```
docker build -t yourusername/nginx-website-template .
```

## Running the Docker Container

```
docker run -d -p 8080:80 yourusername/nginx-website-template

Visit http://localhost:8080 to view your website.
```

Visit `http://localhost:8080` to view your website.

## Pushing the Docker Image

```
docker login

docker push yourusername/nginx-website-template
```
