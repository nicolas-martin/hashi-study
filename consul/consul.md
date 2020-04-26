# Consul #

In a monolith the sub-system calls are called in memory. When a bug is discovered in one of them, we need to redeploy the monolith a unit.

With microservices, we can now deploy at whatever cadence we want. 

The challenges:
- *Discovery*: Before you could mark the function as public and call it in memory. But now you have to put a LB in front of the new service and hardcode the IP. There is now a LB for each services. It also introduces a single point of failure. Manually managed

** The Solution ** : Consul has a central registry and using the service name and DNS we can now get the services.

- *Configuration*: Giant file for all the subsystem. But in a distributed world every service has their own configs. 

** Solution ** : We can now capture all the config in that central consul service.


- *Segmentation*: In a monolith it was easy to invoke internal functions. But now with services, we need to handle NS and EW access.

** Solution ** : Consul connect. Service graph. Creating rules via service name instead of IP (with firewall). Which makes it scale independent. Consul handles identity with TLS. Mutual proxy. Mutual TLS. 

Consul creates a service mesh
