Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.network "forwarded_port", guest: 80, host: 8080
   config.vm.network "private_network", ip: "192.168.56.2"
   config.vm.network "private_network", ip: "192.168.57.2"
  #  maquina host - maquina remota
   config.vm.synced_folder "../data", "/vagrant_data", SharedFoldersEnableSymlinksCreate: false
   config.vm.provision "shell", inline: <<-SHELL
     apt-get update
     apt-get install -y apache2
     apt-get install -y nginx
     apt-get install -y htop
     apt-get install -y python3
     apt-get install -y nano
   SHELL
end
