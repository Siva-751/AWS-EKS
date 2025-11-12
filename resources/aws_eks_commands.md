
aws eks --region ap-southeast-1 describe-cluster --name pc-eks --query cluster.status

aws eks --region 	ap-southeast-1 update-kubeconfig --name pc-eks 
