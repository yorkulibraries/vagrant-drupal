# vagrant-drupal
Setup a box with drupal

## Installation
```
git clone git@github.com:yorkulibraries/vagrant-drupal.git
git clone git@github.com:yorkulibraries/linux_playbooks.git
cd vagrant-drupal
ansible-galaxy install -r requirements.yml 
```

### Vagrant up
```
vagrant up
```

## Edit /etc/hosts

Add an entry for drupal.me.ca in /etc/hosts file
```
192.168.168.168 drupal.me.ca
```

## Site URL
http://drupal.me.ca
