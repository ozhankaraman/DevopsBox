# DevopsBox: Vagrant Docker + Gitlab + Jenkins Devops Environment Builder Using Ansible Playbooks

Script is tested over Vagrant libvirt environment over generic/ubuntu1604 box, but it should also work on other Debian based distros

- - - 

### Follow the below steps to generate your DevopsBox Environment over Vagrant
```
vagrant box add generic/ubuntu1604 --provider=libvirt
mkdir DevopsBox
cd DevopsBox
```
### Clone Git Repo
```
git clone https://github.com/zebrastack/DevopsBox.git
mv DevopsBox/* .
```
### Update hostname of new Vagrant Box in Vagrantfile and Ansible/variables.yml files

### Update required cpu/memory settings in your Vagrantfile (Minimum 2 CPU, 6 GB RAM Recommended)
### Execute Vagrant Enviroment
```
vagrant up
vagrant ssh
```

### Notes:
Port 80,443,8080,8081 are forwarded to the DevopsBox and Docker, Jenkins and Gitlab is installed on same Vagrant Environment and their access url's are below
```
GitLab Url:  http://vagrant_devopsbox_hostname/
Jenkins Url: http://vagrant_devopsbox_hostname:8081/ 
```

You could get Jenkins Admin password directly from DevopsBox or you could check your Ansible Build logs its written over there

Enyoj using your Vagrant Devops Box (y)
