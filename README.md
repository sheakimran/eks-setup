aws version
aws configure


curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"

$HOME/bin && cp ./kubectl $HOME/bin/kubectl && export PATH=$PATH:HOME/bin
kubectl version

curl --silent --location "https://github.com/eksctl-io/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp

sudo mv /tmp/eksctl /usr/local/bin


 eksctl version
 
 
eksctl create cluster   --name dev   --region us-east-1   --nodegroup-name standard-workers   --node-type t3.medium   --nodes 3   --nodes-min 2   --nodes-max 3   --managed

eksctl get cluster
aws eks update-kubeconfig --name dev --region us-east-1

eksctl delete cluster dev --region us-east-1
