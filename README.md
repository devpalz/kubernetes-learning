```shell script

# List all nodes
kubectl get pods

# List all nodes with extra info
kubectl get pods -o wide

# Describe a pod called webapp, you can see the events of the pod
kubectl describe pod <pod-name>

# Delete a pod 
kubectl delete pod <pod-name>

# Dry run the creation of a pod, so you can get hold of the yml definition
kubectl run <pod-name> --image=redis123 --dry-run=client -o yaml > pod2.yaml

# You can extract the definition of a running pod
kubectl get pod <pod-name> -o yaml > pod-definition.yaml

# You can directly edit a running pod
kubctl edit pod <pod-name>

# You can get hold of the replication controller 
kubectl get replicationcontroller

# If you have edited the yml on disc, you can run the following to update it
kubectl replace -f replicaset-definition.yml

# Get everything
kubectl get all

```