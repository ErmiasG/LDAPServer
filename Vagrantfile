# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu-16.04-amd64"
  config.vm.box = "ubuntu/xenial64"
  config.vm.hostname = "ldap.example.com"

  config.vm.network :forwarded_port, host: 8000, guest: 80
  config.vm.network :forwarded_port, host: 1389, guest: 389

  config.vm.provider "virtualbox" do |vb|
    vb.linked_clone = true
    vb.memory = "2048"
  end

  config.vm.provision "shell", path: "provision.sh"
end
