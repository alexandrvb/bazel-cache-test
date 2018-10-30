# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "cache" do |cache|
    cache.vm.box = "bento/ubuntu-18.04"
    cache.vm.network "private_network", ip: "192.168.33.10"
  end
  config.vm.define "node1" do |node|
    node.vm.box = "bento/ubuntu-18.04"
    node.vm.network "private_network", ip: "192.168.33.11"
  end
  config.vm.define "node2" do |node|
    node.vm.box = "bento/ubuntu-18.04"
    node.vm.network "private_network", ip: "192.168.33.12"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end
end
