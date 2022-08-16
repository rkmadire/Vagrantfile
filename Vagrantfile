# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
config.ssh.insert_key = false
config.vm.provider :virtualbox do |vb|
vb.customize ["modifyvm", :id, "--memory", "512"]
 end

 # control
 config.vm.define "control" do |app|
 app.vm.hostname = "control"
 app.vm.box = "ubuntu/trusty64"
 app.vm.network :private_network, ip: "192.168.60.111"
 end
 
 
 # Load Balancer.
 config.vm.define "lb" do |app|
 app.vm.hostname = "lb"
 app.vm.box = "ubuntu/trusty64"
 app.vm.network :private_network, ip: "192.168.60.112"
 end
 
 # Application server 1.
 config.vm.define "app1" do |app|
 app.vm.hostname = "orc-app1.dev"
 app.vm.box = "ubuntu/trusty64"
 app.vm.network :private_network, ip: "192.168.60.113"
 end

 # Application server 2.
 config.vm.define "app2" do |app|
 app.vm.hostname = "orc-app2.dev"
 app.vm.box = "ubuntu/trusty64"
 app.vm.network :private_network, ip: "192.168.60.114"
 end

 # Database server.
 config.vm.define "db" do |db|
 db.vm.hostname = "orc-db.dev"
 db.vm.box = "ubuntu/trusty64"
 db.vm.network :private_network, ip: "192.168.60.115"
 end
 end
