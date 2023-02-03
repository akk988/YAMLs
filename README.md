# YAMLs
Create a Kubernetes cluster in Azure
az aks create \
    --resource-group myResourceGroup \
    --name myAKSCluster \
    --node-count 2 \
    --generate-ssh-keys \
    --attach-acr <acrName>
    
Connect to cluster using kubectl 
az aks get-credentials --resource-group myResourceGroup --name myAKSCluster
kubectl get nodes

Run applications in Azure Kubernetes Service
vi azure-vote-all-in-one-redis.yaml
copy paste the k8s_votingapp_allinone yaml file
Save and close the file. In vi, use :wq.

kubectl apply -f k8s_voringapp.yaml

kubectl get service azure-vote-front --watch

open a web browser to the external IP address of your service. 
    
