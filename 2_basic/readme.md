## Docker Setup
### Installation
 1. Upgrade packages of linux<br>
     `$ sudo yum upgrade`
  
 2. Install dependent packages<br>
      `$ sudo yum install -y yum-utils device-mapper-persistent-data lvm2`
 3. Setup stable repository<br>
      `sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo`
 
 4. Install docker <br>
     `$ sudo yum install docker-ce`
5. Start docker<br>
      `$ sudo systemctl start docker` 
 6. Run hello-world image to verify<br>
      `$ sudo docker run hello-world`
### Uninstall docker

 1. Uninstall docker package<br>
 `$ sudo yum remove docker-ce`
 2. Delete images, containers, and volumes<br>
 `$ sudo rm -rf /var/lib/docker`

### Possible Issues
1. Requires: container-selinux >= 2.9<br>
    **Solution**: Get  the link to the latest container-selinux package and install it.<br>
     `yum install http://mirror.centos.org/centos/7/extras/x86_64/Packages/container-selinux-2.74-1.el7.noarch.rpm` 
