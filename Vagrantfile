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
  # boxes at https://atlas.hashicorp.com/search.
  #config.vm.box = "lubuntu1704"
  config.vm.box = "halvards/lubuntu1604"

  # Disable automatic box update checking. If you disable this, then
  # boxes will only be checked for updates when the user runs
  # `vagrant box outdated`. This is not recommended.
  # config.vm.box_check_update = false

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  # config.vm.network "forwarded_port", guest: 80, host: 8080

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
   config.vm.network "private_network", ip: "192.168.33.10"

  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  # config.vm.network "public_network"

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  # config.vm.synced_folder "../data", "/vagrant_data"

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # Example for VirtualBox:
  #
   config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
     vb.gui = true
 	vb.cpus = 4 
  #   # Customize the amount of memory on the VM:
<<<<<<< HEAD
     	vb.memory = "4028"
	vb.cpus = 2
	vb.customize ["modifyvm", :id, "--vram", "256"]
=======
     vb.memory = "8144"
>>>>>>> 3777356c9237ccdeddc0270eb02e058893d79c2f
   end
  #
  # View the documentation for the provider you are using for more
  # information on available options.

  # Define a Vagrant Push strategy for pushing to Atlas. Other push strategies
  # such as FTP and Heroku are also available. See the documentation at
  # https://docs.vagrantup.com/v2/push/atlas.html for more information.
  # config.push.define "atlas" do |push|
  #   push.app = "YOUR_ATLAS_USERNAME/YOUR_APPLICATION_NAME"
  # end

  # Enable provisioning with a shell script. Additional provisioners such as
  # Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
  # documentation for more information about their specific syntax and use.
   config.vm.provision "shell", inline: <<-SHELL
	apt-get update
<<<<<<< HEAD
	apt-get install -y awscli git wget fish vim
	apt-get install alien dpkg-dev debhelper build-essential
=======
	apt-get install -y awscli git wget fish juju lxd zfsutils-linux
>>>>>>> 3777356c9237ccdeddc0270eb02e058893d79c2f
	wget https://download.sublimetext.com/sublime-text_build-3126_amd64.deb
	sudo dpkg -i sublime-text*.deb
	sudo apt-get install libxss1 libappindicator1 libindicator7 -y
	wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
	# wget https://downloads.citrix.com/12939/icaclient_13.5.0.10185126_amd64.deb?__gda__=1493059163_da57c5d4a30cd783730021da68a3f9ea -O citrix.deb
#	wget https://downloads.citrix.com/12939/icaclientWeb_13.5.0.10185126_amd64.deb?__gda__=1493065331_3812faf1415ad9b412d9a687d9e362fb -O citrix.deb
	# used to remove sudo dpkg -P icaclient
#	sudo ln -s /usr/share/ca-certificates/mozilla/* /opt/Citrix/ICAClient/keystore/cacerts/
#	sudo ctx_rehash /opt/Citrix/ICAClient/keystore/cacerts/
	sudo dpkg -i google-chrome*.deb
	sudo dpkg -i citrix.deb
	sudo apt-get install -f -y

	sudo dpkg -i citrix.deb
	sudo dpkg -i google-chrome*.deb
	wget https://s-media-cache-ak0.pinimg.com/originals/5e/d8/b0/5ed8b052d77850bfefd87950a95133b0.jpg
	# gsettings set org.gnome.desktop.background picture-uri ./5ed8b052d77850bfefd87950a95133b0.jpg
   SHELL
end
