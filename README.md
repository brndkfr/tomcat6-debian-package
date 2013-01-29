Tomcat6 Debian Package
=========================

The purpose of this project is to provide a debian package for Tomcat6 in cases the newest version is not available in debian or ubuntu repositories.

It is inspired by the [glassfish3-debian-package](https://github.com/vbossica/glassfish3-debian-package) project  from [vbossica](https://github.com/vbossica)

Warning
-------
not finalized. do not use.


Build
-----

	mvn clean install
	
* Will download the apache-tomcat-6.0.xx.zip from the website regarding to the version in the pom.xml -> project.version	

* generates debian package

* Finally, copy or publish the file `target/tomcat6.0.xx.deb`.

Installation
------------

To install the package, follow the usual Debian way of doing things (if you haven't set up a apt repository):

    sudo dpkg -i tomcat6.0.xx.deb

	
Plugin configuration
--------------------

* configuration is done via the properties section in the pom.xml and the project.version

### switching to an newer tomcat6 version

* set the `<version>` tag in the pom.xml to the new version, for example 6.0.100
* copy the md5-checksum from the download page into property `<tomcat6-md5>`
* rebuild project


### switching download link

* choose a different mirror download link from the download site, for example: http://www.eu.apache.org/dist/tomcat/tomcat-6/v6.0.36/bin/apache-tomcat-6.0.36.zip
* modify `<tomcat6-base-download-url>` to 
		http://www.eu.apache.org/dist/tomcat/tomcat-6/${project.version}/bin/
	

