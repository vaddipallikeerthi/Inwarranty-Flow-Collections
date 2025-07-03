# Postman API Automation Integration with Github Actions #
This repository is a demonstration for POC for integrating postman tests with github actions.The tests are written in postman and they are executed on the virtual machine with the help of newman and newman-reporter-htmlextra.
Github actions will trigger the project execution on every push on the main branch.Along with that this will be executed manually using workflow_dispatch and runs on the scheduled time with the help of the cron job.

The html reports are archived and kept in artifact section for the team to download it .Along with that they can view the report directly from the github page .
The latest report will be mailed to the team members using Gmail SMTP.

 ## Testing coverage ##
 This project validates the API with a broad testing strategy that includes:  
 
 1.Happy flow testing  
 2.Negative and Edge case testing  
 3.Token testing  
 4.Data driven testing with csv  
 5.Schema validations  
 6.Secrets management with Github Secrets  


## TECH STACK ##

1.Postman  
2.Nodejs 22v  
3.Newman  
4.Newman-Reporter-HTMLExtra  
5.Github Actions  
6.GMAIL SMTP  
7.Github Pages  
8.CSV for data driven testing  
9. AWS EC2 for self hosted runner  

## Project Structure ## 

```
In Warranty
├─ Inwarranty-flow Collection.postman_collection.json
├─ QA.postman_environment.json
└─ testdata.csv

``` 

## Git hub page ##
You can view the latest report in the github link: https://github.com/vaddipallikeerthi/Inwarranty-Flow-Collections/

## How to run the project ##
You can run the project on the local system for that :  
1.Clone the project on the local system : https://github.com/vaddipallikeerthi/Inwarranty-Flow-Collections.git  
2.Install node js and npm   
3.Install Newman using ```npm install -g newman```
4.Install Newman-reporter-htmlextra : ```npm install -g newman-reporter-htmlextra ``` 
5.Run the newman command : ```newman run 'Inwarranty-flow Collection.postman_collection.json' \
             -e QA.postman_environment.json \
             -d testdata.csv \
             -r cli,htmlextra \
             --reporter-htmlextra-export ./newman/index.html```

             
 ## HTML Report ##
 The report will be created in the newman folder  
 ![Postman Report](https://github.com/vaddipallikeerthi/Inwarranty-Flow-Collections/blob/static-content/Report.png)


 



