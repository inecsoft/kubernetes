kind             version

Pod               v1
Service           v1
ReplicaSet        apps/v1
Deployment        apps/v1

kubectl create -f pod-definition.yml
kubectl get pods

kubectl replace -f replicaset-definition.yml
kubectl replace --replicas=6 replicaset-definition.yml
kubectl replace --replace=6 replaceset myapp-replaceset

kubectl create namespace dev
kubectl get pods --namespace=dev
kubectl config set-context $(kubectl config current-context) --namespace=dev

kubectl create -f compute-quota.yaml