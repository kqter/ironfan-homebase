# firewall chef cookbook

Installs/Configures firewall

## Overview

Defines custom iptable rules when the original cookbook doesn't define iptables
rules or there is no cookbook (for example, ssh).

## Attributes

* `[:firewall][:port_scan]`           -  (default: "{ :window => 5, :max_conns => 20, :port => 22 }")
  The recipe 'firewall::port_scan' will search for all properties named 'node[:firewall][:port_scan_*]'. This will create a rule that allows only ':max_conns' connections with a window period of ':window' seconds. For example, the settings above state that a maximum of 20 connections  can be made to the ssh port (22) within a period of 5 seconds. If any more than that are made within 5 seconds, the source will automatically be dropped.

## Recipes 

* `default`                  - Base configuration for firewall
* `port_scan`                - Port Scan


## Integration

Supports platforms: debian and ubuntu

Cookbook dependencies:
* iptables


## License and Author

Author::                Mike Heffner (<mike@librato.com>)
Copyright::             2011, Mike Heffner

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

> readme generated by [cluster_chef](http://github.com/infochimps/cluster_chef)'s cookbook_munger
