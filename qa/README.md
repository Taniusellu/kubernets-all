Create cluster for Qa Env


create hosted zone novqaterraform.com (Route 53)

aws s3 mb s3://novqaterraform.com  (terminal)

aws s3 ls (check)

1.cd qa/

kops create cluster --name=novqaterraform.com --node-size="t2.micro" --master-size="t2.micro" --master-zones="eu-west-1a,eu-west-1b,eu-west-1c" --networking="weave" --topology="private" --bastion="true" --dns="private" --zones="eu-west-1a,eu-west-1b,eu-west-1c" --state="s3://novqaterraform.com" --out=. --target=terraform

2.backend.tf

3.terraform init

4.terraform plan

5.terraform apply


Destroy cluster

terraform destroy 
