# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://vagrantcloud.com/search.
  config.vm.box = "minimal/xenial64"

  # Disable automatic box update checking. If you disable this, then
  # boxes will only be checked for updates when the user runs
  # `vagrant box outdated`. This is not recommended.
  # config.vm.box_check_update = false

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  # NOTE: This will enable public access to the opened port
  # config.vm.network "forwarded_port", guest: 80, host: 8080

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine and only allow access
  # via 127.0.0.1 to disable public access
  config.vm.network "forwarded_port", guest: 8181, host: 8181, host_ip: "127.0.0.1"

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  # config.vm.network "private_network", ip: "192.168.33.10"

  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  # config.vm.network "public_network"

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  config.vm.synced_folder "./data", "/vagrant_data"

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # Example for VirtualBox:
  #
  # config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
  #   vb.gui = true
  #
  # Customize the amount of memory on the VM:
  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "2048", "--cpus", "2"]
  end
  #vb.memory = "1024"
  #config.cpus = 6
  # end
  #
  # View the documentation for the provider you are using for more
  # information on available options.

  # Enable provisioning with a shell script. Additional provisioners such as
  # Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
  # documentation for more information about their specific syntax and use.
  config.vm.provision "shell", inline: <<-SHELL
     echo "========>>> PROVISIONING BASE SYSTEM <<<========"
     sudo ex +"%s@DPkg@//DPkg" -cwq /etc/apt/apt.conf.d/70debconf
     sudo dpkg-reconfigure debconf -f noninteractive -p critical
     sudo apt-get update
     sudo apt-get install -y clang git build-essential tcl clang-tidy
     echo "========>>> INSTALLING DEFAULT HACKATHON PROJECT DEPENDENCIES <<<========"
     sudo apt-get -y install autoconf
     sudo apt-get -y install automake
     sudo apt-get -y install autopoint
     sudo apt-get -y install autotools-dev
     sudo apt-get -y install curl
     sudo apt-get -y install cmake
     sudo apt-get -y install freeglut3-dev
     sudo apt-get -y install g++
     sudo apt-get -y install libc-ares-dev
     sudo apt-get -y install libcairo2-dev
     sudo apt-get -y install libcppunit-dev
     sudo apt-get -y install libepoxy-dev
     sudo apt-get -y install libev-dev
     sudo apt-get -y install libevdev-dev
     sudo apt-get -y install libevent-dev
     sudo apt-get -y install libexpat1-dev
     sudo apt-get -y install libffi-dev
     sudo apt-get -y install libgbm-dev
     sudo apt-get -y install libgles2-mesa-dev
     sudo apt-get -y install libgmp-dev 
     sudo apt-get -y install libgnutls-dev
     sudo apt-get -y install libinput-dev
     sudo apt-get -y install liblz4-dev 
     sudo apt-get -y install liblzo2-dev
     sudo apt-get -y install libmtdev-dev
     sudo apt-get -y install libpam0g-dev
     sudo apt-get -y install libpciaccess-dev
     sudo apt-get -y install libpcre3-dev
     sudo apt-get -y install libseccomp-dev
     sudo apt-get -y install libsqlite3-dev
     sudo apt-get -y install libssh2-1-dev
     sudo apt-get -y install libssl-dev
     sudo apt-get -y install libstartup-notification0-dev
     sudo apt-get -y install libtool
     sudo apt-get -y install libudev-dev
     sudo apt-get -y install libwacom-dev
     sudo apt-get -y install libxcb-composite0-dev
     sudo apt-get -y install libxcursor-dev
     sudo apt-get -y install libxfont-dev
     sudo apt-get -y install libxkbfile-dev
     sudo apt-get -y install libxml2-dev
     sudo apt-get -y install lzop
     sudo apt-get -y install make
     sudo apt-get -y install nasm
     sudo apt-get -y install ncurses*
     sudo apt-get -y install nettle-dev 
     sudo apt-get -y install opencl-headers
     sudo apt-get -y install pkg-config
     sudo apt-get -y install unzip
     sudo apt-get -y install wayland-protocols
     sudo apt-get -y install x11proto*
     sudo apt-get -y install xfonts-utils
     sudo apt-get -y install xutils-dev
     sudo apt-get -y install zlib1g-dev 
     sudo apt-get -y install uuid-dev
     sudo apt-get -y install default-jre
     sudo apt-get -y install gawk
     sudo apt-get -y install gperf
     sudo apt-get -y install libao-dev
     sudo apt-get -y install libasound2-dev
     sudo apt-get -y install libass-dev
     sudo apt-get -y install libavahi-client-dev
     sudo apt-get -y install libavahi-common-dev
     sudo apt-get -y install libbluetooth-dev
     sudo apt-get -y install libbluray-dev
     sudo apt-get -y install libbz2-dev
     sudo apt-get -y install libcap-dev
     sudo apt-get -y install libcdio-dev
     sudo apt-get -y install libcec-dev
     sudo apt-get -y install libcurl-dev
     sudo apt-get -y install libcwiid-dev
     sudo apt-get -y install libdbus-1-dev
     sudo apt-get -y install libegl1-mesa-dev
     sudo apt-get -y install libfontconfig-dev
     sudo apt-get -y install libfreetype6-dev
     sudo apt-get -y install libfribidi-dev
     sudo apt-get -y install libgif-dev
     sudo apt-get -y install libgl-dev
     sudo apt-get -y install libglu-dev
     sudo apt-get -y install libiso9660-dev
     sudo apt-get -y install libjpeg-dev
     sudo apt-get -y install libltdl-dev
     sudo apt-get -y install libmicrohttpd-dev
     sudo apt-get -y install libmpcdec-dev
     sudo apt-get -y install libmysqlclient-dev
     sudo apt-get -y install libnfs-dev
     sudo apt-get -y install libplist-dev
     sudo apt-get -y install libpng-dev
     sudo apt-get -y install libpulse-dev
     sudo apt-get -y install libshairplay-dev
     sudo apt-get -y install libsmbclient-dev
     sudo apt-get -y install libssh-dev
     sudo apt-get -y install libswscale-dev
     sudo apt-get -y install libtag1-dev
     sudo apt-get -y install libtinyxml-dev
     sudo apt-get -y install libusb-dev
     sudo apt-get -y install libva-dev
     sudo apt-get -y install libvdpau-dev
     sudo apt-get -y install libxmu-dev
     sudo apt-get -y install libxrandr-dev
     sudo apt-get -y install libxslt1-dev
     sudo apt-get -y install libxt-dev
     sudo apt-get -y install lsb-release
     sudo apt-get -y install rapidjson-dev
     sudo apt-get -y install python-dev
     sudo apt-get -y install python-imaging
     sudo apt-get -y install python-support
     sudo apt-get -y install swig
     sudo apt-get -y install yasm
  SHELL
end
