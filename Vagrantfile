# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.provision "shell", path: "sshd.sh"
 
  config.vm.box = "centos/7"
  config.vm.box_version = "1905.1"

  config.vm.network "private_network", ip: "192.168.58.101"  

  config.vm.provider "virtualbox" do |vb|

  vb.customize ["modifyvm", :id, "--memory", "4096", "--cpus", "2"]
  
  end

  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "/Users/ulissesrodrigues/Development/byside/ansible/ansible-playbook-new-host/ansible-playbook-new-host.yml"
  end

end
