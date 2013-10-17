Vagrant.configure("2") do |config|
  config.vm.box = "precise32"
  config.vm.box_url = "http://files.vagrantup.com/precise32.box"

  config.vm.network :private_network, ip: "192.168.42.42"

  config.vm.synced_folder "www/", "/srv/www"

  config.vm.provision "chef_solo" do |chef|
    chef.add_recipe "apache2"

    chef.json = {
      "apache" => {
        "default_site_enabled" => true,
        "docroot_dir" => "/srv/www"
      }
    }
  end
end
