--Multi-VM Vagrant Configuration-- \
This repository contains a Vagrantfile for setting up and managing a multi-VM environment using Vagrant. It includes configurations for three virtual machines:\
  ->Web01: Ubuntu 20.04-based VM configured as a web server.\
  ->Web02: Ubuntu 20.04-based VM configured as a secondary web server.\
  ->DB01: CentOS Stream 9-based VM configured as a database server.\\\

#Features\
 -> Private and Public Networking:\
 -> Each VM has a private network IP for internal communication.\
 -> Public network configuration for external connectivity.\
 -> Custom Resource Allocation:\
 -> Web01 is allocated 1 CPU and 1024 MB of RAM.\
 -> Provisioning:\
 -> DB01 is provisioned with a shell script to update system packages.\\\

#Requirements\
  ->Vagrant: Version 2.2.0 or higher\
  ->VirtualBox: Version 6.0 or higher (or any other Vagrant-supported provider)\\\

#Setup Instructions\
  ->Clone the repository:\
  ->go to related directory\
  ->Start the virtual machines:\
      ->vagrant up\
  #Access the virtual machines:\
    ->Web01: vagrant ssh web01-ubuntu20\
    ->Web02: vagrant ssh web02-ubuntu20\
    ->DB01: vagrant ssh db01-centos\
  #Stop the VMs:\
    ->vagrant halt (you can halt together all at once  and one by one when you want to like vagrant up)\\\


#Usage\
-This setup is ideal for:\\

  ->Testing multi-tier application environments.\
  ->Simulating production-like infrastructure.\
  ->Learning or teaching Vagrant and VM networking.\
  ->Feel free to customize and improve the configurations as per your requirements! 😊
