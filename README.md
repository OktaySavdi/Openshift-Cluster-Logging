## Openshift Cluster Logging

install yaml file
```ruby
oc create -f .
```
Confirm the installation.
```ruby
oc get csv -A
oc get csv -n openshift-logging
```
The Cluster Logging components and the Event Router will take a few minutes to deploy. Watch the components to validate everything deploys.
```ruby
watch oc get deployment,pod,pvc,svc,route -n openshift-logging
```
Log into the Kibana UI.

• Use oc to discover the route **oc get routes -n openshift-logging** or click **Monitoring** ->  **Logging** in the OpenShift web console.

• On the Authorize Access page click **Allow selected permissions.**
