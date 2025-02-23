# ToDoApp_UI
ToDoApp_UI (Nodejs)

## Getting Started with Create React App

This project was bootstrapped with Create React App.

1. Install NodeJs 16.x and NPM on Ubuntu
2. Update the backend URL in the src/TodoApp.js
3. Run npm install
4. RUn npm run build
5. Copy the Generated artifacts in nginx server

## Create container image (docker file is already present with codes)

To create a Docker container image from your Node.js code, assuming you already have the Dockerfile in place, follow these steps:

1. Navigate to your project directory: Open a terminal and navigate to the directory containing your Node.js application and the Dockerfile.
```
cd /path/to/your/project
```
2. Build the Docker image: Use the docker build command to build the Docker image. Make sure you're in the same directory as the Dockerfile.
```
$ docker build -t your-image-name .

Replace your-image-name with the name you want for your image. EX: docker build -t todoapp .
The . at the end specifies the current directory as the build context. If your Dockerfile is located elsewhere, replace . with the appropriate path.
```
3. Verify the image: Once the build is complete, you can check if the image was created successfully using the docker images command:
```
docker images

This will list all the Docker images on your local machine, including the one you just built.
```
4. Run the Docker container: After the image is built, you can run it as a container using the docker run command:
```
docker run -p 3000:3000 your-image-name

The -p 3000:3000 flag maps port 3000 on your local machine to port 3000 inside the container. Modify these port numbers if your application uses different ports.
Replace your-image-name with the actual name you assigned to the image. EX: docker run -p 3000:3000 todoapp
Access the Node.js application: If the Node.js application is running on port 3000, you can access it at http://localhost:3000 in your browser or API client.
```
### Summary of commands:
``` 
# Navigate to your project directory
cd /path/to/your/project

# Build the Docker image
docker build -t todoapp .

# Verify the image is created
docker images

# Run the Docker container
docker run -p 3000:3000 todoapp
or
docker run -P --name todoapp-con todoapp
```
