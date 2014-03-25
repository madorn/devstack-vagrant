# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "precise64"
  config.vm.hostname = "devstack-vagrant"
  config.vm.network "private_network", ip: "192.168.10.175"

  config.vm.provider "virtualbox" do |vbx|
    vbx.customize ["modifyvm", :id, "--memory", "4096"]
    vbx.customize ["modifyvm", :id, "--cpuexecutioncap", "90"]
    vbx.customize ["modifyvm", :id, "--rtcuseutc", "on"]
    vbx.customize ["modifyvm", :id, "--nic2", "hostonly"]
  end
end
