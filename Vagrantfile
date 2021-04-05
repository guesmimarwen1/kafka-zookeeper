
Vagrant.configure("2") do |config|
 
  config.vm.box = "hashicorp/bionic64"

  config.ssh.insert_key = false

  config.vm.provider "virtualbox"

  config.vm.hostname = "MyHost"
  # http
  config.vm.network "forwarded_port", guest: 80, host: 8080,
  auto_correct: true
  
  

  
  
  config.vm.network "public_network", bridge: "en1: Wi-Fi (AirPort)"
  
  
  config.ssh.private_key_path = ["~/.ssh/id_rsa", "~/.vagrant.d/insecure_private_key"]
  config.vm.provision "file", source: "~/.ssh/id_rsa.pub", destination: "~/.ssh/authorized_keys"
  config.ssh.username = "vagrant"
  config.ssh.password = "vagrant"  
 
  #First MC 
  
  config.vm.define "MC2" do |mc|
    mc.vm.hostname = 'MC2'
  end  

  config.vm.define "MC3" do |mc|
    mc.vm.hostname = 'MC3'
  end 
  
  config.vm.define "MC0" do |mc|
    mc.vm.hostname = 'MC0'
  end 

  config.vm.define "MC4" do |mc|
    mc.vm.hostname = 'MC4'
  end 
    
end

