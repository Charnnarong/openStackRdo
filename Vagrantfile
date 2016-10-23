# -*- mode: ruby -*-
# vi: set ft=ruby :
required_plugins = %w(vagrant-vbguest)
required_plugins.each do |plugin|
  system "vagrant plugin install #{plugin}" unless Vagrant.has_plugin? plugin
end
# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|

  config.vbguest.auto_update = true

  config.vm.define "ostk" do |d|
    d.vm.box = "centos/7"
    d.vm.hostname = "ostk"
    d.vm.network "private_network" , ip: "10.100.192.10"
    d.vm.synced_folder "./resources", "/vagrant"
    d.vm.provision :shell, path: "scripts/passwordAuthentication.sh"
    d.vm.provision :shell, path: "scripts/bootstrap_ansible.sh"
    d.vm.provision :shell, inline: "PYTHONUNBUFFERED=1 ansible-playbook /vagrant/ansible/rdoQuickStart.yml -c local -vvvvv"
    d.vm.provider "virtualbox" do |v|
      v.memory = 6144
      v.cpus = 4
    end
  end

end
