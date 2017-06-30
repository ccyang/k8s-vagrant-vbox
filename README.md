

https://github.com/jeremievallee/kubernetes-vagrant-ansible
https://kubernetes.io/docs/getting-started-guides/kubeadm/

ansible-playbook /vagrant/playbook.yml -i /vagrant/inventory -e @/vagrant/vars.yml

```
export KUBECONFIG=$HOME/admin.conf

kubectl proxy --address 0.0.0.0 --accept-hosts '.*' &
```

cd /vagrant/data/addon to deploy addons

```
kubectl create -f kube-flannel-rbac.yml
kubectl create -f kube-flannel-vbox.yml
kubectl create -f https://git.io/kube-dashboard
kubectl create -f ./heapster/
```