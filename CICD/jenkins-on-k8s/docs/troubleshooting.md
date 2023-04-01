# Troubleshooting
## GKE Loadbalancer issue
Error syncing load balancer: failed to ensure load balancer: failed to create forwarding rule for load balancer (aa040c2ab1d264d19ac00757ad25035b(default/cd-jenkins)): googleapi: Error 412: Constraint constraints/compute.restrictLoadBalancerCreationForTypes violated for projects/luiz-devops-jenkins. Forwarding Rule projects/luiz-devops-jenkins/regions/us-east1/forwardingRules/aa040c2ab1d264d19ac00757ad25035b of type EXTERNAL_NETWORK_TCP_UDP is not allowed., conditionNotMet

## Root cause
This is caused because the Organization Policy to enforce Disable Global Load
Balancer creation for the entire organization is enabled.

## Solution
Specify the project and apply the enforcement

  ```shell
  gcloud resource-manager org-policies set-policy jenkins/orgpolicy.json \
    --project $GOOGLE_CLOUD_PROJECT 
  ```

## References
https://cloud.google.com/load-balancing/docs/org-policy-constraints

