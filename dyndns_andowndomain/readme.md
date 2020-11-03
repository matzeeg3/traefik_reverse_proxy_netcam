#Prerequisites
1. Linux VM or Raspberry PI
2. Docker installed on the System: https://docs.docker.com/engine/install/debian/
3. Docker Compose installed on System:
   1. Docker Compose Debian: https://docs.docker.com/compose/install/
   2. Docker Compose Raspberry: https://dev.to/rohansawant/installing-docker-and-docker-compose-on-the-raspberry-pi-in-5-simple-steps-3mgl
4. Install the following `sudo apt-get install apache2-utils`
5. Generate a Password for your Dashboard
   * echo $(htpasswd -nbB <USER> "<PASS>") | sed -e s/\$/\$\$/g
6. Edit the docker-compse.yml file:
   * replace `**yourdomain**` with your domain
   * replace `**youremail@here.com**`
   * replace `**admin:pwhash**` with the output from point 5.
7. Edit the dyn-conf.yml:
   * replace `**yourdomain**` with your domain
   * replace `**netcamip**` with your netcam ip
8. Forward Port 80 to the IP of your VM or Raspberry
9. Forware Port 443 to the IP of your VM or Raspberry
10. Create a CNAME on your domain: traefik.yourdomain.zz -> yourdyndnsdomain
11. Create a CNAME on your domain: netcam.yourdomain.zz -> yourdyndnsdomain
12. copy the files to the VM or Raspberry
13. run the following command inside of the directory you upload the files
   * sudo docker-compose up -d
  s 
Now you can enjoy your reverse Proxy with LetsEncrypt certificate