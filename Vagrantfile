# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/trusty64"

  config.vm.network "forwarded_port", guest: 9092, host: 9092

  config.vm.provider "virtualbox" do |vb|
	   vb.memory = 4096
	   vb.cpus = 1
  end

  config.vm.provision "docker" do |d|

    d.build_image "/vagrant",
      args: "-t ti-kafka"
    d.run "ti-kafka",
      auto_assign_name: false,
      args: "-p '2181:2181' -p '9092:9092' --name kafka --env ADVERTISED_HOST=localhost --env ADVERTISED_PORT=9092"

  end


end
