Vagrant.configure("2") do |config| 
  config.vm.box = "spox/ubuntu-arm" 
  config.vm.box_version = "1.0.0"
  config.vm.network "private_network", ip: "192.168.56.11"
  config.vm.network "public_network"
  # add synced folder macbook
  config.vm.synced_folder "/Users/suryanshu/Desktop/myshellscripts", "/opt/scripts"
  # provision shell script ubuntu
  config.vm.provision "shell", inline: <<-SHELL
  apt-get update
  apt-get install -y apache2
  SHELL
  config.vm.provider "vmware_desktop" do |vmware|
    vmware.gui = true
    vmware.allowlist_verified = true
   end
 end
