# Simple Vagrant Apache

## You gots to have
* Virtualbox
* Vagrant

## Now for the complex setup

    vagrant up

Apache will now be running on an Ubuntu box accessible on `http://192.168.42.42/`.

## Optionally configure your hosts file with a nice DNS:

    sudo echo '192.168.42.42 local.dev' >> /etc/hosts

