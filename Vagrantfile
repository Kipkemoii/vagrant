Vagrant.configure("2") do |config|
  config.vm.provision "shell", inline: "echo Hello"
  config.vm.define "master" do |master|
    #Base image
    master.vm.box = "rockylinux/9"

    #Hostname
    master.vm.hostname = "master"

    #Network
    master.vm.network "public_network", type: "dhcp"

    #Provider
    master.vm.provider "virtualbox" do |v|
      v.name = "master"
      v.cpus = 2
      v.memory = 2048
    end 

    # default router
    master.vm.provision "shell",
    run: "always",
    inline: "ip route del default via 10.0.2.2 || true"
  end

  config.vm.define "worker1" do |worer1|
    #Base image
    worker1.vm.box = "rockylinux/9"

    #Hostname
    worker1.vm.hostname = "worker1"

    #Network
    worker1.vm.network "public_network", type: "dhcp"

    #Provider
    worker1.vm.provider "virtualbox" do |v|
      v.name = "worker1"
      v.cpus = 2
      v.memory = 2048
    end
    # default router
    worker1.vm.provision "shell",
    run: "always",
    inline: "ip route del default via 10.0.2.2 || true" 
  end
end
