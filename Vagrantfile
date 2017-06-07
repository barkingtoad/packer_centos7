# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.ssh.insert_key = false
  config.vm.synced_folder '.', '/vagrant', type: 'nfs'

  # VMware Fusion.
  # `vagrant up vmware --provider=vmware_fusion`
  config.vm.define "vmware" do |vmware|
    vmware.vm.hostname = "centos7-vmware"
    vmware.vm.box = "file://../../../builds/vmware-centos7.box"
    vmware.vm.network :private_network, ip: "192.168.3.2"

    config.vm.provider :vmware_fusion do |v, override|
      v.gui = false
      v.vmx["memsize"] = 1024
      v.vmx["numvcpus"] = 1
    end

    config.vm.provision "shell", inline: "echo Hello, World"
  end


    config.vm.provision "shell", inline: "echo Hello, World"
  end

end
