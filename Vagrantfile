# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.define 'spine1' do |spine1|
    spine1.vm.box = "cisco/nxosv-7.0.3.I7.3"
    #spine1.vm.network 'private_network', virtualbox__intnet: 'e1', ip: '169.254.1.11', auto_config: false

    spine1.vm.provider "virtualbox" do |vb|
    # Customize the amount of memory on the VM:
      vb.memory = "2048"
      vb.customize ["modifyvm", :id, "--uart1", "0x3f8", "4"]
      vb.customize ["modifyvm", :id, "--uartmode1", "tcpserver", "2023"]
    end
  end

  config.vm.define 'spine2' do |spine2|
    spine2.vm.box = "cisco/nxosv-7.0.3.I7.3"
    #spine2.vm.network 'private_network', virtualbox__intnet: 'e1', ip: '169.254.1.11', auto_config: false

    spine2.vm.provider "virtualbox" do |vb|
    # Customize the amount of memory on the VM:
      vb.memory = "2048"
      vb.customize ["modifyvm", :id, "--uart1", "0x3f8", "4"]
      vb.customize ["modifyvm", :id, "--uartmode1", "tcpserver", "2024"]
    end
  end
end