# Nginx Website Template

This repository provides a template for an Nginx-based website. Follow the steps below to download, set up, compile, and push the Docker image.

## Prerequisites

* Docker installed on your system.
* Git installed on your system.
* A GitHub account.
* Docker Hub account for pushing images.

## Downloading the Repository

```
git clone https://github.com/ryderhutchings/nginx-website-template.git
```

Now, `cd` into the `nginx-website-template` directory, then navigate to the `html/` folder. You can use `nano` or any text editor to edit the `index.html` file. After editing the HTML, compile the Docker image and push it to Docker Hub.

```bash
cd nginx-website-template
cd html/
nano index.html
cd ..
docker build -t your-dockerhub-username/nginx-website-template .
docker push your-dockerhub-username/nginx-website-template
```

## Building the Docker Image

```
docker build -t yourusername/nginx-website-template .
```

## Pushing the Docker Image

```
docker login

docker push yourusername/nginx-website-template
```

## Deploying Service to K3s
To deploy the Nginx website to your K3s cluster, apply the YAML files using:

**MAKE SURE TO ADD** `yourusername/nginx-website-template` **TO** `deployment.yaml`.

```
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

## How to Find the IP Address

```
kubectl get pods -o wide
```

For the port:
```
kubectl get service -n <namespace>
```

** Hi future me!! **

