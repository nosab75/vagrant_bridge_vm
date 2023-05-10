Vagrant.configure("2") do |config|
   config.vm.define "server1" do |srv1|
    srv1.vm.box = "generic/ubuntu1804"
    srv1.vm.hostname = 'ubuntu1'
    srv1.vm.network :public_network, ip: "192.168.1.98"
    srv1.vm.box_download_insecure=true
   end

   config.vm.define "server2" do |srv2|
    srv2.vm.box = "generic/ubuntu1804"
    srv2.vm.hostname = 'ubuntu2'
    srv2.vm.network :public_network, ip: "192.168.1.99"
    srv2.vm.box_download_insecure=true
   end

# Fournisseur
    config.vm.provider "virtualbox" do |v|
     # v.gui = true
      v.memory = 1024
      v.cpus = 1
    end
end
