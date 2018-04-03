VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # Use the same key for each machine
  config.ssh.insert_key = false

  config.vm.define "vagrant1" do |vagrant1|
    vagrant1.vm.box = "ubuntu/trusty64"
    #vagrant1.vm.network "private_network", ip: "192.168.35.10"
    config.vm.provision "ansible" do |ansible|
      ansible.verbose = "vvv"
      ansible.playbook = "provisioning/vagrant1/main.yml"
    end
  end
  config.vm.define "vagrant2" do |vagrant2|
    vagrant2.vm.box = "ubuntu/trusty64"
    #vagrant2.vm.network "private_network", ip: "192.168.35.11"
    config.vm.provision "ansible" do |ansible|
      ansible.verbose = "vvv"
      ansible.playbook = "provisioning/vagrant2/installdocker.yml"
    end
  end
end
