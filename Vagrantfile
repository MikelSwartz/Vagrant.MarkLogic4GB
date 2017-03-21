# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "bmcgonigle/centos68"
  config.vm.provider "virtualbox" do |v|
    v.memory = 4096
  end
  config.vm.network "forwarded_port", guest: 7999, host: 7999
  config.vm.network "forwarded_port", guest: 8000, host: 8000
  config.vm.network "forwarded_port", guest: 8001, host: 8001
  config.vm.network "forwarded_port", guest: 8003, host: 8003
  
  config.vm.provision "shell",
    path: "marklogic.provision.sh"
end
