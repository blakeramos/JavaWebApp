# Integrating Oracle DevCS with external Jenkins Server and IntelliJ IDE

## Getting Started
What you will need:
* Oracle Cloud Trial Account
* IntelliJ IDE
* Jenkins

### Lab: 100
This part of the lab will help you get started with an Oracle cloud trial acccount:
* Click on this URL [Oracle Cloud Trial Account](https://myservices.us.oraclecloud.com/mycloud/signup?language=en&sourceType=:ex:tb:::RC_PDMK171128P00097:DevOps_HOL&SC=:ex:tb:::RC_PDMK171128P00097:DevOps_HOL&pcode=PDMK171128P00097), and complete all the required steps to get your free Oracle Cloud Trial Account.
* You must wait to receive your account before continuing to the "Create an Autonomous Developer Cloud Service instance" section:

#### Create an Autonomous Developer Cloud Service instance:
* Go to [Oracle Cloud Service](https://cloud.oracle.com/home) homepage.
* Insert photos
* Create Autonomous Developer Cloud Service Instance
* Create Project within your Autonomous Developer Cloud Service instance.

### Lab: 200
#### In this lab you will setup GIT with your IntelliJ IDE. 
* Download provided Java Web Application. <--- insert link
* Download [Git](https://git-scm.com/downloads)
* Open IntelliJ and open the project folder that you just downloaded.
* Go to IntelliJ preferences --> Version Control --> Git
* You are now going to configure the path to the Git executable. Your Git executable path should be: 
```
/usr/local/bin/git
```
If this does not work, open up the terminal and type in:
```
which git
````
This should give you the path to your git executable. 
* Click on apply 

* Go back to your project and click on code.
* Create a new repository 
* Refresh the page and click the "http" button. Copy this link as we will need it to allows our IntelliJ IDE to commit, push, and pull changes to our code repo.
* Go back to IntelliJ IDE and click on VCS --> Checkout from Version Control --> Git
* Insert copied Git URL from DevCS and paste into IntelliJ. Click on test and then enter your credentails that you used to log into your cloud tenancy. 
* Clone the repo and open the project within IntelliJ. From there go into the index.jsp file and change the output.
* Save your changes
* Click on VCS --> Git --> Push
* Commit and push your changes. Once that is complete go back to your DevCS project, click 'project' on the left hand side and see that your changes have been committed. 








  


