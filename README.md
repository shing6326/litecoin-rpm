## Litecoin

The rpm source for litecoin daemon.
For more details of litecoin, please visit https://github.com/litecoin-project/litecoin

## Building the source rpm

Install rpmspectool to download the source files inside rpm spec
```bash
yum install rpmspectool
```

Install mock environment to build the rpm
https://github.com/rpm-software-management/mock/wiki

Copy the spec file from repository
```bash
cd ~
mkdir rpmbuild/SPECS
cp SPECS/litecoin.spec rpmbuild/SPECS/
```

Download the source file and build source rpm
```bash
spectool -g -R rpmbuild/SPECS/litecoin.spec
```

Build the source rpm using mock
```bash
mock --resultdir=$HOME --buildsrpm --spec rpmbuild/SPECS/litecoin.spec --sources rpmbuild/SOURCES -v
```

Compile
```bash
mock -v litecoin-0.16.3-1.el7.src.rpm
```
