# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "bento/centos-7.3"
  
  config.ssh.insert_key = 'true'
  config.ssh.username = 'root'
  config.ssh.password = 'vagrant'

  config.vm.define "foohost" do |foohost|
  end

  config.vm.provider "vmware_workstation" do |vmware_workstation|
     vmware_workstation.gui = true
     vmware_workstation.whitelist_verified = true
  end
   
  config.vm.provision "ansible_local" do |ansible|
     ansible.verbose = "v"
     ansible.playbook = "playbook.yml"
  end

end
