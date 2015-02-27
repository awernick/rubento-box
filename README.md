# Rubento-Box
Base Vagrant box for Ruby on Rails development on CentOS 7

## Requirements
  * Virtualbox
  * Vagrant

## Deployment
  ```shell
  host $ git clone https://github.com/awernick/rubento-box.git
  host $ cd rubento-box
  host $ vagrant up
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
