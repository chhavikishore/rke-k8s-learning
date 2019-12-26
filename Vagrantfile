# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "geerlingguy/centos7"

  config.vm.define :m1 do |node|
    node.vm.network :private_network, ip: '192.168.110.2'
  end

  config.vm.define :m2 do |node|
    node.vm.network :private_network, ip: '192.168.110.3'
  end

  config.vm.define :m3 do |node|
    node.vm.network :private_network, ip: '192.168.110.4'
  end
end
