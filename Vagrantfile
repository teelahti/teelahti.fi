# vi: set ft=ruby :
# -*- mode: ruby -*-

Vagrant.configure(2) do |config|
	config.vm.box = "ubuntu/trusty64"
	config.vm.hostname = "jekyll"
	config.vm.network "forwarded_port", host: 4000, guest: 4000
  config.vm.synced_folder ".", "/src"
	config.vm.provision "shell", path: "vagrant-bootstrap.sh", privileged: false

	config.ssh.forward_agent = true
end