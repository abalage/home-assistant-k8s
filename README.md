# home-assistant-k8s
Home Assistant deployment manifests for Kubernetes

You can either use the plain YML files, or use [Kustomize](https://kustomize.io/).

An example of overwriting FQDN can be found in ˙overlay/kustomize.yml`

Deployment is tested on K3s-v1.24.8+k3s1.

## Usage

1. Create a namespace for Home assistant:  
   ```kubectl create ns home-assistant```

2. Build the deployment by using kubectl's built-in kustomize feature:  
   ```kubectl apply -k overlay -n home-assistant```
