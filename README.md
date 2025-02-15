# The Basics of Google Cloud Compute: Challenge Lab 

Before this we have to set Zone and Region and Exports Variable. 

### list the active account 
`gcloud auth list`

### list the project ID
`gcloud config list project`


### Set the region and zone

`gcloud config set compute/zone yourZoneName`
`gcloud config set compute/region yourRegionName`

### create a variable for region,

`export REGION=yourRegion`

### create a variable for the zone

`export ZONE=yourZone`
## Task 1. Create a Cloud Storage bucket

Under Cloud Storage we can create cloud bucket using GUI


## Task 2. Create and attach a persistent disk to a Compute Engine instance

### create isntance from terminal
`gcloud compute instances create my-instance --machine-type e2-medium --zone=$ZONE`

### ceate a new disk named mydisk
`gcloud compute disks create mydisk --size=200GB \
--zone $ZONE
`
### Attaching a disk

`gcloud compute instances attach-disk gcelab --disk mydisk --zone $ZONE
`
Attach the persistent disk to the instance.

## Task 3. Install an NGINX web server

update server

```sudo apt-get update```

install NGINX

```sudo apt-get install -y nginx```

NGINX is running

```ps auwx | grep nginx```

