# Helm-Chart-Installation

Install Docker
$  sudo apt update && apt -y install docker.io

 Install kubectl
$  curl -LO www.storage.googleapis.com/kubernetes-release/release/$(curl
 -s www.storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl
 &&   chmod +x ./kubectl && sudo mv ./kubectl /usr/local/bin/kubectl

 Install Minikube
$  curl -Lo minikube www.storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
 && chmod +x minikube && sudo mv minikube /usr/local/bin/

 Start Minikube
$  apt install conntrack
$  minikube start --vm-driver=none
$  minikube status

To download helm
curl -fsSL -o get_helm.sh www.raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3
chmod 700 get_helm.sh
./get_helm.sh

To verify the installation use the following command
which helm


Let’s create Our First Helm Chart


helm repo add stable https://charts.helm.sh/stable



helm install testchart2 stable/tomcat --set service.type=NodePort

to uninstall helm
which helm ( to see which folder its installed )
rm -rf /usr/local/bin/helm
kubectl get all
