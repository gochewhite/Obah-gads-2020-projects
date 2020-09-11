#lab: Getting Started with GKE

##Objective :
1. Provision a Kubernetes cluster using Kubernetes Engine.

2. Deploy and manage Docker containers using kubectl.

##stepsA Confirm that needed APIs are enabled
1.Sign in to the Google Cloud Platform (GCP) Console
2.In the GCP Console, on the Navigation menu (Navigation menu), click APIs & Services.
3.Make sure this APIs are enabled
 .Kubernetes Engine API
 .Container Registry API
 4.If either API is missing, click Enable APIs and Services at the top.

##StepB: Start a Kubernetes Engine cluster
1.In GCP console, on the top right toolbar, click the Open Cloud Shell button.

2.input your zone ```
export MY_ZONE=us-central1-a

```
3.Start a Kubernetes cluster managed by Kubernetes Engine. Name the cluster webfrontend and configure it to run 2 nodes: ```
      gcloud container clusters create webfrontend --zone $MY_ZONE --num-nodes 2

```

4. After the cluster is created, check your installed version of Kubernetes:```
      kubectl version
```
##Stepc : Run and deploy a container
1.From your Cloud Shell prompt, launch a single instance of the nginx container. (Nginx is a popular web server.): ```
    kubectl create deploy nginx --image=nginx:1.17.10
```
2.View the pod running the nginx container:```
      kubectl get pods
```
3.Expose the nginx container to the Internet:```
    kubectl expose deployment nginx --port 80 --type LoadBalancer      
```
4.View the new service: ```
   kubectl get services
```
5. Scale up the number of pods running on your service:```
      kubectl scale deployment nginx --replicas 3
```
6.Confirm that Kubernetes has updated the number of pods:```
    kubectl get pods
```
7..Congratulations!
you configured a Kubernetes cluster in Kubernetes Engine. You populated the cluster with several pods containing an application, exposed the application, and scaled the application..
