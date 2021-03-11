Install docker on ubuntu

1. sudo apt update
2. sudo apt install apt-transport-https ca-certificates curl software-properties-common
3. curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
4. sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
5. sudo apt update
6. apt-cache policy docker-ce
7. "docker-ce:
      Installed: (none)
      Candidate: 18.03.1~ce~3-0~ubuntu
      Version table:
      18.03.1~ce~3-0~ubuntu 500
      500 https://download.docker.com/linux/ubuntu bionic/stable amd64 Packages"
8. sudo apt install docker-ce
9. sudo systemctl status docker
     source: digital ocean website

Run Jenkins on docker

1. Pull Jenkins image from dockerhub

`docker pull jenkins`

2. Check for Jenkins docker image ID and run docker

`docker run -d -p 80:80 cd14cecfdb3a`               'cd14cecfdb3a' is docker image ID

3. Open Jenkins console on browser

  localhost:8080

4. fetch admin password from logs  path (/var/jenkins_home/secrets/initialAdminPassword)
   `docker logs bb6425734fc4`                     'bb6425734fc4' is containerID

5. Set username and password

6. Created Jenkins Jobs to echo "hello world"

9. Set cron using build periodically
    `H * * * * `

10. Add build step to print hello work using execute shell.


Please find screenshots from `screenshots` folder.     
