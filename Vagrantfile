# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "precise64"

  config.vm.box_url = "http://files.vagrantup.com/precise64.box"

  config.vm.network :private_network, ip: "192.168.100.100"

  config.berkshelf.enabled = true

  config.vm.provision :chef_solo do |chef|
  	chef.add_recipe "ajenti"
  	chef.add_recipe "apache2"

    chef.json = {}
  end
end
