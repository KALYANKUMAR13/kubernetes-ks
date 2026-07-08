
**General Architecture**
<img width="938" height="494" alt="image" src="https://github.com/user-attachments/assets/3abbff82-3038-4597-951e-f893f32a377e" />


**Tools to Create One:**
1. Console,
2. IaC
3. eksctl
4. eksdemo(advanced with karpenter knowledge)

   Needed things:
   above used to create cluster,
   AWS IAM Authenticator for k8s ->  This authenticates your user to EKS(your iam cred to call eks endpoint)
   https://docs.aws.amazon.com/eks/latest/userguide/auth-configmap.html




<img width="899" height="463" alt="image" src="https://github.com/user-attachments/assets/f22b213e-17df-4229-a6d5-06fa3878b4af" />

https://docs.aws.amazon.com/eks/latest/best-practices/subnets.html

The nodes connect to the EKS control plane through (a) an EKS public endpoint or (b) a Cross-Account elastic network interfaces (X-ENI) managed by EKS. When a cluster is created, you need to specify at least two VPC subnets. EKS places a X-ENI in each subnet specified during cluster create (also called cluster subnets). The Kubernetes API server uses these Cross-Account ENIs to communicate with nodes deployed on the customer-managed cluster VPC subnets.


**Authentication**
To have access to EKS Cluster.
1. OIDC
2. Auth Configmap (live inside cluster)
3. EKS Auth 
