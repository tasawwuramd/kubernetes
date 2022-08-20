# kubernetes

V5

- Docker is most popular container software
    - An alternative to Docker is rkt - which also works with kubernetes
- Docker Engine
    - Docker runtime
    - software to make run docker images
- Docker Hub
    - Docker repository

Benefits of Docker
    - isolation
    - closes parity between dev,QA and production environments
    - docker makes develpments teams able to ship faster
    - you can run same docker images , on laptops , data center VMs and cloud providers

V6
Kubernetes Setup
    - Starting with minikube to quickly spin up a local single machine with a kubernetes cluster
    - later will spin up a cluster on AWS using Kops
        - Kops is a tool used to run highly available production cluster

- using AWS free tier ( allows 750 hours of t2.micro's/month)
    - aws.amazon.com
- using on local machine
    - github.com/kubernetes/minikube
-using Digital Ocean

V7
Minikube
    - Too user to run K8s Locally
    - Minikube runs a single-node cluster of K8s inside a linux VM
    - Works with Windows, Linux, and Mac OS

V8
Starting Minikube
    - Download Minikube
        - Run "minikube start" 
            - to start minikube cluster
        - minikube version
            - to check version of minikube
In windows home edition hyper-v is not available so we can use virtual box to run minikube/kubernetes

    - Install kubectl to run kubernetes commands

To Check Kubernetes configuration
    - cat ~/.kube/config

To open minikube dashboard
    - minikube dashboad

Example:
    - Create Deployment
        - kubectl create deployment hello-minikube --image=k8s.gcr.io/echoserver:1.4
    - Exposing node port
        - kubectl expose deployment hello-minikube --type=NodePort --port=8000
    - Start minikube service
        - minikube service hello-minikube
    - Stop minikube
        - minikube stop
    - Clear all minikube and fresh start
        - minikube delete

V9 
 