# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/xenial64"

  config.vm.synced_folder "./project", "/home/vagrant/project"

  config.vm.provider "virtualbox" do |vb|

    vb.memory = "2048"

    #vb.gui = true
    #vb.customize ["modifyvm", :id, "--vram", "64"]
    #vb.customize ["modifyvm", :id, "--accelerate3d", "on"]
  end

  #config.vm.provision "shell", inline: <<-SHELL
  #  sudo apt-get install -y lightdm lxde vim-gnome
  #SHELL

  config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get update
    sudo apt-get install -y virtualbox-guest-dkms virtualbox-guest-utils virtualbox-guest-x11
    sudo apt-get install -y build-essential git cmake docker
  SHELL

end

