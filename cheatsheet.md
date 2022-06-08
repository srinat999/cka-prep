kubectl cheatsheet
https://kubernetes.io/docs/reference/kubectl/cheatsheet/

Start a deployment and get the YAML out
kubectl run nginx --image=nginx --dry-run=client -o yaml > pod.yaml

Scaling replicas
kubectl scale --replicas=3 rs/foo  

Executing a command inside a pod
k exec nginxx01-977cc6949-49kxh -- bash -c "date"

For secrets, if you want to include key value pairs, use the keyword stringData instead of Data

Run a command as a particular user:
Use SecurityContext in the pod description

Alias for kubectl
alias k='kubectl'

Exposing a deployment as a service
k expose deployment nginx --port=8080 --type=LoadBalancer