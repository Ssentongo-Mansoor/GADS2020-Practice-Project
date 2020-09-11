# Create a virtual machine using the gcloud command line
Inorder for you to create a Virtual Machine on google cloud Platform using the Google Cloud Shell, follow the following steps;

1. Sign in into your Google Cloud Platform Account.

2. In GCP console, on the top right toolbar, click the Open Cloud Shell button
![](images/cloudshell.png)
<br/>
3. Click continue <br/>
![](images/continue.png)
A terminal will be loaded and you will be able to type in different commands to perform differednt tasks using the CLI.
<br/>
We need to set up a region and a zone where our Virtual Machine will be created

4. Set a zone
Type
```BASH
gcloud config set compute/zone your-zone
```
Replace 'your-zone' with the exact zone where you want to create your virtual machine forexample 'us-central1-a', do not include quotes.

5. Create a Virtual machine with the following commands

```BASH
gcloud compute instances create "my-vm" --machine-type "machine-type" --image-project "image-family" --image "image" --subnet "default"

```
Replace 
* "my-vm" with the name of your instance forexample "vm-1"
* "machine-type" with the type of machine that you want forexample "n1-standard-1"
* "image-family" with the image family that you are creating forexample "debian-cloud"
* "image" with the name of the boot disk image to deploy on the VM forexample "debian-9-stretch-v20190213"

6. Create the VM. 
Tap enter on the keyboard and your Virtual Machine will be created

7. View the Virtual Machine
```BASH
gcloud compute instances list
```
8. Exit the Terminal
```BASH
exit
```
