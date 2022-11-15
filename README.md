This repo is used to deploy code into a K8s cluster.  ArgoCD is installed in the same K8s cluster and is used for continuous deployment (CD)
Continuous integration is achieved using Jenkins and the application code, Jenkinsfile, and Dockerfile in the k8scode repo is used to build a docker image, and push it to docker hub.
