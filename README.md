DevopsBox: Vagrant Docker + Gitlab + Jenkins Devops Environment Builder Using Ansible Playbooks

Script is tested over Vagrant libvirt environment over generic/ubuntu1604 box, but it should also work on other Debian based distros

Follow the below steps to generate your DevopsBox Environment over Vagrant
1) vagrant box add generic/ubuntu1604 --provider=libvirt
2) mkdir DevopsBox
3) cd DevopsBox
4) git clone https://github.com/zebrastack/DevopsBox.git
5) mv DevopsBox/* .
6) Update new Vagrant Environments hostname in both Vagrantfile and Ansible/variables.yml files
7) Update required cpu/memory settings in your Vagrantfile (Minimum 2 CPU, 6 GB RAM Recommended)
8) Execute Vagrant Enviroment
vagrant up

GitLab Url:  http://vagrant_box_hostname/
Jenkins Url: http://vagrant_box_hostname:8081/ 
