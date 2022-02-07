
VAGRANTFILE_API_VERSION = "2"
VAGRANTFILE_VM_BOX = "ubuntu/impish64"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.define 'cicd-toolbox' do |cicdtoolbox|
    cicdtoolbox.ssh.insert_key = false
    cicdtoolbox.vm.box = VAGRANTFILE_VM_BOX
    cicdtoolbox.vm.hostname = 'cicdtoolbox'
    cicdtoolbox.vm.network "private_network", ip: ""
    cicdtoolbox.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.memory = "4096"
      vb.cpus = 2
    end
     cicdtoolbox.vm.provision "shell", path: "vmSetup.sh"
  end
end
