# NodeJs-Docker-local-deployment

we need to install Docker, Git clone the repo. 

    git clone https://github.com/MANISANKARDIVI/NodeJS-app.git

Create Docker-Image

    cd NodeJS-app
    docker build -t your-registry-name/nodeapp .

Push in to your Docker_registry

> 1.  If you want to Test the Image is working & create Container
 
    docker run -itd --name=nodeapp -p 3000:3000 your-registry-name/nodeapp

> 2. We can Access the WebUI on Port
 
    https://localhost:3000

> 3. First we need to login in docker-registry & Then push into Registry

    docker login
    Enter your UserName: ****
    Enter Your Passwd: ****
    docker push your-registry/nodeapp

# NodeJs-k8s-local-deployment

# 1. Create a namespace
Now we are Trying K8S deployment

    cd k8s-manifest

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

