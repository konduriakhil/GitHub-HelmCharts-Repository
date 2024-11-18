Helm Charts GitHub Pages
-------------------------
## Package the Helm Chart
```sh
helm package <chart-directory>
```
![alt text](images/helm1.png)
![alt text](images/helm2.png)
## copy the .tgz file to GitHub pages repository 
![alt text](images/helm3.png)
##  Generate the Helm Repository Index
* Use helm repo index to generate an index.yaml file. This file contains metadata for your Helm repository.
```sh
helm repo index . --url https://konduriakhil.github.io/GitHub-HelmCharts-Repository
```
![alt text](images/helm9.png)
![alt text](images/helm10.png)
## Change the Git Hub repository to GitHub Pages for the accomodation of the Helm charts
![alt text](images/helm4.png)
![alt text](images/helm5.png)
![alt text](images/helm6.png)
  ### Change the Branch to main
  ![alt text](images/helm7.png)

## Push these changes to the GitHub Pages repository
```sh
git add .
git commit -m "push the secrets to GitHub Pages"
git push
```
![alt text](images/helm8.png)
![alt text](images/helm11.png)
## Adding the repository of charts to Other machine to use charts
![alt text](images/helm12.png)
```sh
# Adding the repository
helm repo add myrepo https://konduriakhil.github.io/GitHub-HelmCharts-Repository

# Update the repository
helm repo update myrepo

# List the repositories
helm repo list

# To search available charts in a repository
helm search repo myrepo
```
## Deploy the helm chart
```sh
# helm install <release-name> myrepo/<chart-name>
helm install app1 myrepo/secrets
```
![alt text](images/helm13.png)
![alt text](images/helm14.png)