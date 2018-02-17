# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box_check_update = false
  config.vm.define "master" do |master|
    master.vm.box = "ubuntu/trusty64"
    master.vm.hostname = "master"
    master.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
      vb.gui = false
    end
    master.vm.network :private_network, ip: "192.168.42.99"
    master.vm.provision "ansible_local" do |ansible|
      ansible.playbook = "main.yml"
      ansible.install = true
      ansible.limit = "all"
      ansible.inventory_path = "hosts"
    end
  end
end
