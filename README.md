# jfrog-pipelines-jpd-helm
Sample of JFrog Pipeline to deploy an instance of the JFrog Platform using Helm charts

**Work in progress**

---

### How to setup the pipeline

1. Fork this git repo 

1. Create a Helm remote repository acme-helm-jfrog-remote for https://charts.jfrog.io in Artifactory

1. Create an integration for the git repository
     gitIntegration: acme_co_github

1. Create an integration for the artifactory server containing the helm repo
     artifactoryIntegration: acme_co_artifactory

1. Create a Kubernetes integration for the targeted Kubernetes cluster
     kubernetesIntegration: acme_co_aks

1. Create a PEM integration with the JFrog license in it 
      licenseIntegration: acme_co_license


# Had to update helm client to 3.6.3 for local helm pull tests
# https://www.jfrog.com/jira/browse/RTFACT-26063

# https://www.jfrog.com/confluence/display/JFROG/Helm+Charts+for+Advanced+Users