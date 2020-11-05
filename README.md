# Nokia SR OS Protobufs
 
## Overview
 
The Nokia SR OS protobufs are for configuration and management of SR OS based routers.
 
Protobufs are provided for the following platforms:
 
- 7250 Interconnect Router (IXR)
- 7450 Ethernet Service Switch (ESS)
- 7750 Service Router (SR)
- 7950 Extensible Routing System (XRS)
- Virtualized Service Router (VSR)
 
## Working with the repository
 
The repository is created in order to provide a flexible programmatic interface to assist with network automation tasks.
 
### `master` branch
 
The `master` branch provides the protobufs for all releases per platform.  Cloning this branch will provide the maximum output, however, it may be more extensive then required for your use case.
 
```
git clone https://github.com/nokia/7x50_protobufs
```
 
### Per-release branches
 
Each release is provided as a separate branch.  The platforms use a set of common protobufs and these are represented as sros_major.minor, for example `sros_19.10`.  Each release is tagged with the full release revision as well, for example `sros_19.10.r1`
 
To obtain the protobufs for a specific release clone the following:
 
```
git clone -b sros_19.10.r1 --depth 1 https://github.com/nokia/7x50_protobufs
```
 
#### Obtaining the differences between releases
 
To compare between two different sets of protobufs using git, clone the `master` branch or a release specific branch such as `sros_19.10` and then execute the following:
 
```
git diff sros_19.10.r1 sros_19.10.r2
```
 
#### Obtaining a TAR file of the protobufs for a specific release
 
To obtain a compressed TAR file of the available protobufs for a specific release, clone the repository and then execute the following:
 
```
git archive --format tar.gz sros_19.10.r1 > nokia_protobufs.10.r1.tar.gz
```
 
## Documentation
 
Further documentation for Nokia SR OS protobufs can be found on the [Nokia Support Portal](https://customer.nokia.com/support/s/) and in the SR OS user and reference guides on the [Nokia Doc Center](https://documentation.nokia.com/).

For more information on developing automation for Nokia's IP and optical products, visit the [Network Developer Portal](https://network.developer.nokia.com/).
