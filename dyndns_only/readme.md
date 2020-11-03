#Prerequisites
1. Linux VM or Raspberry PI
2. Docker installed on the System: https://docs.docker.com/engine/install/debian/
3. Docker Compose installed on System:
   1. Docker Compose Debian: https://docs.docker.com/compose/install/
   2. Docker Compose Raspberry: https://dev.to/rohansawant/installing-docker-and-docker-compose-on-the-raspberry-pi-in-5-simple-steps-3mgl
4. Edit the docker-compse.yml file:
   * replace `**youremail@here.com**`
5. Edit the dyn-conf.yml:
   * replace `**yourdyndnshere**` with your domain
   * replace `**netcamip**` with your netcam ip
6. Forward Port 80 to the IP of your VM or Raspberry
7. Forware Port 443 to the IP of your VM or Raspberry
8. copy the files to the VM or Raspberry
9. run the following command inside of the directory you upload the files
   * sudo docker-compose up -d  
  
Now you can enjoy your reverse Proxy with LetsEncrypt certificate