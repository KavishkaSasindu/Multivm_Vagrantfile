Vagrant.configure("2") do |config|
    config.vm.define "web01-ubuntu20" do |web01|
        web01.vm.box = "ubuntu/focal64"
        web01.vm.hostname = "web01"
        web01.vm.network  "private_network", ip: "192.168.56.30"
        web01.vm.network  "public_network"

        web01.vm.provider "virtualbox" do |vb|
            vb.memory = "1024"
            vb.cpus = "1"
        end    
    end
    
    config.vm.define "web02-ubuntu20" do |web02|
        web02.vm.box = "ubuntu/focal64"
        web02.vm.hostname = "web02"
        web02.vm.network  "private_network", ip: "192.168.56.32"
        web02.vm.network  "public_network"

        web02.vm.provider "virtualbox" do |vb|
            vb.memory = "1024"
            vb.cpus = "1"
        end
    end

    config.vm.define "db01-centos" do |db01|
        db01.vm.box = "eurolinux-vagrant/centos-stream-9"
        db01.vm.hostname = "db01"
        db01.vm.network  "private_network", ip: "192.168.56.34"
        db01.vm.network  "public_network"

        db01.vm.provider "virtualbox" do |vb|
            vb.memory = "1024"
            vb.cpus = "1"
        end

        db01.vm.provision "shell" , inline: <<-SHELL
            yum install wget mariadb-server unzip -y
            systemctl start mariadb
            systemctls enable mariadb
        SHELL
    end
end

