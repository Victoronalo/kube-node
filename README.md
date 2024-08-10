# kube-node

Project: Working With Kubernete Nodes



-I started by creating two EC2 instances namely master and worker instance.



-I customized the instances with the required AMI (Linux 2)



-I used a t2 medium size



-I configured the required security groups



-Proceeded to ssh into the master instance.



-To install docker engine, I ran “yum install docker –y



-I proceeded to run “systemctl enable docker”



-To start docker I ran the command “systemctl start docker”



-To check the status I ran the command “systemctl status docker”



-To install the kubeadm, kubectl, I ran this command below to se SE Linux mode
             * cat <<EOF | sudo tee /etc/yum.repos.d/kubernetes.repo
[kubernetes]
name=Kubernetes
baseurl=https://pkgs.k8s.io/core:/stable:/v1.30/rpm/
enabled=1
gpgcheck=1
gpgkey=https://pkgs.k8s.io/core:/stable:/v1.30/rpm/repodata/repomd.xml.key
exclude=kubelet kubeadm kubectl cri-tools kubernetes-cni
EOF




-I then ran the command “sudo setenforce 0




-Proceeded to run this command  below to install
      * sudo sed -i 's/^SELINUX=enforcing$/SELINUX=permissive/' /etc/selinux/config




-I ran this command “sudo systemctl enable --now kubelet



-I ran the command “systemctl restart kubelete”



I learnt a lot in this project, though I encountered some difficulties but I was able to pull through.

