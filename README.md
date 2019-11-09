# CAT_helm
We’re creating a Helm 3.0 deployment and expect an alpha to be available November 6th.

The Helm chart source is here:
https://github.com/heliumplusdatastage/CAT_helm.git

These are the commands to run it on GKE.

Prerequisites: 
1) Install helm3.
2) Clone the repo.

Step-1: Appstore postgres DB requires a persistent disk with a name (appsstore-db-volume). Use the command to create a persistent disk,
“gcloud compute disks create appstore-db-volume --size 5Gi --zone <Cluster zone>”

Step-2: Deploy chart using the command below,
“helm install <Name> ./CAT_helm”

Here are kubectl commands showing its status after it’s installed.

Use the command below to get the list of pods,
“kubectl get pods”

Use the command below to get the list of services,
“kubectl get svc”

Use the command below to get a detailed description of the pod,
“kubectl describe pods <name of the pod>”
