# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "centos/8"
  config.vm.box_version = "1905.1"
  config.vm.hostname = 'k8s-dev'
  config.vm.define vm_name = 'test'
  
  config.vm.network :private_network, ip: "172.17.8.120"
  config.vm.provider :virtualbox do |v|
      v.name = "test"
      v.customize ["modifyvm", :id, "--cpus", 2]
      v.customize ["modifyvm", :id, "--memory", 4096]
      v.customize ['modifyvm', :id, '--nicpromisc1', 'allow-all']
  end
end
