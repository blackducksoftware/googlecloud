# A sample two-tier template for GCP
This template deploys standard two-tier application protected by a VM-Series firewall. 

# Deployment steps
1. Install the gcloud SDK https://cloud.google.com/sdk/downloads

2. Edit the two-tier-template.py with your GCP deployment details
```
#Variables
zone = # Enter the desired ZONE for deployment
region = # Enter the desired Region for deployment 
sshkey = # Enter your PUBLIC ssh key and make sure you append it with your username. GCP requirement
bootstrap_bucket = # Enter a bucket name where you have stored the VM-Series bootstrap files.
serviceaccount = # GCP service account. Default one created by GCP should suffice
image = # FW image name for the VM-Series. Check the beta deployment guide

```
3. Save the file and deploy using the CLI
```
   $gcloud deployment-manager deployments create deployment1 --config two-tier-sample.yaml
```