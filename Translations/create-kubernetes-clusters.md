# Creating Kubernetes Clusters with GKE using CLI
In order to create clusters using the Google Cloud Shell, follow the following steps;

1. Sign in into your Google Cloud Platform Account.

2. In GCP console, on the top right toolbar, click the Open Cloud Shell button and click the Activate Cloud Shell button
![](images/cloudshell.png)
1. Click continue
![](images/continue.png)
A terminal will be loaded and you will be able to type in different commands to perform differednt tasks using the CLI.
We need to set up a region and a zone where our your cluster will be created

1. Set a zone
Type
```BASH
gcloud config set compute/zone your-zone
```
Replace 'your-zone' with the exact zone where you want to create your virtual machine forexample 'us-west1-a', do not include quotes.

## Creating a GKE cluster
* Type the following command in the shell

```BASH
gcloud container clusters create 'cluster-name' --num-nodes=1
```
**NOTE**
Replace 'cluster-name' with the name of the cluster, dont include quotes
on --num-nodes=1, you can replace 1 with the number of nodes that you want to create.

* After creating your cluster, you need to get authentication credentials to interact with the cluster

Use the following command
```BASH
gcloud container clusters get-credentials 'cluster-name'
```

To test if your cluster is initialized, run:
```BASH
kubectl get node
```

Exit the Shell
```BASH
exit
```