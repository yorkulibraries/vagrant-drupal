app = ENV['APP'] || 'drupal'

Vagrant.configure("2") do |config|
  config.vm.hostname = "vagrant"
  config.vm.box = "bento/ubuntu-20.04"
  config.vm.define "vagrant-#{app}"
  config.vm.provider "virtualbox" do |vb|
    # Customize the amount of memory on the VM:
    vb.memory = "2048"
    vb.name = "vagrant-#{app}"
  end
  config.vm.network :private_network, ip: "192.168.168.168"
  config.vm.provision "ansible" do |ansible| 
    ansible.playbook="provision.yml" 
    ansible.extra_vars = {
      users_to_create: [],
      sudoers: []
    } 

  end 

  def provisioned?(vm_name='default', provider='virtualbox')
    File.exist?(".vagrant/machines/#{vm_name}/#{provider}/action_provision")
  end

  config.vm.synced_folder "custom", "/var/www/drupal/web/themes/custom", create: false, mount_options: ["dmode=775,fmode=664"], fsnotify: true, exclude: []
  
end
