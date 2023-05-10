Vagrant.configure("2") do |config|
  srv1.vm.box = "generic/ubuntu1804"
  config.vm.hostname = "app1"
  config.vm.network :public_network
  config.vm.box_download_insecure=true

# Fournisseur
    config.vm.provider "virtualbox" do |v|
     # v.gui = true
      v.memory = 1024
      v.cpus = 1
    end
end


Vagrant.configure("2") do |config|
config.vm.define "server1" do |srv1|
srv1.vm.box = ".\\ubuntu-20.04-0.1.box"
srv1.vm.hostname = 'ubuntu1'
srv1.vm.network :public_network, ip: "192.168.1.98"
srv1.vm.provision :shell, :path => "master.sh"
end
config.vm.define "server2" do |srv2|
srv2.vm.box = ".\\ubuntu-20.04-0.1.box"
srv2.vm.hostname = 'ubuntu2'
srv2.vm.network :public_network, ip: "192.168.1.99"
srv2.vm.provision :shell, :path => "slave.sh"
end
end