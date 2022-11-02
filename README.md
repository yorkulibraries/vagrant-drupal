# vagrant-drupal
Setup a box with drupal and Bootstrap Barrio theme for development. This is a slightly simpler setup than [Drupal VM](https://www.drupalvm.com/).

## Installation
```
git clone git@github.com:yorkulibraries/vagrant-drupal.git
cd vagrant-drupal
git clone git@github.com:yorkulibraries/linux_playbooks.git
git clone git@github.com:yorkulibraries/yudl_barrio.git custom/yudl_barrio
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

## Admin 
```
User: admin
Pass: admin
```

# Making changes to the yudl_barrio theme
The folder **custom** is sync'ed with **/var/www/drupal/web/themes/custom/** so any changes to this folder is reflected on the site.

You should be able to make changes to the **/var/www/drupal/web/themes/custom/yudl_barrio/** files to see the changes reflected immediately.

