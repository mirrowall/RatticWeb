RatticWeb
=========

Build Status: [![Build Status](https://travis-ci.org/tildaslash/RatticWeb.png?branch=master)](https://travis-ci.org/tildaslash/RatticWeb)

RatticWeb is the website part of the Rattic password management solution, which allows you to easily manage your users and passwords.

To quickly get an RatticDB demo running do the following:
* Install VirtualBox from https://www.virtualbox.org/
* Install Vagrant from http://www.vagrantup.com/
* Install Ansible from http://ansible.cc/ (we need 1.4+)
* Check out this repo
* Run ```vagrant up``` in the root of this repo
* Wait for vagrant to deploy the machine
* Browse to https://localhost:8443/
* Login with Username: admin Password: rattic
* ...
* Profit!

If you decide to use RatticWeb you should take the following into account:
* The webpage should be served over HTTPS only, apart from a redirect from normal HTTP.
* The filesystem in which the database is stored should be protected with encryption.
* The access logs should be protected.
* The machine which serves RatticWeb should be protected from access.
* Tools like <a href=="http://www.ossec.net/">OSSEC</a> are your friend.

Requirements:
* <a href="https://pypi.python.org/pypi/pip">pip</a> (don't need, but useful)
* <a href="http://pypi.python.org/pypi/Django/1.4.3">Django 1.4.3</a>
* <a href="http://south.readthedocs.org/en/0.7.6/">Django South</a>
* <a href="http://tastypieapi.org/">Django Tastypie 0.9.12</a>
* <a href="https://www.dlitz.net/software/pycrypto/">PyCrypto</a>
* <a href="https://pypi.python.org/pypi/Markdown">Python Markdown</a>
* <a href="https://pypi.python.org/pypi/selenium">Python Selenium</a>

Support and Known Issues:
* Through <a href="http://twitter.com/RatticDB">twitter</a> or <a href="https://github.com/tildaslash/RatticWeb/issues?state=open">Github Issues</a>
* Apache config needs to have "WSGIPassAuthorization On" for the API keys to work  

Dev Setup: <https://github.com/tildaslash/RatticWeb/wiki/Development>

If you want to edit the help files:
* Clone the wiki files from ```git@github.com:tildaslash/RatticWeb.wiki.git```
* Add a file called ```ratticweb/local_settings.py``` that sets the ```HELP_SYSTEM_FILES``` variable to the location of the checked out wiki.

