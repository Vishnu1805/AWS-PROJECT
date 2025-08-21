I have Hosted my React web App in Ec2 Instance 
#Server Creation
I have created a EC2 ubunutu server 
i hvae installed node and npm For running my project
and installed pm2 
teh i have clone the project repo from  the git 
then enter in to the project 
and then using the command npx expo export i have export project 
i have run the project with the comnmand pm2 serve dist 80 --name TaskManager
and the project is succesfully running 

<img width="1352" height="699" alt="Screenshot 2025-08-21 122337" src="https://github.com/user-attachments/assets/8e9a3102-444d-469e-90b8-b93171f21c3d" />

-------------------docker-----------------------------------------
#Server Creation
I have created a EC2 ubunutu server
i hvae installed node and npm For running my project
i have installed docker also
then i have clone the project repo from  the git 
then i have create the docker image by using the command 
docker build -t taskmanager .
then i hav erun the docker image 
docker run -d -p 80:3000 --name taskmanger
docker ps to check the running containers

