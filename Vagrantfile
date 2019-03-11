# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.synced_folder ".", "/vagrant", type: "virtualbox"
  config.vm.provision "ansible_local" do |ansible|
    ansible.become = true
    ansible.limit = "all"
    ansible.inventory_path = "/vagrant/inventory"
    ansible.playbook = "/vagrant/playbook.yml"
    ansible.verbose = "v"
  end
end
