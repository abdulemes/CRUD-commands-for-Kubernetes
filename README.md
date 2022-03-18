# CRUD-commands-for-Kubernetes

## Intro to Kubernetes Minikube

To get familiar with Kubernetes, we first of all try hands on minikube which provides a testing environment by creating one control plane and one worker node.

First step is to install minikube from brew on mac or chocolatey on windows machine. 

![IMG_9401](https://user-images.githubusercontent.com/93732510/158900830-93ff5f47-40d1-4f5b-a8b4-b9b4a772623b.jpg)

Next is to start minikube on a VM. if a vm is not already installed on the local machine, we can include it the minikube command.

![IMG_9402](https://user-images.githubusercontent.com/93732510/158901876-cc517711-af43-4375-bc20-d04f1931e3be.jpg)

we are going to use kubectl to communicate with the cluster which has already been installed as a dependency for minikube. So now that minikube has started the vm, we run kubectl command to check it can communicate with the cluster.

![IMG_9404](https://user-images.githubusercontent.com/93732510/158902387-36e4ad27-caae-4b6d-82ad-f526ef8ff1e7.jpg)

Next is to check the status of the cluster to ensure all the components are live and running. 

![IMG_9405](https://user-images.githubusercontent.com/93732510/158902744-755967eb-01fa-4e28-9627-d620590a60aa.jpg)

Now we can create an image for the container.

![IMG_9406](https://user-images.githubusercontent.com/93732510/158903883-f9c1aae8-cfe2-4c25-98bb-9ca58e5ed977.jpg)

This should have created a pod via deployment which we can check too confirm.

![IMG_9407 2](https://user-images.githubusercontent.com/93732510/158981310-b889a957-f98a-4e4d-901d-9d7dc121e061.jpg)

we can edit an image in a pod via deployment because its a minikube cluster, and the image will get replaced with a new one to reflect the change. 

![IMG_9408](https://user-images.githubusercontent.com/93732510/158981927-55b119c9-2a28-4621-8d4f-cac7ea1e45d5.jpg)

we can create another image but this time a backend service like mongodb.

![IMG_9408](https://user-images.githubusercontent.com/93732510/158985025-7bbb92cc-0237-415b-9546-2ac0e69feb7a.jpg)

Another command we can explore is the describe command which gives information about a pod.

![IMG_9410](https://user-images.githubusercontent.com/93732510/158985775-a0821f7c-b2e8-4896-886f-5381628b74e1.jpg)

Also we can use replicaset command to replicate a pod. 

![IMG_9412](https://user-images.githubusercontent.com/93732510/158988448-706341fb-0bb1-4365-82ab-7977e90c248c.jpg)

To get the logs in time of troubleshooting, we can use the logs command.

![IMG_9413](https://user-images.githubusercontent.com/93732510/159025481-f940281d-2282-49af-9e1d-0593a8d76be9.jpg)

Gaining control of the container can be done through exec command.

![IMG_9415](https://user-images.githubusercontent.com/93732510/159025736-7f9ac15b-af33-4e94-885d-848a301c4e49.jpg)

At this point we can do a clean up of the environment by deleting the deployment. 

![IMG_9416](https://user-images.githubusercontent.com/93732510/159026146-e7a7f035-8d37-4971-b4b6-d41f7d2eae6d.jpg)







