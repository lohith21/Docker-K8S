``` 
   1  ls
    2  kubectl get nodes 
    3  kubectl get nodes --show-labels
    4  ls
    5  vim helloworld-nodeselector.yaml
    6  ls
    7  kubectl get deploy 
    8  kubectl create -f helloworld-nodeselector.yaml 
    9  kubectl get pods 
   10  kubectl describe pod helloworld-deployment-57986b947d-7p2nx
   11  kubectl get nodes
   12  kubectl label nodes worker2 hardware=virtual
   13  kubectl get nodes --show-labels
   14  kubectl get pods 
   15  kubectl get pods -o wide 
   16  kubectl label nodes worker1 hardware=virtual
   17  kubectl get pods -o wide 
   18  kubectl get nodes --show-labels
   19  kubectl get pods -o wide 
   20  kubectl scale --replicas=6 deploy helloworld-deployment
   21* kubectl get po
   22  ls
   23  kubectl scale --replicas=3 deploy helloworld-deployment
   24  ls
   25  vim helloworld-nodeselector-multi.yaml 
   26  kubectl create -f helloworld-nodeselector-multi.yaml 
   27  kubectl get pods 
   28  kubectl describe pod helloworld-deployment-2-7fd7bbcd7-86jfs
   29  kubectl label nodes worker1 env=prod
   30  kubectl get pods 
   31  kubectl get pods -o wide 
   32  kubectl get nodes --show-labels
   33  kubectl get pods -o wide 
   34  kubectl label nodes worker1 env-
   35  kubectl label nodes worker1 hardware-
   36  kubectl get nodes --show-labels
   37  kubectl get pods -o wide 
   38  kubectl label nodes worker1 hardware=virtual
   39  kubectl get nodes --show-labels
   40  kubectl label nodes worker2 hardware-
   41  kubectl get nodes --show-labels
   42  kubectl get pods -o wide 
   43  kubectl scale --replicas=5 deploy helloworld-deployment
   44  kubectl get pods -o wide 
   45  ls
   46  kubectl label nodes worker1 hardware-
   47  kubectl label nodes worker1 env-
   48  kubectl label nodes worker2 env-
   49  kubectl get pods

``` 
