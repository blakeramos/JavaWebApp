# Integrating Oracle DevCS with external Jenkins Server and IntelliJ IDE
## What is Jenkins and why is it important?
* Jenkins is a server that allows for continuous integration and continuous development. A few features include regular deployment, daily backups, weekly cleanups, vulnerability scans, workflow environment, and the list goes on. 
* Easy installation
* Hundreds of plugins that allows Jenkins to integrate with practically every tool in the CI/CD delivery toolchain. 
* Distributed: Ability to work across multiple machines helping to drive test/deployment across multiple platforms faster. 
* [Companies that use Jenkins](https://wiki.jenkins.io/pages/viewpage.action?pageId=58001258)

## What is IntelliJ IDEA?
* Java IDE that is designed to maximize developer productivity. 
* Built-in tools and supported frameworks.
* [Companies that use IntelliJ](https://www.jetbrains.com/company/customers/)


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
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/cloud.oracle.png)
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-29%20at%202.37.06%20PM.png)
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-29%20at%202.38.55%20PM.png)
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-29%20at%202.39.12%20PM.png)

* Create an __Autonomous Developer Cloud Service Instance__
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-29%20at%202.39.28%20PM.png)
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-29%20at%202.47.16%20PM.png)
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-29%20at%202.49.03%20PM.png)
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-29%20at%202.49.40%20PM.png)

* Click on the instance's hamburger menu and then click on __Access Service Instance__
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-29%20at%202.58.09%20PM.png)

* Create a __Project__ within your Autonomous Developer Cloud Service instance.
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-29%20at%202.58.52%20PM.png)
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-29%20at%203.00.08%20PM.png)
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-29%20at%203.00.20%20PM.png)
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-29%20at%203.00.34%20PM.png)

* Go to the code section on the lefthand side and click on __create a new repository__.
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-29%20at%203.26.38%20PM.png)

* __Name__: CodeRepo
* Click __Import existing repository__
* __Import existing repo__: https://github.com/blakeramos/JavaWebApp
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-29%20at%203.34.58%20PM.png)


### Lab: 200
#### In this lab you will setup GIT with your IntelliJ IDE. 
* Download [Git](https://git-scm.com/downloads)
* Download [IntelliJ](https://www.jetbrains.com/idea/download/#section=mac)
* Go to __IntelliJ preferences --> Version Control --> Git__
 ![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-29%20at%203.24.57%20PM.png)
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-29%20at%203.25.11%20PM.png)

* You are now going to configure the path to the Git executable. Your Git executable path should be: 
```
/usr/local/bin/git
```
If this does not work, open up the terminal and type in:
```
which git
```
This should give you the path to your git executable. 
* Click on __OK__ 
* Go back to your project on __Autonomous Developer Cloud Service__ and click on __code__.
* Click the "http" button. Copy this link as we will need it to allows our IntelliJ IDE to commit, push, and pull changes to our code repo.
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-29%20at%203.35.38%20PM.png)

* Go back to __IntelliJ IDE__ and click on __VCS --> Checkout from Version Control --> Git__
* Insert copied Git URL from Autonomous DevCS and paste into IntelliJ. Click on test and then enter your credentails that you used to log into your cloud tenancy. 
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-29%20at%203.30.04%20PM.png)
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-29%20at%203.30.31%20PM.png)

* Clone the repo and open the project within IntelliJ. From there go into the index.jsp file and change the output.
* Save your changes
* Click on __VCS --> Git --> Push__
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-30%20at%208.53.53%20AM.png)

* __Commit__ and __push__ your changes. Once that is complete go back to your Autonomous DevCS project, click 'project' on the left hand side and see that your changes have been committed. 
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-30%20at%208.56.22%20AM.png)
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-30%20at%208.56.35%20AM.png)

* __NOTE__: Go back to your Autonomous Developer Cloud Service project, go to the sidebar to confirm you are in project. You should see that your changes from IntelliJ have been recognized. You should also be able to see the changes in the 'code' section. 

### Lab: 300
This part of the lab will help you create your external Jenkins web server and connect it via webhooks with Autonomous Developer Cloud Service. 
* Download [Jenkins](https://jenkins.io/download/) 2.149
* Jenkins will then ask for the __administration password__. To get this password type in the terminal
```
sudo cat /Users/Shared/Jenkins/Home/secrets/initialAdminPassword
```
* Copy the password in terminal and past is in the __Administration Password__ field. 
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-30%20at%202.56.05%20PM.png)
* Click "install suggested plugins". This process may take a few minutes to complete. Until this is done feel free to browse Oracle's Autonomous Developer Cloud Services to make yourself familiar with all the different offerings. 
* Setup admin information and continue. 
* Go to __configure --> Global Tool Configuration__, install the following plugins:
  * Unleash Maven Plugin
  * Notification Plugin
  * Build Authorization Token Root Plugin
  ![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-30%20at%202.44.36%20PM.png)
  ![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-30%20at%202.44.54%20PM.png)
  ![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-30%20at%202.45.10%20PM.png)
  * __Note__: Be sure to restart your server after installing the plugins. 
  
* Configure Git, Java, and Maven settings: Go to __Manage Jenkins --> Global Tool Configuration__
 * For Git give any name you want and then set your path to your git.exe. To find this path go into terminal and type in
 ```
 which git
 ```
 * For Java give any name you want and then set the path of JAVA_HOME. To find this path go into terminal and type in
 ```
 /usr/libexec/java_home
 ```
 * For Maven, choose install automatically. 
 ![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-30%20at%202.43.58%20PM.png)
 ![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-30%20at%202.44.12%20PM.png)
 
* Go to the Jenkins Dashboard page and click __create new jobs__ and or __new item__ to create a job. 
  * __Enter an item name__: AutoDevCS_JavaApp
  * __Job type__: Maven
  * Press __OK___
  ![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-31%20at%201.56.43%20PM.png) Ignore red text in the picture above ^^^.
  
* In the __description__ field of the __general__ tab on the Configuration page, enter a desrciption of the job that you see fit.
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-31%20at%202.00.04%20PM.png)

* Click the __Source Code Management__ tab.
  * Select the __git__ options
  * Enter the __Oracle Autonomous Developer Cloud Service Git repository URL__.
  * In the __credentials__ section click __add-->Jenkins__ and provide your Oracle Autonomous Developer Cloud Service credentials. 
  * Click __Add__ when you are done. If you are receiving a red error please make sure you have entered your credentials correctly. The error message should disappear after Jenkins verifies your credentials. 
  * __Note__: Make sure that you select the credentials you have just created. 
  ![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-30%20at%202.46.18%20PM.png)
  
* Click the __Build__ tab.
  * Root POM: __HelloWorld/pom.xml__
  * Goals and options: __clean install__
  ![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-30%20at%202.46.40%20PM.png)
  
* Click the __Post-build Actions__ tab
  * Click the __Add post-build action__ button and select the __Archive the artifacts__ options.
  * You will now see a __Files to archive__ field enter: __HelloWorld/*.war__
  ![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-30%20at%202.46.40%20PM.png)
  
* Click the __Build Triggers__ tab
  * Select the __Trigger builds remotely__ check box
  * In the __Authentication token__ field enter: __my_auth_token__
* Click __save__

![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-30%20at%202.46.25%20PM.png)

* Go to your terminal and type the command:
```
ssh -R 80:localhost:8080 ssh.localhost.run
```
This will allow your external Jenkins server to connect to the internet. You can now log into your Jenkins server using the new url provided. 

![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-31%20at%208.50.11%20AM.png)

* __Note__: If you aren't seeing your changes in your Autonomous DevCS project you might need to restart you server because of a broken pipe. Just re-type in the terminal command in the above picture and it should start to work again. 

### Lab: 400
This part of the lab will help you create and configure the webhooks that will allow our external Jenkins server and Oracle Autonomous Developer Cloud project to communicate. __Congrats! You are almost done!!!!!__
* In Oracle Autonomous Developer Cloud Service interface, open the project, and click __Administration --> Webhooks__ in the side bar.
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-31%20at%2010.31.26%20AM.png)

  * Click __+ New Webhook__
    * __Type__: Select __Hudson/Jenkins - Build trigger__
    * __Name__: Enter __JenkinsBuildWebhook__ 
    * __Build Server Url__: Your jenkins URL: (eg: http://username.localhost.run)
    * __Job name__: __AutoDevCS_JavaApp__
    * __Build Server Security__: Select __Build Token Root Plugin__, the build will be triggered only if the Build Authorization Token Root plugin is installed on the Jenkins server. 
    * __Remote Build Token__: my_auth_token, the same token name that was specified in the Jenkins job.
    * __Repository__: The repository you made in Oracle Autonomous Developer Cloud Service. 
    * Click __Done__
    ![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-31%20at%2010.42.08%20AM.png)
    
  * Select the webhook you just created and click __Test__
  If the configuration is correct you will see a green check mark. If it is not there will be a red x and you will need to go into the logs to debug. Once you see the green check mark, your webhook is ready to send a notification to the Jenkins server to run a build when any update is pushed to the specified Git repo.
  
  * In the webhooks page, click __+ New Webhook__
    * __Type__: Select __Jenkins - Notification Plugin__
    * __Name__: Enter __JenkinsGetNotification__ 
    * __Base Url__: Your jenkins URL: (eg: http://username.localhost.run)
    * Check the box that says __Ongoing Builds__ 
    * Click __Done__
    The webhook is now able to get notification from the Jenkins server when the build runs and is complete.
    ![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-31%20at%2010.42.16%20AM.png)

* Copy the __JenkinsGetNotification__ webhook __URL__ (if you look at the picture above. That URL with the "HTTP" box beside it is the one you need to copy.)
  * Now go back to your __Jenkins server__. Open the __configure__ page for your job.
  * Click on the __Job Notifications__ tab
  * Select __Add Endpoint__
    * In the __URL__ field paste the JenkinsGetNotification webhook URL that you copied earlier. 
    * You __DO NOT__ have to change any other fields.
  * Select __Save__
  ![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-31%20at%2010.42.31%20AM.png)
  
Now your Autonomous Developer Cloud Service and Jenkins server are ready to send and recieve notifications. 
* Go to your Autonomous Developer Cloud Service, on the side bar select __Code__
  * Go into the directory and change the output in __Index.jsp__
  * To do so, there is a pencil icon that allows you to update your code within Autonomous Developer Cloud Service. 
  * Click __Commit__ (Enter a commit message)
  ![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-31%20at%2010.48.52%20AM.png)
  
* Go to the side bar and click project.
  * You should see a notification that you have pushed your code to the master.

* Go to your Jenkins server
  * On the main page you should see a build happening under __Build Executor Status__. The initial build may take some time to complete. If the build does not succeed you can select your Job and the specific build. In the build there is a log that you can read to debug if necessary. 

When the build is running, if you go back to your Autonomous Developer Cloud Service project.
* Go to __Projects__
* You should see that a __Tracked Build__ is running. 
  * Once the build succeeds you will see a __Build Success Notification__
  
When the build is complete, if you go back to your Autonomous Developer Cloud Service project.
* Go to __Projects__
* You should see that a __Tracked Build__ has ended with the status: __Success__. 

Oracle Autonomous Developer Cloud Service Project notifications
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-31%20at%2010.54.31%20AM.png)
Jenkins Server View (when building):
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-31%20at%2010.53.55%20AM.png)

With a successful build, go back to the Jenkins server.
* In the __Build__ page of your __Job__.
* You can now download the __build artifact__ and __deploy__ it to your server or on Oracle Java Cloud Service.
![alt text](https://github.com/blakeramos/JavaWebApp/blob/master/a1screeenshots/Screen%20Shot%202018-10-31%20at%2010.54.10%20AM.png)
# What next???!!?!?!
* [Deploying a Java EE application to a Java Cloud Service Instance](https://www.oracle.com/webfolder/technetwork/tutorials/obe/cloud/javaservice/JCS/eclipse_jcs/eclipse_jcs.html)
* [Deploying a Jenkins server on OCI](https://blogs.oracle.com/cloud-infrastructure/deploy-jenkins-on-oracle-cloud-infrastructure) 
