## create kind cluster

kind delete cluster --name dev-cluster
kind create cluster --config config.yaml

## move the config file to an accessible location 

cp /root/.kube/config /workspaces/dev_environment/.kube/

## revise kubeconfig

 cat /root/.kube/config


## Ingress

kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/kind/deploy.yaml
