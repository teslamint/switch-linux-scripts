# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
  config.vm.box = "archlinux/archlinux"
  config.vm.provider "virtualbox" do |vb|
    vb.cpus = "4"
    vb.memory = "4096"
  end
  config.vm.provision "shell", inline: <<-SHELL
    pacman -Sy --noconfirm wget git make gcc swig bc patch m4 bison flex pkg-config libusb
    sudo -u vagrant mkdir /home/vagrant/nx-linux
    sudo -u vagrant cp /vagrant/* /home/vagrant/nx-linux/
  SHELL
end
