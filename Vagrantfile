# vi: set ft=ruby :
# vm to dev freeipa

Vagrant.configure("2") do |config|
  config.vm.box = "fedora/30-cloud-base"
  config.vm.box_version = "30.20190425.0"

  # config.vm.network "forwarded_port", guest: 80, host: 8080
  # config.vm.network "private_network", ip: "192.168.33.10"
  # config.vm.network "public_network"
  # config.vm.synced_folder "../data", "/vagrant_data"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "2048"
  end

  config.vm.provision "shell", run: "once", inline: <<-SHELL
    yum update -y
    yum group install "Development Tools" -y 
    yum install docker -y
  SHELL
end
