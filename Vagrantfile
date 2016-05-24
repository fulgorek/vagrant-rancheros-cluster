
# -*- mode: ruby -*-
# vi: set ft=ruby :

nodes = {
  :count => 2,
  :mem   => 512,
  :cpus  => 1
}

Vagrant.configure(2) do |config|
  config.vm.box = "rancherio/rancheros"

  (1..nodes[:count]).each_with_index do |index|
      hostname = "rancher-%02d" % index
      ipv4     = "192.168.50.#{index+99}"
      ssh_port = "#{index+2399}"

      # config.ssh.private_key_path = ['~/.vagrant.d/insecure_private_key', '~/.ssh/id_rsa']
      config.vm.provider "virtualbox" do |v|
         v.linked_clone = true
         v.cpus         = nodes[:cpus] || 1
         v.memory       = nodes[:mem] || 512
      end

      config.vm.define hostname do |m|
        m.vm.synced_folder ".", "/vagrant", disabled: true
        m.vm.network :forwarded_port, guest: 22, host: ssh_port, id: 'ssh'
      end

      config.vm.network :private_network, ip: ipv4, auto_config: false
  end
end
