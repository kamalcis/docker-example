# DockerExample


# Docker Image Handling
===============================================================
In this current folder I already saved a docker image "demo-docker.tar" using the 
docker CMD > docker save demo-docker.tar demo-docker-app:latest



# To run the saved docker image
1. Dowonload the source code from git and point to folder demo-docker in the command prompt
2. Run the CMD => docker load --input demo-docker.tar
3. The image will be available in local docker client. If we run the command => docker images 
   then the repository should list demo-docker-app
4. CMD> docker run --rm -d -p 81:80/tcp demo-docker-app:latest 
5. Browse http://localhost:81/  The application home page should be displayed. 


# Step -1: Create New Docker image from the code build
To create a new docker image from this code and DockerFile please follow the instructions
1. Open the folder DOCKER-EXAMPLE 
2. Make sure you have node version v18.18.0 
3. Build the solution using CMD> ng build
3. Run the Docker Desktop from start menu
4. Build Docker Image using the CMD> docker build --pull --rm -f "Dockerfile" -t angular-docker-example "." 
5. TO verify the docker image created run command CMD> docker images 
6. In the repository list the image "angular-docker-example" should be listed. 


# Step-2: To run the docker image created in step-1
1. Make sure you are in the root directory in terminal
2. Run the docker command CMD> docker run --rm -d -p 80:80/tcp angular-docker-example:latest
3. Visit the site http://localhost:80 in browser
4. Application Home page e.g. angular default should be displayed. 







================================================================

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 13.3.5.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.
