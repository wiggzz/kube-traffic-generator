# Kube Traffic Generator

This project will create a mock kubernetes service (petclinic) along with a deployment and pods. And also pod (traffic-generator) which creates some artificial traffic by calling 3 petclinic endpoints every second. Additionally after 100 seconds the deployment is scaled up to 4 or scaled down to 2.

## Installation

Ensure you have appropriate RBAC permissions to be able to create `RoleBindings` and `ClusterRoles`. On GKE see https://cloud.google.com/kubernetes-engine/docs/how-to/role-based-access-control for more information.

Then, in the right kubernetes context, apply the `resources.yaml` file in this repository.

    kubectl apply -f resources.yaml

# Removal

To remove the traffic generator, delete it using kubectl

    kubectl delete -f resources.yaml

