Vagrant.configure("2") do |config|
  config.vm.box = "debian/contrib-stretch64"
  config.vm.boot_timeout = 0

  # Enable caching
  # Install with
  #   vagrant plugin install vagrant-cachier

  # Set the box up vaguely close to lug.org.uk "live"
  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook            = "prepare.yml"
    ansible.install_mode        = :pip
  end

  config.vm.provision "ansible_local", run: "always" do |ansible|
    ansible.playbook            = "site.yml"
    ansible.install_mode        = :pip
#    ansible.vault_password_file = "Vault-Password"
###  Only required when we start using Vault to hide SSH keys and users ###
  end

#  config.vm.define :admin do |admin|
#    admin.vm.hostname = "admin.lug.org.uk"
#  end

  config.vm.define "web-01" do |web01|
    web01.vm.hostname = "web-01.lug.org.uk"
  end

#  config.vm.define :mailin01 do |mailin01|
#    mailin01.vm.hostname = "mail-in-01.lug.org.uk"
#  end

  config.vm.define :snm do |snm|
    snm.vm.hostname = "snm.lug.org.uk"
  end

#  config.vm.define :mailman do |mailman|
#    mailman.vm.hostname = "mailman.lug.org.uk"
#  end

end
