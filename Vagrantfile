# -*- mode: ruby -*-
# vi: set ft=ruby :
VAGRANTFILE_API_VERSION = "2"

VM_NAME = "wombo_combo"
MEMORY_SIZE_MB = 1024
NUMBER_OF_CPUS = 2

unless Vagrant.has_plugin?("vagrant-docker-compose")
  system("vagrant plugin install vagrant-docker-compose")
  puts "Dependencies installed, please try the command again."
  exit
end

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.provision "docker"
  config.vm.provision "docker_compose"

  config.vm.define "wombo_combo_box" do |elixir_box|
    elixir_box.vm.provider "virtualbox" do |v|
      v.name = VM_NAME
      v.customize ["modifyvm", :id, "--memory", MEMORY_SIZE_MB]
      v.customize ["modifyvm", :id, "--cpus", NUMBER_OF_CPUS]
    end
    elixir_box.vm.network :private_network, ip: "192.168.55.55"
    elixir_box.vm.network :forwarded_port, guest: 80, host: 8080
    elixir_box.vm.provision :shell, :path => "vagrant_provision.sh"
  end
end
