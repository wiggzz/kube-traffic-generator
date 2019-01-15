# Kube Traffic Generator

This project will create a mock kubernetes service along with a deployment and pods, and also create some artificial traffic in terms of calls to that service as well as scaling of the deployment (so that some kubernetes events will be generated).

## Installation

Ensure you have appropriate RBAC permissions to be able to create `RoleBindings` and `ClusterRoles`. On GKE:
    
    kubectl create clusterrolebinding cluster-admin-binding --clusterrole cluster-admin --user YOUR_EMAIL

see https://cloud.google.com/kubernetes-engine/docs/how-to/role-based-access-control for more information.

Then, in the right kubernetes context, apply the `resources.yaml` file in this repository.

    kubectl apply -f resources.yaml

# Removal

To remove the traffic generator, delete it using kubectl

    kubectl delete -f resources.yaml

