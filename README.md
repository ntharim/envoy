# envoy

Auto service discovery and linking for Docker

Adapted from [binocarlos/arpanet](https://github.com/binocarlos/arpanet)

`envoy` is a thin wrapper for:

 * [consul](https://github.com/hashicorp/consul) - service discovery and K/V store
 * [cadvisor](https://github.com/google/cadvisor) -  container metrics
 * [ambassadord](https://github.com/progrium/ambassadord) - auto tcp forwards
 * [registrator](https://github.com/progrium/registrator) - auto service registering

## Quickstart

### Variables

```bash
$ export HOSTNAME=$(hostname)
$ export PRIVATE_IP=$(ifconfig eth0 | awk -F ' *|:' '/inet addr/{print $4}')
```

### Install

```bash
$ sudo sh -c 'curl -L https://raw.githubusercontent.com/ntran13/envoy/master/envoy > /usr/local/bin/envoy'
$ sudo chmod a+x /usr/local/bin/envoy
$ sudo -E envoy setup
$ envoy pull
```

### Usage - Single Host

```bash
$ envoy consul boot 1
$ envoy start
```

## Usage - Multiple Hosts

//TODO