
Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/focal64"
  config.vm.synced_folder  "./ansible", "/etc/ansible"
  config.vm.synced_folder  "./app", "/var/www/html"
  config.vm.network  "public_network"
  

  # Enable provisioning with a shell script. Additional provisioners such as
  # Ansible, Chef, Docker, Puppet and Salt are also available. Please see the
  # documentation for more information about their specific syntax and use.
   config.vm.provision "shell", inline: <<-SHELL
     sudo apt-get update
     sudo apt install -y software-properties-common
     sudo add-apt-repository --yes -update ppa:ansible/ansible
     sudo apt install -y ansible
     ansible-playbook /etc/ansible/playbooks/nginx.yml
   SHELL
end
