![image](https://github.com/user-attachments/assets/d584ba5d-d63f-47be-ae1b-301fbc52b2ef)# DOCKER-Creating-A-Python-Flask-Web-Application-With-A-Redis-Database
This is a Capstone mini project n3 from my self paced docker learning 

The goal of the website is to calculate the number of visitors of the website and store it in the Redis database

This is the overall plan : First thing to do is to write the Python code in wich we will use Flask framework , then we will create a Dockerfile from that code , then a Docker Compose file in wich we will use the Flask image we just created and Redis image from the DockerHub.

![Capture d'écran 2024-08-30 165446](https://github.com/user-attachments/assets/3daef798-c39d-4f55-b5ba-a0c32537b5e7)


First , I created the Python code in .py file 

![image](https://github.com/user-attachments/assets/cd421fa5-08c7-49ef-98f1-b7d3ffdc912f)

Then i created a requirements.txt , this is the apps that needs to be installed 

![image](https://github.com/user-attachments/assets/409fae77-8daf-4090-a93f-9330d131d48a)

Then Creating the Dockerfile for the app image : 

![image](https://github.com/user-attachments/assets/8dde38c1-1e0f-44f5-a9be-3b8a8863f942)

Then creating the Docker Compose file : 

build : .  , since the dockerfile is in the same rep and the docker compose file

volumes : .:/app , so it copies all files and changements done locally to the container and so to the website

FLASK_DEBUG: "true" , so every changement is done automatically and we dont need to stop the container and rebuild the image ! 

and the redis is to create a container running the redis db 

![image](https://github.com/user-attachments/assets/975db93c-70c8-4331-84e6-27da088bb202)

*Webpage is exposed on port 5000 and docker compose is exposed on port 9000*


Then applying the docker compose file : 

![Capture d'écran 2024-08-30 171408](https://github.com/user-attachments/assets/e8e0a2e1-b1a1-4af9-82fe-28889595889e)

![Capture d'écran 2024-08-30 171419](https://github.com/user-attachments/assets/bfc20370-cc33-4f2c-9893-d647595f3cd8)

Website is working using EC2 public Ip and port 9000 

![image](https://github.com/user-attachments/assets/bd041aae-2299-4bc5-8e8c-40e537a99271)

after refreshing many times : 

![image](https://github.com/user-attachments/assets/f3c8c161-69ed-4c3e-b044-445be5da504e)


Testing some changes in the app.py Code and seeing if it workds automatically ! 

![image](https://github.com/user-attachments/assets/5565c450-4014-4c10-8888-a4299c74c3c6)


![image](https://github.com/user-attachments/assets/8120181d-5c91-4107-99ca-49386e554bd5)


*SUCCES*

![image](https://github.com/user-attachments/assets/5ee7c50f-5c72-4802-8af5-70a8a1804d0f)


