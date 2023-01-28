## Jenkins shared library example 

The code attached to this repository, is a groovy script that can be used as a Jenkins shared library. 

### Functions that this library can do

The following tasks can be performed using tis library:

- <b>dockerLogin:</b> Perform login process with docker private/public repository 
- <b>buildImage:</b> Perform build docker image process
- <b>buildJar:</b> Perform maven package process for Java application
- <b>dockerPush:</b> Start pushing newly build docker image to destination 

Start your kubernetes cluster by using minikube with the following command:

    minikube start

Clone this repository and install all components using by executing the following command in root directory of your repo:

    ./install.sh
    

To access your application, you need to create a tunnel in minikube to give services an external IP that requested one. You can do this by using the dollowing command:

    minikube tunnel

Check your frontend service for external IP. From that, you can access the application in the browser. To check service of frontend, use the following:

    kubectl get svc/frontend

Uninstall all components using the following

    ./uninstall

### Run on your machine with Helmfile

Clone this repository and install all components using by executing the following command in root directory of your repo:

    helmfile sync
    
To access your application, you need to create a tunnel in minikube to give services an external IP that requested one. You can do this by using the dollowing command:

    minikube tunnel

Check your frontend service for external IP. From that, you can access the application in the browser. To check service of frontend, use the following:

    kubectl get svc/frontend

Uninstall all components using the following

    helmfile destroy

### Cleanup

Stop your minikube cluster with the following:

    minikube stop
    
You can also destroy your minikube image and free up some space with:

    minikube delete
