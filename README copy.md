# deploy-to-eks-using-github-actions
1. Create an EKS Cluster using this command:

eksctl create cluster --name primuslearning --region us-east-2 --nodegroup-name linux-nodes --node-type t2.micro --nodes 2

2. Then create .github folder and then create workflow folder inside .github folder 
3. create file with .yml extension and write the workflow code
4. Create a github repository and config AWS CREDENTIALS 
(credentials name should be the same with the one inside github-actions-ci.yml)
5. Create secrets in github repo created
        Go to settings of repo created
        click on secrets and variables-->actions-->new repo secret --> add secret ID and key.
6. Create new github repo and copy ssh then clone it
6. Test application by getting the dns name and going to a web browser
(go to aws console, search for elastic load balancer->Description then copy the DNS NAME) or copy the dns name doing : kubectl get services 

kubectl get pods ----> to see the pod that run

Clean up: Run: eksctl delete cluster --name primuslearning
