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
* Create an __Autonomous Developer Cloud Service Instance__
* Create a __Project__ within your Autonomous Developer Cloud Service instance.
* Go to the code section on the lefthand side and click on __create a new repository__.
* insert copying instructions from before 

### Lab: 200
#### In this lab you will setup GIT with your IntelliJ IDE. 
* Download provided Java Web Application. <--- insert link
* Download [Git](https://git-scm.com/downloads)
* Open IntelliJ and open the __project folder__ that you just downloaded.
* Go to __IntelliJ preferences --> Version Control --> Git__
* You are now going to configure the path to the Git executable. Your Git executable path should be: 
```
/usr/local/bin/git
```
If this does not work, open up the terminal and type in:
```
which git
```
This should give you the path to your git executable. 
* Click on __apply__ 
* Go back to your project and click on __code__.
* Create a __new__ repository 
* Refresh the page and click the "http" button. Copy this link as we will need it to allows our IntelliJ IDE to commit, push, and pull changes to our code repo.
* Go back to IntelliJ IDE and click on __VCS --> Checkout from Version Control --> Git__
* Insert copied Git URL from DevCS and paste into IntelliJ. Click on test and then enter your credentails that you used to log into your cloud tenancy. 
* Clone the repo and open the project within IntelliJ. From there go into the index.jsp file and change the output.
* Save your changes
* Click on __VCS --> Git --> Push__
* __Commit__ and __push__ your changes. Once that is complete go back to your DevCS project, click 'project' on the left hand side and see that your changes have been committed. 
* If you don't have Java and Git installed please do so before going onto the next step.
 * [Java](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
 * [Git](https://git-scm.com/downloads)

### Lab: 300
This part of the lab will help you create your external Jenkins web server and connect it via webhooks with Autonomous Developer Cloud Service. 
* Download [Jenkins](https://jenkins.io/download/) 2.149
* Jenkins will then ask for the __administration password__. To get this password type in the terminal
```
sudo cat /Users/Shared/Jenkins/Home/secrets/initialAdminPassword
```
* Click "install suggested plugins". This process may take a few minutes to complete. Until this is done feel free to browse Oracle's Autonomous Developer Cloud Services to make yourself familiar with all the different offerings. 
* Setup admin information and continue. 
* Go to __configure --> Global Tool Configuration__, install the following plugins:
  * Unleash Maven Plugin
  * Notification Plugin
  * Build Authorization Token Root Plugin
* Configure Git, Java, and Maven settings: Go to __Manage Jenkins --> Global Tool Configuration__
 * For Git give any name you want and then set your path to your git.exe. To find this path go into terminal and type in
 ```
 which git
 ```
 * For Java give any name you want and then set the path of JAVA_HOME. To find this path go into terminal and type in
 ```
 which java
 ```
* Go to the Jenkins Dashboard page and click __create new jobs__ and or __new item__ to create a job. 
  * __Enter an item name__: AutoDevCS_JavaApp
  * __Job type__: Maven
  * Press __OK___
* In the __description__ field of the __general__ tab on the Configuration page, enter a desrciption of the job that you see fit.
* Click the __Source Code Management__ tab.
  * Select the __git__ options
  * Enter the Oracle Autonomous Developer Cloud Service Git repository URL.
  * In the __credentials__ section click __add-->Jenkins__ and provide your Oracle Autonomous Developer Cloud Service credentials. 
  * Click __Add__ when you are done. If you are receiving a red error please make sure you have entered your credentials correctly. The error message should disappear after Jenkins verifies your credentials. 
* Click the __Build__ tab.
  * Root POM: __HelloWorld/pom.xml__
  * Goals and options: __clean install__
* Click the __Post-build Actions__ tab
  * Click the __Add post-build action__ button and select the __Archive the artifacts__ options.
  * You will now see a __Files to archive__ field enter: __HelloWorld/*.war__
* Click __save__




  


