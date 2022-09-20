## As we have build the jenkin server and reactjs server in previous doc and build image from docker for reactjs app in application server. Now we have to     build image from jenkin only and push the image in docker with below steps:

#### Step-1: First create the New Item in jenkins with the name and choose pipeline.

![image](https://user-images.githubusercontent.com/42695637/190360001-6b883a79-d160-4cc3-9618-18c2a3f69c18.png)


#### Step-2: Give the same configuration as like previous but now we need to mention the repository URL for github which is for docker build image

```https://github.com/mayankkh1/docker.git```
     
#### Step-3: Put the jenkins file which is present in current repository upload in your code.

#### Step-4: Put the docker and nginx file which is present in current repository upload in your code.


#### Step-5: After that create webhook URL in github with below url:
  
```http://JenkinServerIP:8080/github-webhook/```
     
 
#### Step-6: After that install plugin in Jenkin related to docker:
  
```CloudBees Docker Build and Publish plugin```
```Docker Pipeline```
```Docker plugin```
```docker-build-step```
    
#### Step-7: Enter the credential for dockerhub in managecredentials as like ubuntu user.
             
```Manage Jenkins ==> Manage Credentials ==> jenkins ==> Global credentials (unrestricted) ==> Add Credentials ==> Put the details and create```

#### Step-8: Now add the ubuntu user or SSH user which is used for authentication in docker group with below command:
  
```usermod -aG docker ubuntu```
     
#### Step-9:  Now try to run the build manually first if it's working fine then try manually to upload in dockerhub

#### Step-10: Afer that we need to modify jenkin file according to existing jenkin file in directory for CI and CD. 
    
     
     
     

     
