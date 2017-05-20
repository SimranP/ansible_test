# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://atlas.hashicorp.com/search.
  config.vm.define "box1" do |box1|
    box1.vm.box = "centos6.7_box"    # using a specific IP.
    box1.vm.network "private_network", ip: "192.168.33.10"
    box1.vm.provider "virtualbox" do |vb|
       vb.memory = "2048"
       vb.cpus = 1
    end
  end
  config.vm.define "box2" do |box2|
    box2.vm.box = "centos6.7_box"
    #box2.vm.network "forwarded_port", guest: 8080, host: 8080

    box2.vm.network "private_network", ip: "192.168.33.11"
    box2.vm.provider "virtualbox" do |vb|
        vb.memory = "2048"
        vb.cpus = 1
    end
  end
end
