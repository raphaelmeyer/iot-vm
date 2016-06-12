# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/xenial64"

  config.vm.synced_folder "./project", "/home/ubuntu/project"

  config.vm.provider "virtualbox" do |vb|

    vb.memory = "2048"
    vp.cpus = 2

    #vb.gui = true
    #vb.customize ["modifyvm", :id, "--vram", "64"]
    #vb.customize ["modifyvm", :id, "--accelerate3d", "on"]
  end

  config.ssh.forward_x11 = true

  #config.vm.provision "shell", inline: <<-SHELL
  #  sudo apt-get install -y lightdm lxde vim-gnome
  #SHELL

  config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get update
    sudo apt-get install -y virtualbox-guest-dkms virtualbox-guest-utils virtualbox-guest-x11
    sudo apt-get install -y build-essential git cmake docker.io
    sudo apt-get install -y mosquitto-clients curl libgtest-dev google-mock
    sudo apt-get install -y qtbase5-dev qt5-default qml-module-qtquick2
    sudo apt-get install -y qml-module-qtquick-controls qml-module-qtquick-dialogs qml-module-qtquick-particles2 qtdeclarative5-dev
    sudo adduser ubuntu docker
  SHELL

end

