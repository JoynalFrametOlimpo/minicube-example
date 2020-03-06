Step for installation (Ubuntu Distro)

1.- Install and Setup kubectl

sudo apt-get update && sudo apt-get install -y apt-transport-https
curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
echo "deb https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee -a /etc/apt/sources.list.d/kubernetes.list
sudo apt-get update
sudo apt-get install -y kubectl


2.- Install VirtualBox or KMZ

3.- Install Minikube

curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64 \
  && chmod +x minikube

sudo mkdir -p /usr/local/bin/
sudo install minikube /usr/local/bin/

4.- Confirm Installation

# Select drive <driver_name> https://kubernetes.io/docs/setup/learning-environment/minikube/#specifying-the-vm-driver 
# For example with virtual box:->   minikube start --vm-driver=virtualbox 

minikube start --vm-driver=<driver_name>    

5.- Basics Commands

# Verificate status
minikube status

# Stop cluster
minikube stop


# Start cluster
minikube start

# If you have previously installed minikube, and run the following error
# before execute "minikube start" -> machine does not exist.
# you need to clear minikube's local state:
minikube delete


