# eks-terraform
manual steps for creating eks cluster:
1) login to aws Iam and create role aws service and use case is Eks ....eks cluster next next name and then create cluster
2) search roles select own created role ,,permission attach policy ec2  ,vpc,route53 full access  and then 
3)now we have to create the eks cluster search eks enter
4)name ,version ,select the role we have created ,tags next
5)chose vpc and subnet (priva public )securty group /chose endpoint public+private ,networking components,next...next create
6) Now we have create new role for nodes
7) go to iam create role trusted entity aws services use case ec2 next
8) policy amazonec2container-registry-readonlypolicy  and node-amazoneks worker-nodepolicy  and aws -eks cni-policy next name next create role
9) GO to eks dashboard compute /node group /create nodegroup /name /select role we create /then select instance type t3medium ,
10) scaling capactiy 222 subnet and then (optionalkey pair) next create
11) Now go to terminal local
12) cd ~/.aws/
13) ls
14) rm config and otherfile
15) aws configure
16) aws eks update-kubeconfig --region us-east-1 --name test-cluster2
17)kubectl get nodes
