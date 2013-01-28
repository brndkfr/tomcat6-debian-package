Glassfish3 Debian Package
=========================

The purpose of this project is to provide a debian package for Tomcat6 in cases the newest version is not available in debian or ubuntu repositories.

Build
-----

The package is build using [Gradle] [1] so make sure it is installed on your system. After having downloaded the official Glassfish archive and placed it at the root of this checked out project:

    wget http://download.java.net/glassfish/3.1.2.2/release/glassfish-3.1.2.2.zip .
    gradle unzip

and create the package

    gradle clean debian

Finally, copy or publish the file `target/tomcat6.0.xx.deb`.

Installation
------------

To install the package, follow the usual Debian way of doing things (if you haven't set up a apt repository):

    sudo dpkg -i tomcat6.0.xx.deb


