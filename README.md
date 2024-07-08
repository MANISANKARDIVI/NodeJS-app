# NodeJs-local-deployment

# 1. Create a namespace

Apply the given NodeJs namespace.yaml file

    kubectl apply -f namespace.yaml

# 2.  create ConfigMap 

Apply the given configmap.yaml file

    kubectl apply -f configmap.yaml

# 3. Create Deployment for NodeJs

> Apply the given NodeJs deployment.yaml file

    kubectl apply -f deployment.yaml

# 4.  Create service for NodeJs

    kubectl apply -f service.yaml

# 5. Create HorizontalPodAutoScaller for NodeJs

    kubectl apply -f hpa.yaml

# 6. Create Ingress for NodeJs

    kubectl apply -f ingress.yaml

