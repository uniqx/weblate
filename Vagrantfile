Vagrant.configure("2") do |config|

  config.vm.box = "debian/buster64"
  config.vm.network "forwarded_port", guest: 8080, host: 8080


  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "vagrant.playbook.yml"
    ansible.install_mode = "apt"
  end

  config.vm.provider :libvirt do |libvirt|
    libvirt.cpus = 2
    libvirt.memory = 4096
  end

end
