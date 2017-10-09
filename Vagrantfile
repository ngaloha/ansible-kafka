Vagrant.configure("2") do |config|

  config.vm.define :master do |master|
    master.vm.box = "centos/6"
    master.vm.provider :virtualbox do |v|
      v.name = "node-1"
      v.customize ["modifyvm", :id, "--memory", "2048"]
    end
    master.vm.network :private_network, ip: "10.211.55.100"
    master.vm.hostname = "node-1"
  end

  config.vm.define :ansible do |ansible|
    ansible.vm.box = "centos/6"
    ansible.vm.provider :virtualbox do |v|
      v.name = "ansible"
      v.customize ["modifyvm", :id, "--memory", "1024"]
    end
    ansible.vm.network :private_network, ip: "10.211.55.102"
    ansible.vm.network "public_network"
    ansible.vm.hostname = "ansible"
  end

end
