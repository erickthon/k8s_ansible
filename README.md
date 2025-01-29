k8s-cluster/
│── inventory.ini  # Define Raspberry Pi nodes
│── playbook.yml   # Main Ansible playbook
│── roles/
│   ├── common/    # Common setup (updates, dependencies, cgroups)
│   │   ├── tasks/main.yml
│   │   ├── handlers/main.yml
│   │   ├── defaults/main.yml
│   ├── containerd/  # Install and configure containerd
│   │   ├── tasks/main.yml
│   │   ├── handlers/main.yml
│   │   ├── defaults/main.yml
│   ├── master/    # Initialize Kubernetes master node
│   │   ├── tasks/main.yml
│   │   ├── handlers/main.yml
│   │   ├── defaults/main.yml
│   ├── worker/    # Join worker nodes to the cluster
│   │   ├── tasks/main.yml
│   │   ├── handlers/main.yml
│   │   ├── defaults/main.yml
│   ├── network/   # Install CNI plugin (Flannel/Calico)
│   │   ├── tasks/main.yml
│   │   ├── handlers/main.yml
│   │   ├── defaults/main.yml
│   ├── extras/    # Optional: Install MetalLB, Ingress, monitoring
│   │   ├── tasks/main.yml
│   │   ├── handlers/main.yml
│   │   ├── defaults/main.yml
