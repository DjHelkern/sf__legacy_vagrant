Vagrant.configure("2") do |config|
  config.vm.box = "generic/centos6"
  config.vm.define "postgresql-8-4"
  config.vm.hostname = "postgresql" 
  config.vm.network "forwarded_port", guest: 5432, host: 5432

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "4096"
    vb.cpus = 2
  end

  config.vm.provision "shell", inline: <<-SHELL
    yum -y update
    yum -y install postgresql-server postgresql postgresql-contrib
    /etc/rc.d/init.d/postgresql initdb
    /etc/init.d/postgresql start
  SHELL
end
