# Python Dash Application 

# Introduction 
Create Python Dash app and deploy it on Azure Web App Service through Docker.

Dash is an open-source framework for building data visualization interfaces to build interactive dashboards quickly. 
Dash helps data scientists to build analytical web applications without requiring advanced web development knowledge. 

# Getting Started
- Create interactive Dashboard project with Plotly Dash framework
- Create Docker image locally through the docker file provided in repo, e.g. dashapp1
> docker build -t dashapp1 .
> docker run -it --rm -p 3000:3000 dashapp1

- Create Azure Container Registry resource in Azure Portal and login from command prompt or Azure CLI locally
> docker login 'your azure container registry URL' OR
> az acr login --name 'your azure container registry URL'

- Once Login succeeded tag image and push into Azure Container Registry
> docker tag dashapp1 'your azure container registry URL'/dashapp1:0.0.1
> docker push 'your azure container registry URL'/dashapp1:0.0.1

- Create Web App service resource and select Azure Docker Registry as a source and your pushed image 

# Reference
https://learn.microsoft.com/en-us/training/modules/deploy-run-container-app-service/

![image](https://user-images.githubusercontent.com/94110694/220659739-ed40425c-4f26-4d2b-923f-053751cb5315.png)




