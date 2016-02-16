
image="ubuntu/trusty64"
dev_dir ="./"

Vagrant.configure("2") do |config|

	# Specify the base box
    config.vm.box = "#{image}"

    # Setup synced folder
    config.vm.synced_folder "#{dev_dir}", "/projects"



    # Shell provisioning
    config.vm.provision "shell" ,inline: <<-SHELL
      sudo apt-get update
      sudo apt-get install -y software-properties-common
      sudo apt-get install -y git
      sudo apt-get install -y nodejs-legacy
      sudo apt-get install -y npm
      sudo apt-get install -y python-pip
      sudo pip install ansible
      sudo pip install awscli
      sudo pip install boto
      sudo npm install azure-cli -g
      echo "export ANSIBLE_HOST_KEY_CHECKING=False" >> ~/.profile
      echo "export ANSIBLE_SSH_ARGS='-o IdentitiesOnly=yes'" >> ~/.profile
    SHELL


end
