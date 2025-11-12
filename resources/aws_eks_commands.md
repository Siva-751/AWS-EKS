
aws eks --region ap-southeast-1 describe-cluster --name pc-eks --query cluster.status

aws eks --region 	ap-southeast-1 update-kubeconfig --name pc-eks 

inside ec2 machine kubecl machine
-----------------------------------
curl -O https://s3.us-west-2.amazonaws.com/amazon-eks/1.32.9/2025-09-19/bin/linux/amd64/kubectl.sha256

sha256sum -c kubectl.sha256

OR

openssl sha1 -sha256 kubectl

chmod +x ./kubectl

mkdir -p $HOME/bin && cp ./kubectl $HOME/bin/kubectl && export PATH=$HOME/bin:$PATH

kubectl version --short --client

