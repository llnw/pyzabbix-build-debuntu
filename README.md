LLNW pyzabbix packaging for Debian/Ubuntu
=========================================

* Upstream:  https://github.com/lukecyca/pyzabbix
* PyPi:  https://pypi.python.org/pypi/pyzabbix

Building the package:
---------------------

* Fetch the [current version]
* Extract the source tree into the repo root:

    `tar xvzf pyzabbix-0.6.tar.gz --strip-components=1`
* `dpkg-buildpackage -us -uc`

Package maintenance:
--------------------

* `dch` - add a changelog entry and match the version to the new dist version

Ubuntu PPA:
-----------
* PPA: https://launchpad.net/~llnw/+archive/pyzabbix

To perform a release, you need a launchpad.net account with an authorized GPG key.

* Alter collectd/debian/changelog for the release (i.e. append ~ubuntu12.04 to the version string, change release from unstable to precise)
* `dpkg-buildpackage -S` - Create a source package for this Ubuntu version
* `dput ppa:llnw/pyzabbix pyzabbix_0.6-llnw1~ubuntu12.04_source.changes` - upload to launchpad.net build cluster


  [current version]: https://pypi.python.org/packages/source/p/pyzabbix/pyzabbix-0.6.tar.gz

