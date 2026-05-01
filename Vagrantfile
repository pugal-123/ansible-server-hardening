Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/jammy64"
  config.vm.hostname = "hardened-server"
  config.vm.network "private_network", ip: "192.168.56.10"
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
    vb.cpus = 1
    vb.name = "hardened-server"
  end
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "site.yml"
    ansible.inventory_path = "inventory.ini"
    ansible.verbose = "v"
  end
end
