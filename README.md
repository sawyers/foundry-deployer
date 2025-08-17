# foundry-deployer
Deploy foundry service on AWS

## Plan

- Create Route53 domain in us-east-1
- Create ACM cert for the same
- Automate via github actions
- Deploy Foundry VTT with attached EBS volume
- Attach deploy to ALB and some form of scaling (auto scaling group or more likely Fargate)
- See service deployed
- Scale up and down to see that the service can be 'halted' to save $$
- See that on scale up the EBS volume is correctly attached to have persistant storage

## Goals

Deploying a pre-made service is a useful exercise. Other services that I'd like to deploy in the same manner include `rundeck`, `zabbix`, and `jenkins` since all these would relate to things I want to do at my normal job. 

I also want to dip into using actions as a build pipeline since we expect to move at least some workload over to actions while only the most complex or expensive jobs stay in the existing jenkins.

Starting with the lower bar of a less complicated and documented process, but it should end up being very similar across all of these since I think there is a vendor generated docker already.