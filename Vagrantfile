# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|

	config.vm.define "admin", primary: true do |srvr4|
		srvr4.vm.box = "bento/ubuntu-22.04"
		srvr4.vm.hostname = "admin.oteck.fr" # Nom de l'hôte pour la machine
		srvr4.vm.network "public_network", ip: "192.168.1.50", bridge: "eth1"
		srvr4.vm.provider "virtualbox" do |vb|
			vb.name = "admin.oteck.fr"
			vb.memory = "1024" # RAM en Mo
			vb.cpus = 1 # Nombre de CPU
		end
		srvr4.vm.provision "shell", inline: <<-SHELL
		 sudo apt-get update
    
		# Installer Ansible
		sudo apt-get install -y software-properties-common
		sudo add-apt-repository --yes --update ppa:ansible/ansible
		sudo apt-get install -y ansible
		cat > /etc/netplan/50-netcfg.yaml <<EOF
network:
  version: 2
  renderer: networkd
  ethernets:
    eth0:
      dhcp4: true
    eth1:
      addresses:
        - 192.168.1.50/24
EOF
			sudo netplan apply
		SHELL
	end
	config.vm.define "web1" do |srvr5|
		srvr5.vm.box = "bento/ubuntu-22.04"
		srvr5.vm.hostname = "web1.oteck.fr" # Nom de l'hôte pour la machine
		srvr5.vm.network "public_network", ip: "192.168.1.51", bridge: "eth1"
		srvr5.vm.provider "virtualbox" do |vb|
			vb.name = "web1.oteck.fr"
			vb.memory = "1024" # RAM en Mo
			vb.cpus = 1 # Nombre de CPU
		end
		srvr5.vm.provision "shell", inline: <<-SHELL
		cat > /etc/netplan/50-netcfg.yaml <<EOF
network:
  version: 2
  renderer: networkd
  ethernets:
    eth0:
      dhcp4: true
    eth1:
      addresses:
        - 192.168.1.51/24
EOF
			sudo netplan apply
		SHELL
	end
	#
	config.vm.define "web2" do |srvr61|
		srvr61.vm.box = "bento/ubuntu-22.04"
		srvr61.vm.hostname = "web2.oteck.fr" # Nom de l'hôte pour la machine
		srvr61.vm.network "public_network", ip: "192.168.1.52", bridge: "eth1"
		srvr61.vm.provider "virtualbox" do |vb|
			vb.name = "web2.oteck.fr"
			vb.memory = "1024" # RAM en Mo
			vb.cpus = 1 # Nombre de CPU
		end
		srvr61.vm.provision "shell", inline: <<-SHELL
		cat > /etc/netplan/50-netcfg.yaml <<EOF
network:
  version: 2
  renderer: networkd
  ethernets:
    eth0:
      dhcp4: true
    eth1:
      addresses:
        - 192.168.1.52/24
EOF
			sudo netplan apply
		SHELL
	end
	config.vm.define "front" do |srvr6|
		srvr6.vm.box = "bento/ubuntu-22.04"
		srvr6.vm.hostname = "front.oteck.fr" # Nom de l'hôte pour la machine
		srvr6.vm.network "public_network", ip: "192.168.1.53", bridge: "eth1"
		srvr6.vm.provider "virtualbox" do |vb|
			vb.name = "front.oteck.fr"
			vb.memory = "1024" # RAM en Mo
			vb.cpus = 1 # Nombre de CPU
		end
		srvr6.vm.provision "shell", inline: <<-SHELL
		cat > /etc/netplan/50-netcfg.yaml <<EOF
network:
  version: 2
  renderer: networkd
  ethernets:
    eth0:
      dhcp4: true
    eth1:
      addresses:
        - 192.168.1.53/24
EOF
			sudo netplan apply
		SHELL
	end
	config.vm.define "bdd" do |srvr7|
		srvr7.vm.box = "bento/ubuntu-22.04"
		srvr7.vm.hostname = "bdd.oteck.fr" # Nom de l'hôte pour la machine
		srvr7.vm.network "public_network", ip: "192.168.1.54", bridge: "eth1"
		srvr7.vm.provider "virtualbox" do |vb|
			vb.name = "bdd.oteck.fr"
			vb.memory = "1024" # RAM en Mo
			vb.cpus = 1 # Nombre de CPU
		end
		srvr7.vm.provision "shell", inline: <<-SHELL
		cat > /etc/netplan/50-netcfg.yaml <<EOF
network:
  version: 2
  renderer: networkd
  ethernets:
    eth0:
      dhcp4: true
    eth1:
      addresses:
        - 192.168.1.54/24
EOF
			sudo netplan apply
		SHELL
	end
	config.vm.define "ns1" do |srvr71|
		srvr71.vm.box = "bento/ubuntu-22.04"
		srvr71.vm.hostname = "ns1.oteck.fr" # Nom de l'hôte pour la machine
		srvr71.vm.network "public_network", ip: "192.168.1.80", bridge: "eth1"
		srvr71.vm.provider "virtualbox" do |vb|
			vb.name = "ns1.oteck.fr"
			vb.memory = "1024" # RAM en Mo
			vb.cpus = 1 # Nombre de CPU
		end
		srvr71.vm.provision "shell", inline: <<-SHELL
		cat > /etc/netplan/50-netcfg.yaml <<EOF
network:
  version: 2
  renderer: networkd
  ethernets:
    eth0:
      dhcp4: true
    eth1:
      addresses:
        - 192.168.1.80/24
EOF
			sudo netplan apply
		SHELL
	end
	config.vm.define "ns2" do |srvr8|
		srvr8.vm.box = "bento/ubuntu-22.04"
		srvr8.vm.hostname = "ns2.oteck.fr" # Nom de l'hôte pour la machine
		srvr8.vm.network "public_network", ip: "192.168.1.81", bridge: "eth1"
		srvr8.vm.provider "virtualbox" do |vb|
			vb.name = "ns2.oteck.fr"
			vb.memory = "1024" # RAM en Mo
			vb.cpus = 1 # Nombre de CPU
		end
		srvr8.vm.provision "shell", inline: <<-SHELL
		cat > /etc/netplan/50-netcfg.yaml <<EOF
network:
  version: 2
  renderer: networkd
  ethernets:
    eth0:
      dhcp4: true
    eth1:
      addresses:
        - 192.168.1.81/24
EOF
			sudo netplan apply
		SHELL
	end
	config.vm.define "monitoring" do |srvr9|
		srvr9.vm.box = "bento/ubuntu-22.04"
		srvr9.vm.hostname = "monitoring.oteck.fr" # Nom de l'hôte pour la machine
		srvr9.vm.network "public_network", ip: "192.168.1.55", bridge: "eth1"
		srvr9.vm.provider "virtualbox" do |vb|
			vb.name = "monitoring.oteck.fr"
			vb.memory = "1024" # RAM en Mo
			vb.cpus = 1 # Nombre de CPU
		end
		srvr9.vm.provision "shell", inline: <<-SHELL
		cat > /etc/netplan/50-netcfg.yaml <<EOF
network:
  version: 2
  renderer: networkd
  ethernets:
    eth0:
      dhcp4: true
    eth1:
      addresses:
        - 192.168.1.55/24
EOF
			sudo netplan apply
		SHELL
	end
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://vagrantcloud.com/search.
  #config.vm.box = "bento/ubuntu-22.04"

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
  # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  #config.vm.network "private_network", ip: "192.168.1.30"

  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  #config.vm.network "public_network", ip: "192.168.1.30"

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  config.vm.synced_folder "./vagrant_share", "/vagrant_data"

  # Disable the default share of the current code directory. Doing this
  # provides improved isolation between the vagrant box and your host
  # by making sure your Vagrantfile isn't accessible to the vagrant box.
  # If you use this you may want to enable additional shared subfolders as
  # shown above.
  # config.vm.synced_folder ".", "/vagrant", disabled: true

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # Example for VirtualBox:
  #
  #config.vm.provider "virtualbox" do |vb|
  # Display the VirtualBox GUI when booting the machine
   #  vb.gui = false
  #
  # Customize the amount of memory on the VM:
    # vb.memory = "1024"
  #end
  #
  # View the documentation for the provider you are using for more
  # information on available options.

  # Enable provisioning with a shell script. Additional provisioners such as
  # Ansible, Chef, Docker, Puppet and Salt are also available. Please see the
  # documentation for more information about their specific syntax and use.
  # config.vm.provision "shell", inline: <<-SHELL
  #   apt-get update
  #   apt-get install -y apache2
  # SHELL
end
