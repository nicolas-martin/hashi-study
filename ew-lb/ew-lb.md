# How consul eliminates the need for east-west LB #

LB - A
   - B
   - C

LB does 4 things 
1 Discovery
1 Fault tolerance
1 Load Balancing
1 Access control

With modern microservices, it becauser difficult to scale the LB.

IP based vs Identity-based networking and security
Consul uses service names instead of IP which has the benefit of being more scalable and easy to operate


## Consul ##
1. Uses DNS for service discovery "a.service.consul"

1. Uses health check on the services it runs on and adds / remove then automatically.

1. Uses randomized access

1. Uses consul connect to do service to service access control
