# -*- mode: ruby -*-
# vi: set ft=ruby :

ENV['VAGRANT_DEFAULT_PROVIDER'] = 'libvirt'
Vagrant.configure(2) do |cnf|
  cnf.vm.define 'camel' do |machine|
    #machine.vm.box = "fedora/27-cloud-base"
    #machine.vm.box_version = "20171105"
    machine.vm.box = 'centos/7'
    machine.vm.box_url = machine.vm.box
    machine.vm.provider 'libvirt' do |prv|
      prv.nested = true
      prv.memory = 2048
      prv.cpus = 1
    end
     cnf.vm.provision "ansible" do |ansible|
    	ansible.playbook = "playbook.yml"
     end
  end
end
