Vagrant.configure("2") do |config|
#  config.vm.box = "geerlingguy/ubuntu1604"
#  config.vm.box = "bento/ubuntu-16.04"
  config.vm.box = "box-cutter/ubuntu1404-desktop"

  config.vm.provider "virtualbox" do |vb|
    vb.gui = true
    vb.memory = "1024"
  end

  config.vm.provision "shell", inline: <<-SHELL
    #apt-get update
    #apt-get install -y ansible
  SHELL

  config.vm.provision :ansible do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "ubuntuvm.yml"
  end
end
