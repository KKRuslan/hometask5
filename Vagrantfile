Vagrant.configure("2") do |config|

    config.vm.box = "centos/7"
  
    config.vm.provision "shell", inline: <<-SHELL
	      mkdir /etc/folder1
        mkdir /etc/folder2
        cp /vagrant/mv.service /etc/systemd/system/mv.service
        systemctl daemon-reload
        systemctl start mv.service
        systemctl enable mv.service
    SHELL
  end
