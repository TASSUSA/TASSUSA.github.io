Vagrant::Config.run do |config|

  config.vm.box = "precise32"
  config.vm.box_url = "http://files.vagrantup.com/precise32.box"
  config.vm.forward_port 4000, 4000
  config.vm.provision :shell,
    :inline => "sudo apt-get update && sudo apt-get -y install curl build-essential git && gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 && curl -sSL https://get.rvm.io | bash -s stable --ruby && rvm install 2.2.3 && source /usr/local/rvm/scripts/rvm && /usr/local/rvm/bin/rvm use 2.2.3 && sudo /opt/vagrant_ruby/bin/gem install redcarpet github-pages"

  config.ssh.forward_agent = true
end

#gem install redcarpet
#gem install github-pages
#sudo apt-get update && sudo apt-get -y install curl build-essential git ruby && sudo /opt/vagrant_ruby/bin/gem install github-pages

#sudo apt-get update && sudo apt-get -y install curl build-essential git && gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 && curl -sSL https://get.rvm.io | bash -s stable --ruby && rvm install 2.2.3 && source /usr/local/rvm/scripts/rvm && /usr/local/rvm/bin/rvm use 2.2.3 && sudo /opt/vagrant_ruby/bin/gem install github-pages --no-ri --no-rdoc