Deploying Consul with Argo CD

High-level Steps:
1. Create a Kubernetes Cluster
2. Deploy ArgoCD (execute the "install_argo_cd.sh" script)
3. Deploying Consul Servers
    * Create a new git repo
    * Define Consul Helm chart values - Create a Consul config file
    * Define Consul configuration entries
    * Create an Argo CD project for Consul and apply the project to K8S cluster
        - $ kubectl apply -f consul-project.yaml 
Warning: metadata.finalizers: "resources-finalizer.argocd.argoproj.io": prefer a domain-qualified finalizer name to avoid accidental conflicts with other finalizer writers
appproject.argoproj.io/consul created

    * Deploy Consul with Argo CD
        - Create Argo CD Application file (consul-application.yaml)
        - $ kubectl apply -f consul-application.yaml
        


