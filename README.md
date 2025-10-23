2048 Game on AWS EKS with Fargate & ALB:
Deployed the 2048 game using Amazon EKS, Fargate, and AWS Load Balancer Controller to achieve a fully serverless, scalable, and production-ready Kubernetes setup.

Tech Stack:
AWS EKS – Managed Kubernetes
AWS Fargate – Serverless compute
AWS ALB Controller – Traffic management
Helm, eksctl, kubectl – Cluster automation

Quick Setup
eksctl create cluster --name demo-cluster --region us-east-1 --fargate
kubectl apply -f https://tinyurl.com/aws-2048-yaml
helm install aws-load-balancer-controller eks/aws-load-balancer-controller \
  -n kube-system --set clusterName=demo-cluster --set region=us-east-1 \
  --set vpcId=<your-vpc-id>
Access the ALB DNS URL in your browser to play 

Highlights
Serverless Kubernetes with Fargate
Secure IAM & OIDC integration
ALB-managed scalable ingress
Hands-on cloud-native deployment experience

Chaithanya M
Deployed on AWS | July 2025
