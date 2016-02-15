# -*- mode: ruby -*-
# vi: set ft=ruby :
#
Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.hostname = "piwik"
  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.provider "virtualbox" do |vb|
    vb.memory = 2048
    vb.cpus= 2
  end
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yaml"
  end
end
