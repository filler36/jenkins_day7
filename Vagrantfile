Vagrant.configure("2") do |config|
  
  config.vm.define "nexus" do |nexus|
    nexus.vm.box = "sbeliakou/centos"
    nexus.vm.hostname = "nexus"
    nexus.vm.network "private_network", ip: "192.168.56.112"
    nexus.vm.provider "virtualbox" do |vb|
      vb.name = "nexus"
      vb.memory = "1024"
    end
    nexus.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook.yml"
    end
  end

end

