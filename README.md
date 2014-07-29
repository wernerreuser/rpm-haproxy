rpm-haproxy
===========

An RPM spec file to build and install the is HAProxy TCP/HTTP reverse proxy.

To Build:

    sudo yum -y install rpmdevtools && rpmdev-setuptree
    sudo yum -y install pcre-devel gcc make openssl-devel
    wget https://raw.github.com/wernerreuser/rpm-haproxy/master/haproxy.spec -O ~/rpmbuild/SPECS/haproxy.spec
    wget http://haproxy.1wt.eu/download/1.5/src/devel/haproxy-1.5-3.tar.gz -O ~/rpmbuild/SOURCES/haproxy-1.5-3.tar.gz
    rpmbuild -bb  ~/rpmbuild/SPECS/haproxy.spec
