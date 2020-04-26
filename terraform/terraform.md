# Terraform #

Infrastructure management. 

Works by looking at your configuration file, doing a refresh to get a view how things in the real world is then plan is made to figure out the difference between real world and the plan. 
And then finally an apply phase which executes the plan.

Can be extended to different providers 
_Iaas_
- AWS
- Azure,
- GCP
- Openstack
- Vmware

_Pass_
- Heroku
- k8s
- lambda

_Saas_
- DataDog
- Fastly
- Github


## How to manage TF? ##
Similar problems to software development? When team grow larger, can now define modules. That can be published to a registry (private or public)
