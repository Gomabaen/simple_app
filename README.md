# Simple app for Docker learning purposes.

This is a simple Angular 8 application to be run in Docker container.

## Docker development server image

Steps to run run this application in development mode (assuming you have Docker environment setup): 
- Acquire the image from Docker Hub by executing: ***sudo docker pull cowdale/docker-learning:part1_15***
- You can start and publish the application by executing: ***sudo docker run -it -d -p 8080:4200 --name cowdale cowdale/docker-learning:part1_15 ng serve --host 0.0.0.0***
    - The application is published to port 4200, the example command publishes image's port 4200 to Docker machine's port 8080. Change the port to suite your needs.
    - ***Note that the application takes some time to start up.*** After ~10 seconds open a browser and hit to url http://localhost:8080 
    - If you wish to see Angular's logging then leave -d out from the starting command
- The image has bash installed so for more detailed investigations you can access the running image by executing: ***sudo docker exec -it cowdale bash***
    - This requires that you started the image with --name cowdale parameters.


