Virtual Machines
=======
The virtual machines in this repository leverage Vagrant and Puphpet/puppet to provision all the dependencies required to start working with PHP-IO.

Available Instances
------------
php-uv: PHP 5.5, MySQL, Apache and php-uv extension

Set up
------------
After cloning the repository before running "vagrant up" you may want to make a few modifications to the virtual machine configuration.

**Local Development Directory:**
The virtual machine will mount a directory on your host machine.  This will allow you to continue developing as you normally would.  Currently the default location for development files is: **/var/www**.  If your development files are located elsewhere than you will want to make a modification to the configuration before provisioning the vm.

Change synched folder location:

1. Open the config.yaml file: puphpet/config.yaml
2. Change vagrantfile-local:vm:synced_folder:6cH1AsAnXHnf:source to the location of your development folder.
3. Save Changes

**Add Hosts Entry**
The default host name is **local.dev**.  In order for you to access this domain on your host machine you will need to make an entry in your /etc/hosts file.

1. Open /etc/hosts and add:
```
192.168.56.102  local.dev
```

Usage
------------
**Start VM**
To start the VM change into the directory that contains your VagrantFile.
```
$: cd vagrant-vm
$: vagrant up
```

**SSH into VM**
```
$: vagrant ssh
```

VM Information
------------
**OS:** debian

**IP:** 192.168.56.102

**Host:** local.dev

**MySQL User:** root

**MySQL Password:** root

**Web Server User:** www-data

**Web Server Directory:** /var/www/site

**Apache Installed Modules:** php, rewrite

