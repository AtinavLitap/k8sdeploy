This repo is used to deploy code into a K8s cluster.  ArgoCD is installed in the same K8s cluster and is used for continuous deployment (CD)

Continuous integration is achieved using Jenkins.  The Jenkinsfile in the k8scode repo uses the Dockerfile in the k8scode repo to build a docker image and push it to docker hub.  The same Jenkinsfile also updates the image in the deployment.yaml in the current repo.

ArgoCD detects the change in the docker image in the repo and reconciles the deployment in the K8s cluster to match that in the k8sdeploy repo.


