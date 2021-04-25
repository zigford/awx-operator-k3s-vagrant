# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.provider :libvirt do |libvirt|
    libvirt.memory = "4096"
    libvirt.cpus = 4
    libvirt.disk_driver :cache => 'unsafe'
  end  # The most common configuration options are documented and commented below.
  config.vm.box = "centos/8"
  config.vm.network "private_network", ip: "192.168.33.10"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "main.yml"
  end
end
