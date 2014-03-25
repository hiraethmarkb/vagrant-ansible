# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # Box config
  config.vm.box = "centos65-x86_64-20131205"
  config.vm.box_url = "https://github.com/2creatives/vagrant-centos/releases/download/v6.5.1/centos65-x86_64-20131205.box"

  # Network config
  config.vm.network :forwarded_port, guest: 80, host: 8080
  config.vm.network :private_network, ip: "192.168.33.10"

  # VM provider config
  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "256"]
  end

  # VM provisioning config - yay! we're using ansible
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provisioning/playbook.yml"
    #ansible.inventory_path = "provisioning/ansible_hosts"
    ansible.host_key_checking = "false"
    #ansible.verbose = "v"
    #ansible.verbose = "vv"
    #ansible.verbose = "vvv"
    #ansible.verbose = "vvvv"
  end

end
