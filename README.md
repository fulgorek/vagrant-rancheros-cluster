# RancherOS Cluster with Vagrant

Run a local RancherOS cluster on using Vagrant/VirtualBox.

## Getting started
1.) Install dependencies

* Virtualbox (Tested with 5.0.2)
* Vagrant (Tested with 1.8.1)

2.) Clone this project

```
git clone git@github.com:fulgorek/vagrant-rancheros-cluster.git
cd vagrant-rancheros-cluster
```

3.) Up and Running

```
vagrant up
```

```
vagrant ssh rancher-01
vagrant ssh rancher-02
vagrant ssh rancher-03
```


### Customizing and configuring


To get a feel for how RancherOS works under the hood checkout the
[RancherOS Repo](https://github.com/rancherio/os) for details.

# License
Copyright (c) 2015 [Alejandro Torres](https://github.com/fulgorek)
Copyright (c) 2014-2016 [Rancher Labs, Inc.](http://rancher.com)

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

[http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

