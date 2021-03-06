Packaging Instructions
======================

Install the required package building packages.

    sudo yum install rpmbuild golang

Setup a standard RPM build workspace with the required folders.

    mkdir rpmbuild
    mkdir rpmbuild/{BUILD,RPMS,SOURCES,SPECS,SRPMS}

Run the following commands to download the required source archive, the RPM spec
file and build the package.

    cd SOURCES
    wget https://github.com/driskell/log-courier/archive/vVERSION.zip
    cd SPECS
    wget https://raw.githubusercontent.com/driskell/log-courier/vVERSION/contrib/rpm/log-courier.spec
    rpmbuild -ba log-courier.spec

Building a Source RPM
=====================

Follow the instructions for a binary package using the following rpmbuild
parameters instead.

    rpmbuild -bs --sign log-courier.spec
