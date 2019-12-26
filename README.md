Pre-requiste :

Install vagrant 
Install RKE(Rancher Kubernetes Engine) https://rancher.com/docs/rke/latest/en/installation/#creating-the-cluster-configuration-file and follow all steps of OS requirement as well https://rancher.com/docs/rke/latest/en/os/ before running rke up command

Steps to deploy a k8s cluster:

1) Run command `vagrant up` to run VM in virtualbox.
2) Run command `rke config --name cluster.yml` on terminal.
3) In one VM set role option via terminal to be etcd, worker, controlplane. In IP provide th eIP of VM from Vagrantfile and then in ssh key path use the complete path of installation of .vagrant/machines/machine_name/virtualbox/private_key
4) For other 2 VM set role option via terminal to be worker. In IP provide th eIP of VM from Vagrantfile and then in ssh key path use the complete path of installation of .vagrant/machines/machine_name/virtualbox/private_key
5) Run `rke up`, if it fails first time try once again running `rke up`.
6) To remove cluster use `rke remove` command and to remove VM use `vagrant destroy`.
