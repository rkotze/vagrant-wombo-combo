# Vagrant: Wombo Combo

If you like your windows dev setup and need to work in both windows and linux environments. This could be the setup for you. ;)

## Getting started

1. Install [Ruby](https://www.ruby-lang.org/en/documentation/installation/)
1. Install [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
1. Install [Vagrant](https://www.vagrantup.com/downloads.html)
1. Install docker compose plugin `vagrant plugin install vagrant-docker-compose`
1. Copy `vagrant_provision.sh` and `Vagrantfile` one level above the project folder. (You can make it part of the project as well, to share the setup between dev teams)
1. Open terminal where the `Vagrantfile` is and run `vagrant up` to setup your new vm.
1. When finished installing: run `vagrant ssh` to login to your machine
1. Navigate to `cd /vagrant` this will give you access to your project folders and files.
1. This virtual world is now your oyster

**Feel free to customise the `VagrantFile` and `vagrant_provision.sh` to fit your project.**

## What's in the box

1. ubuntu/xenial64
1. Docker
1. Docker-compose
1. Elixir
1. Node

## Useful commands

`vagrant up` - start the machine and provision if first boot up

`vagrant ssh` - access the machine

`vagrant reload` - restart the machine

`vagrant reload --provision` - force install on new provisions added to `VagrantFile`

`vagrant suspend` - saves the exact point-in-time state of the machine for quicker resume.
