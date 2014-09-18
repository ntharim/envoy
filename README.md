# envoy

Auto service discovery and linking for Docker

Adapted from [binocarlos/arpanet](https://github.com/binocarlos/arpanet)

`envoy` is a thin wrapper for:

 * [consul](https://github.com/hashicorp/consul) - service discovery and K/V store
 * [cadvisor](https://github.com/google/cadvisor) -  container metrics
 * [ambassadord](https://github.com/progrium/ambassadord) - auto tcp forwards
 * [registrator](https://github.com/progrium/registrator) - auto service registering