# vagrant box for iot workshop

## setup vagrant box

    vagrant up
    vagrant provision
    vagrant reload

## setup host

    git clone git@github.com:raphaelmeyer/street-light-simulator.git
    cd street-light-simulator
    git checkout develop/gathering
    git submodule update --init --recursive

    cd ..

    git clone git@github.com:raphaelmeyer/streetlightd.git
    cd streetlightd
    git checkout gathering
    git submodule update --init --recursive

## build daemon in vagrant box

    vagrant ssh

    ubuntu$ cd project/streetlightd
    ubuntu$

## build simulator vagrant box

    vagrant ssh

    ubuntu$ cd project/street-light-simulator
    ubuntu$ mkdir build
    ubuntu$ cd build
    ubuntu$ qmake ..
    ubuntu$ make

## execute single command

    vagrant ssh -c "echo hello"


