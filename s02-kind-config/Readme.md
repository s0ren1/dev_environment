## create kind cluster

kind create cluster --config=config.yaml

## move the config file to an accessible location 

cp /root/.kube/config /workspaces/dev_environment/.kube/

## kubeconfig mapping

export KUBECONFIG=/workspaces/dev_environment/.kube/config