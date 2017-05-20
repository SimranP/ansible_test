# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.define "box1" do |box1|
    box1.vm.box = "centos6.7_box"

    box1.vm.network "private_network", ip: "192.168.33.10"
    box1.vm.network "forwarded_port", guest: 8153, host: 8153
    box1.vm.network "forwarded_port", guest: 8154, host: 8154

    box1.vm.provider "virtualbox" do |vb|
       vb.memory = "2048"
       vb.cpus = 1
    end
  end

  config.vm.define "box2" do |box2|
    box2.vm.box = "centos6.7_box"

    box2.vm.network "private_network", ip: "192.168.33.11"

    box2.vm.provider "virtualbox" do |vb|
        vb.memory = "2048"
        vb.cpus = 1
    end
  end
end
