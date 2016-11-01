# Vagrant: Wombo Combo

## Docker, Elixir and NodeJS

## Getting started

1. Install [Ruby](https://www.ruby-lang.org/en/documentation/installation/)
1. Install [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
1. Install [Vagrant](https://www.vagrantup.com/downloads.html)
1. Install docker compose plugin `vagrant plugin install vagrant-docker-compose`
1. Copy `vagrant_provision.sh` and `Vagrantfile` one level above the project folder. (You can make it part of the project as well, to share the setup between dev teams)
1. Open terminal wher the `Vagrantfile` is and run `vagrant up` to setup your new vm.
1. When finished installing: run `vagrant ssh` to login to your machine
1. Navigate to `cd /vagrant` this will give you access to your project folders and files.
1. Then this virtual world is your oyster

Update the vagrant forwarding ports.

Update the private ip.

## What in box

1. docker
1. docker-compose
1. Elixir
1. Node
