# Clean Up the stuff 
```
root@master:~ # systemctl stop kubelet.service
root@master:~ # docker kill $(docker ps -qa )
root@master:~ # docker rm $(docker ps -qa )
root@master:~ # rm -rf /etc/kubernetes/* /var/lib/etcd /var/lib/kubelet/*
root@master:~ # 
```


# Pull Image on Master  

```
root@master:~/docker-kubernetes-sf-11-Feb-2022/02-K8s/00-Setup# docker images | wc -l
12
root@master:~/docker-kubernetes-sf-11-Feb-2022/02-K8s/00-Setup#
```
```
root@master: # 
REPOSITORY                           TAG                 IMAGE ID            CREATED             SIZE
calico/kube-controllers              v3.22.0             df76d42861ee        2 weeks ago         132 MB
calico/cni                           v3.22.0             f86797de8afd        2 weeks ago         236 MB
calico/pod2daemon-flexvol            v3.22.0             59daef946c8c        2 weeks ago         21.4 MB
calico/node                          v3.22.0             f109b1742d34        2 weeks ago         213 MB
k8s.gcr.io/kube-apiserver            v1.21.9             dd4e1ec4649e        3 weeks ago         126 MB
k8s.gcr.io/kube-controller-manager   v1.21.9             296f8f79dfa8        3 weeks ago         120 MB
k8s.gcr.io/kube-scheduler            v1.21.9             174d7ea3958f        3 weeks ago         50.9 MB
k8s.gcr.io/kube-proxy                v1.21.9             b8f2a40e7bd1        3 weeks ago         104 MB
k8s.gcr.io/pause                     3.4.1               0f8457a4c2ec        13 months ago       683 kB
k8s.gcr.io/coredns/coredns           v1.8.0              296a6d5035e2        16 months ago       42.5 MB
k8s.gcr.io/etcd                      3.4.13-0            0369cf4303ff        17 months ago       253 MB
root@master: #
```

# Pull Image on Worker 
```
root@worker2:~# docker images | wc -l
6
root@worker2:~#
```

```
root@worker2:~# 
REPOSITORY                  TAG                 IMAGE ID            CREATED             SIZE
calico/cni                  v3.22.0             f86797de8afd        2 weeks ago         236 MB
calico/pod2daemon-flexvol   v3.22.0             59daef946c8c        2 weeks ago         21.4 MB
calico/node                 v3.22.0             f109b1742d34        2 weeks ago         213 MB
k8s.gcr.io/kube-proxy       v1.21.9             b8f2a40e7bd1        3 weeks ago         104 MB
k8s.gcr.io/pause            3.4.1               0f8457a4c2ec        13 months ago       683 kB
root@worker2:~#
```




# Now Re-Run the Scripts on Master Node: 
```
root@master:~/docker-kubernetes-sf-11-Feb-2022/02-K8s/00-Setup# sh install-k8s-master-node.sh
``` 

