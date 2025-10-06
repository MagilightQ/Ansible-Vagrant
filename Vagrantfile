Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/jammy64"
  config.vm.network "forwarded_port", guest: 80, host: 8080

  config.vm.define "webserver" do |web|
    web.vm.hostname = "webserver"
    web.vm.network "private_network", ip: "192.168.56.10"

    web.vm.provider "virtualbox" do |vb|
      vb.name = "ansible-webserver"
      vb.memory = 1024
      vb.cpus = 1
    end

    web.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbooks/site.yml"
      ansible.inventory_path = "inventory/hosts"
      ansible.limit = "all"
    end
  end
end
