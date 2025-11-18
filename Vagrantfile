IMAGE_ubuntu_2204   = "bento/ubuntu-22.04"
IMAGE_Debian_12     = "bento/debian-12"

ENV['VAGRANT_NO_PARALLEL'] = 'yes'

Vagrant.configure(2) do |config|
  #config.vm.provision "shell", path: "bootstrap.sh"

  NodeType1 = 1
  (1..NodeType1).each do |type1_id|
    config.vm.define "type1#{type1_id}" do |type1_vm|
      type1_vm.vm.box = IMAGE_Debian_12
      type1_vm.vm.hostname = "type1#{type1_id}"
      #type1_vm.vm.network "private_network", ip: "192.168.56.10#{type1_id}"
	  type1_vm.vm.network "public_network"
      type1_vm.vm.provider "virtualbox" do |v|
        v.name = "type1#{type1_id}"
        v.memory = 1024
        v.cpus = 1
      end
      # type1_vm.vm.provision "shell", path: "bootstrap_t1.sh"
    end
  end
  


  NodeType2 = 1
  (1..NodeType2).each do |type2_id|
    config.vm.define "type2#{type2_id}" do |type2_vm|
      type2_vm.vm.box = IMAGE_Debian_12
      type2_vm.vm.hostname = "type2#{type2_id}.example.com"
      #type2_vm.vm.network "private_network", ip: "192.168.56.11#{type2_id}"
	  type2_vm.vm.network "public_network" 
      type2_vm.vm.provider "virtualbox" do |v|
        v.name = "type2#{type2_id}"
        v.memory = 1024
        v.cpus = 1
      end
      # type2_vm.vm.provision "shell", path: "bootstrap_t2.sh"
	end
  end
 
 


NodeType3 = 1
  (1..NodeType3).each do |type3_id|
    config.vm.define "type3#{type3_id}" do |type3_vm|
      type3_vm.vm.box = IMAGE_Debian_12
      type3_vm.vm.hostname = "type3#{type3_id}.example.com"
      #type2_vm.vm.network "private_network", ip: "192.168.56.11#{type3_id}"
	  type3_vm.vm.network "public_network" 
      type3_vm.vm.provider "virtualbox" do |v|
        v.name = "type3#{type3_id}"
        v.memory = 1024
        v.cpus = 1
      end
      # type2_vm.vm.provision "shell", path: "bootstrap_t2.sh"
    end
  end




NodeType4 = 1
  (1..NodeType4).each do |type4_id|
    config.vm.define "type4#{type4_id}" do |type4_vm|
      type4_vm.vm.box = IMAGE_Debian_12
      type4_vm.vm.hostname = "type4#{type4_id}.example.com"
      #type4_vm.vm.network "private_network", ip: "192.168.56.11#{type2_id}"
	  type4_vm.vm.network "public_network" 
      type4_vm.vm.provider "virtualbox" do |v|
        v.name = "type4#{type4_id}"
        v.memory = 1024
        v.cpus = 1
      end
      # type2_vm.vm.provision "shell", path: "bootstrap_t2.sh"
    end
 end
end