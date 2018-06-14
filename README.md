
**Note:** This is a **read-only mirror** of the formal [Gerrit](https://gerrit.hyperledger.org/r/#/admin/projects/fabric) repository,
where active development is ongoing. Issue tracking is handled in [Jira](https://jira.hyperledger.org/secure/Dashboard.jspa?selectPageId=10104)

## Status

This project is an _Active_ Hyperledger project. For more information on the history of this project see the [Fabric wiki page](https://wiki.hyperledger.org/projects/Fabric). Information on what _Active_ entails can be found in
the [Hyperledger Project Lifecycle document](https://wiki.hyperledger.org/community/project-lifecycle).

[![Build Status](https://jenkins.hyperledger.org/buildStatus/icon?job=fabric-merge-x86_64)](https://jenkins.hyperledger.org/view/fabric/job/fabric-merge-x86_64/)
[![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/955/badge)](https://bestpractices.coreinfrastructure.org/projects/955)
[![Go Report Card](https://goreportcard.com/badge/github.com/hyperledger/fabric)](https://goreportcard.com/report/github.com/hyperledger/fabric)
[![GoDoc](https://godoc.org/github.com/hyperledger/fabric?status.svg)](https://godoc.org/github.com/hyperledger/fabric)
[![Documentation Status](https://readthedocs.org/projects/hyperledger-fabric/badge/?version=latest)](http://hyperledger-fabric.readthedocs.io/en/latest/?badge=latest)

## Hyperledger Fabric

Hyperledger Fabric is a platform for distributed ledger solutions, underpinned
by a modular architecture delivering high degrees of confidentiality,
resiliency, flexibility and scalability. It is designed to support pluggable
implementations of different components, and accommodate the complexity and
intricacies that exist across the economic ecosystem.

Hyperledger Fabric delivers a uniquely elastic and extensible architecture,
distinguishing it from alternative blockchain solutions. Planning for the
future of enterprise blockchain requires building on top of a fully-vetted,
open source architecture; Hyperledger Fabric is your starting point.
## Quick Start of e2e-cli on centos7

1. docker
```
curl -sSL https://get.daocloud.io/docker | sh
docker -v
```

2. docker-compose
```
sudo yum -y install epel-release
sudo yum -y install python-pip
sudo yum clean all
curl -L https://get.daocloud.io/docker/compose/releases/download/1.9.0/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
docker-compose -v
```

3. git
```
sudo yum install curl-devel expat-devel gettext-devel openssl-devel zlib-devel gcc perl-ExtUtils-MakeMaker
wget https://github.com/git/git/archive/v2.3.0.zip
unzip v2.3.0.zip
cd git-2.3.0
make prefix=/usr/local/git all
sudo make prefix=/usr/local/git install
sudo vim /etc/profile
  export PATH=/usr/local/git/bin:$PATH
source /etc/profile
git version
```

4. golang
```
wget https://storage.googleapis.com/golang/go1.8.3.linux-amd64.tar.gz
sudo tar -C /usr/local -xzf go1.8.3.linux-amd64.tar.gz
sudo vim /etc/profile
  export PATH=$PATH:/usr/local/go/bin
  export GOPATH=/opt/gopath
source /etc/profile
go version
```

5. fabric sourse code
```
git clone https://github.com/hyperledger/fabric.git
cd fabric
```

6. fabric binary & images
```
cd fabric/scripts
bootstrap.sh 1.1.0 -s
(very slow as Great Firewall,try another way to download)
```

6. run e2e_cli
```
cd fabric/examples/e2e_cli
network_setup.sh up
(release binary to the right dir)
```

## Releases

- [v1.1.0-alpha - January 25, 2018](https://github.com/hyperledger/fabric/releases/tag/v1.1.0-alpha)
- [v1.0.5 - December 6, 2017](https://github.com/hyperledger/fabric/releases/tag/v1.0.5)
- [v1.1.0-preview - November 1, 2017](https://github.com/hyperledger/fabric/releases/tag/v1.1.0-preview)
- [v1.0.4 - October 31, 2017](https://github.com/hyperledger/fabric/releases/tag/v1.0.4)
- [v1.0.3 - October 3, 2017](https://github.com/hyperledger/fabric/releases/tag/v1.0.3)
- [v1.0.2 - September 10, 2017](https://github.com/hyperledger/fabric/releases/tag/v1.0.2)
- [v1.0.1 - August 10, 2017](https://github.com/hyperledger/fabric/releases/tag/v1.0.1)
- [v1.0.0 - July 11, 2017](https://github.com/hyperledger/fabric/releases/tag/v1.0.0)
- [v1.0.0-rc1 - June 23, 2017](https://github.com/hyperledger/fabric/releases/tag/v1.0.0-rc1)
- [v1.0.0-beta - June 8, 2017](https://github.com/hyperledger/fabric/releases/tag/v1.0.0-beta)
- [v1.0.0-alpha2 - May 14, 2017](https://github.com/hyperledger/fabric/releases/tag/v1.0.0-alpha2)
- [v1.0.0-alpha - March 16, 2017](https://github.com/hyperledger/fabric/releases/tag/v1.0.0-alpha)
- [v0.6.1-preview - October 15, 2016](https://github.com/hyperledger/fabric/releases/tag/v0.6.0-preview)
- [v0.6.0-preview - September 16, 2016](https://github.com/hyperledger/fabric/releases/tag/v0.6.0-preview)

## Release Roadmap

Please visit the [Hyperledger Fabric wiki](https://wiki.hyperledger.org/projects/fabric/roadmap) for our release roadmap. We plan on a quarterly release cadence following the v1.1.0 release, delivering on a scoped set of themes and select features. Unless specified otherwise, all releases will be upgradable from the prior minor release.

## Documentation, Getting Started and Developer Guides

Please visit our
online documentation for
information on getting started using and developing with the fabric, SDK and chaincode:
- [v1.1](http://hyperledger-fabric.readthedocs.io/en/release-1.1/)
- [v1.0](http://hyperledger-fabric.readthedocs.io/en/release-1.0/)
- [master branch (development)](http://hyperledger-fabric.readthedocs.io/en/master/)

It's recommended for first-time users to begin by going through the Getting Started section of the documentation in order to gain familiarity with the Hyperledger Fabric components and the basic transaction flow.

## Contributing

We welcome contributions to the Hyperledger Fabric project in many forms.
There’s always plenty to do! Check [the documentation on how to contribute to this project](http://hyperledger-fabric.readthedocs.io/en/latest/CONTRIBUTING.html)
for the full details.

## Community

[Hyperledger Community](https://www.hyperledger.org/community)

[Hyperledger mailing lists and archives](http://lists.hyperledger.org/)

[Hyperledger Chat](http://chat.hyperledger.org/channel/fabric)

[Hyperledger Fabric Issue Tracking (JIRA)](https://jira.hyperledger.org/secure/Dashboard.jspa?selectPageId=10104)

[Hyperledger Fabric Wiki](https://wiki.hyperledger.org/projects/Fabric)

[Hyperledger Wiki](https://wiki.hyperledger.org/)

[Hyperledger Code of Conduct](https://wiki.hyperledger.org/community/hyperledger-project-code-of-conduct)

[Community Calendar](https://wiki.hyperledger.org/community/calendar-public-meetings)

## License <a name="license"></a>

Hyperledger Project source code files are made available under the Apache License, Version 2.0 (Apache-2.0), located in the [LICENSE](LICENSE) file. Hyperledger Project documentation files are made available under the Creative Commons Attribution 4.0 International License (CC-BY-4.0), available at http://creativecommons.org/licenses/by/4.0/.
