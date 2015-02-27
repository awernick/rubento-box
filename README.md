# Rubento-Box
Base Vagrant box for Ruby on Rails development on CentOS 7

## Requirements
  * Virtualbox
  * Vagrant

## Deployment
Building the virtual machine is this easy:
```shell
host $ cd rails-app-dir
host $ curl -O https://raw.githubusercontent.com/awernick/rubento-box/master/Vagrantfile
host $ vagrant up
```
That's it.

After the installation has finished, you can access the virtual machine with
```
host $ vagrant ssh
...
[vagrant@localhost ~]$
```
Port 3000 in the host computer is forwarded to port 3000 in the virtual machine. Thus, applications running in the virtual machine can be accessed via localhost:3000 in the host computer. Be sure the web server is bound to the IP 0.0.0.0, instead of 127.0.0.1, so it can access all interfaces:
```
rails server -b 0.0.0.0
```

## What's In The Box
  * Git
  * SQLite3
  * RVM (includes Ruby 2.2.0)
  * Rails 4.2.0
  * Bundler

## Virtual Machine Management

When done just log out with `^D` and suspend the virtual machine

    host $ vagrant suspend

then, resume to hack again

    host $ vagrant resume

Run

    host $ vagrant halt

to shutdown the virtual machine, and

    host $ vagrant up

to boot it again.

You can find out the state of a virtual machine anytime by invoking

    host $ vagrant status

Finally, to completely wipe the virtual machine from the disk **destroying all its contents**:

    host $ vagrant destroy # DANGER: all is gone

Please check the [Vagrant documentation](http://docs.vagrantup.com/v2/) for more information on Vagrant.

## Access

Vagrant has been havinga few problems with SSH acess for new base boxes created with version 1.7.2. The following is the username and the password for vagrant account in case SSH public key access stops working
```
#vagrant
username: vagrant
password: vagrant
```
=======
# rubento-box
Base Vagrant box for Ruby on Rails development on CentOS 7
