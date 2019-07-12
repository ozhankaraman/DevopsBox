VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "generic/ubuntu1604"

  config.vm.hostname = "dev.zebrastack.com"

  config.vm.network "forwarded_port", guest: 80, host: 80
  config.vm.network "forwarded_port", guest: 443, host: 443
  config.vm.network "forwarded_port", guest: 8080, host: 8080
  config.vm.network "forwarded_port", guest: 8081, host: 8081

  config.vm.provider "libvirt" do |libvirt|
      libvirt.memory = 6144
      libvirt.cpus = 2
   end

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "Ansible/playbook.yml"
  end
end
