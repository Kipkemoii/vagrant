Vagrant.configure("2") do |config|
  config.vm.define "master" do |master|
    #Base image
    master.vm.box = "rockylinux/9"

    #Hostname
    master.vm.hostname = "master"

    #Network
    master.vm.network "private_network", type: "dhcp"

    #Provider
    master.vm.provider "virtualbox" do |v|
      v.name = "master"
      v.cpus = 2
      v.memory = 2048
    end 
  end

  config.vm.define "worker1" do |worer1|
    #Base image
    worer1.vm.box = "rockylinux/9"

    #Hostname
    worer1.vm.hostname = "master"

    #Network
    worer1.vm.network "private_network", type: "dhcp"

    #Provider
    worer1.vm.provider "virtualbox" do |v|
      v.name = "master"
      v.cpus = 2
      v.memory = 2048
    end 
  end
end
