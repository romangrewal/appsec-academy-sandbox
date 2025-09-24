Vagrant.configure("2") do |config|
  config.vm.box = "centos/stream9"
  config.vm.box_version = "20250922.0"
  config.vm.hostname = "localhost"
  
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "infrastructure/ansible/dependencies.yml"
    ansible.inventory_path = "infrastructure/ansible/inventory.ini"
    ansible.sudo = true
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "infrastructure/ansible/owaspjuiceshop.yml"
    ansible.inventory_path = "infrastructure/ansible/inventory.ini"
    ansible.sudo = true
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "infrastructure/ansible/tirreno.yml"
    ansible.inventory_path = "infrastructure/ansible/inventory.ini"
    ansible.sudo = true
  end

end
