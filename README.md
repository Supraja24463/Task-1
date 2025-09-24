# Static Application Deployment with Jenkins and Docker

This project demonstrates deploying a simple static application using Jenkins CI/CD pipeline and Docker.

## Steps
1. `index.html` contains the static page (Hello Supraja).
2. `Dockerfile` builds an Nginx container to serve the static page.
3. `Jenkinsfile` defines a pipeline to build and deploy the app.

## Run Locally
```bash
docker build -t hello-supraja .
docker run -d -p 8080:80 hello-supraja
```
Visit: [http://localhost:8080](http://localhost:8080)

## CI/CD with Jenkins
- Configure Jenkins with Docker installed.
- Create a pipeline job and point it to this repository.
- Trigger the pipeline → Your app will be built and deployed automatically.
