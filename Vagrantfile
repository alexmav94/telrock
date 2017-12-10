Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
   config.vm.box_check_update = false
   config.vm.network "private_network", ip: "192.168.33.10"
   config.vm.synced_folder ".", "/vagrant"
   config.vm.provider "virtualbox" do |vb|
     vb.memory = "1024"
   end
 
  config.vm.provision "ansible" do |ansible|
   ansible.playbook = "provisioning/playbook.yml"
   end
end
