# Microservice_containerization

Собирал и запускал с использованием следующих команд:

docker build -t first_image_py_app

docker run -it --rm -p 8080:8080 --name my-running-app first_image_py_app 
