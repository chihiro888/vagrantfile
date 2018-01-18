# -*- mode: ruby -*-
# vi: set ft=ruby :

MEMORY = 4096
CPU_COUNT = 2

Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-17.10"

  config.vm.network "private_network", ip: "192.168.33.66"

  # config.vm.network "forwarded_port", guest: 80, host: 8080

  config.vm.synced_folder  ".", "/vagrant", disabled: true

  config.vm.provider "virtualbox" do |vb|
      vb.customize ["modifyvm", :id, "--memory", MEMORY.to_s]
      vb.customize ["modifyvm", :id, "--cpus", CPU_COUNT.to_s]
  end
end
