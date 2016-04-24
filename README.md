Vagrant Tomcat 7
============

Want to get a Tomcat stack to develop without having to install it on your local machine ?

If you find yourself needing quick to configure web stack, but also one that is customizable try this Vagrant project

Vagrant allows for Virtual Machines to be quickly setup, and easy to use.

And this project aims to make it very easy to spinup a Tomcat stack in a matter of minutes.

Requirements
------------
* VirtualBox <http://www.virtualbox.com>
* Vagrant <http://www.vagrantup.com>
* Git <http://git-scm.com/>

Usage
-----

### Startup

1. Clone this repository
2. From the command-line:
```
$ vagrant up
```
That is pretty simple.

### Connecting

#### Tomcat
The Tomcat server is available at <http://localhost:8080> and the Tomcat Manager is available at <http://localhost:8080/manager> in its GUI and script form (useful for deploying from Maven using the [Tomcat7 Maven Plugin](https://tomcat.apache.org/maven-plugin-2.0/tomcat7-maven-plugin/))

#### MySQL
Externally the MySQL server is available at port 8889, and when running on the VM it is available as a socket or at port 3306 as usual.
Username: root
Password: root

Technical Details
-----------------
* Ubuntu 14.04 64-bit
* Tomcat 7 and Tomcat Manager
* MySQL 5.6
* OpenJDK 7

We are using the base Ubuntu 14.04 box from Vagrant. If you don't already have it downloaded
the Vagrantfile has been configured to do it for you. This only has to be done once
for each account on your host computer.

The web root is located in the project directory at `src/` and you can install your files there

And like any other vagrant file you have SSH access with
```
$ vagrant ssh
```

Acknowledgements
----------------

This Vagrant project is inspired by <https://github.com/mattandersen/vagrant-lamp>.

