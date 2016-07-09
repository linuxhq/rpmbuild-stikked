# rpmbuild-stikked

Create a Stikked RPM for RHEL/CentOS.

## Requirements

To download package sources and install build dependencies

    yum -y install rpmdevtools yum-utils

## Build process

To build the package follow the steps outlined below

    git clone https://github.com/linuxhq/rpmbuild-stikked.git rpmbuild
    mkdir rpmbuild/SOURCES
    spectool -g -R rpmbuild/SPECS/Stikked.spec
    yum-builddep rpmbuild/SPECS/Stikked.spec
    rpmbuild -ba rpmbuild/SPECS/Stikked.spec

## License

BSD

## Author Information

This package was created by [Taylor Kimball](http://www.linuxhq.org).
