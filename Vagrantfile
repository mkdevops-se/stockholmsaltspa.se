# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANT_NAME="vagrant.mjlife.se"

Vagrant.configure("2") do |config|
  config.ssh.insert_key = false
  config.ssh.forward_agent = true

  config.vm.box = "centos/7"
  config.vm.box_check_update = false
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.network "private_network", ip: "10.187.57.250"

  config.vm.define VAGRANT_NAME
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "512"
    vb.name = VAGRANT_NAME
  end

  # https://www.vagrantup.com/docs/provisioning/ansible.html
  config.vm.provision "ansible", type: "ansible" do |ansible|
    ansible.playbook = "provision.yml"
    ansible.inventory_path = "inventory.ini"
    ansible.limit = VAGRANT_NAME
  end

end
