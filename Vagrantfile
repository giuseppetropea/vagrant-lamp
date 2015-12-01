# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"
VM_NAME = "vagrant-lamp"
VM_IP = "192.168.56.101"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    
  config.vm.define VM_NAME 
  config.vm.box = "ubuntu/trusty64"
  config.vm.hostname = VM_NAME
  config.vm.network "private_network", ip: VM_IP 

	config.vm.provision "shell", path: "provision.sh"
  
  config.vm.boot_timeout = 300

  config.vm.provider "virtualbox" do |vm|
    vm.name = VM_NAME
    vm.memory = 1024
    vm.cpus = 2
  end

end
