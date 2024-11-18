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

```sh
helm package <chart-directory>
helm repo index ./charts --url https://<your-username>.github.io/<repository-name>
helm repo add myrepo https://konduriakhil.github.io/GitHub-HelmCharts-Repository

```