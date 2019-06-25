# VM-JavaServer
How to run Java Server on VM(ubuntu)

## Create Tomcat on VM

###### Install tomcat on VM

Can refer to the URL to implement
https://tecadmin.net/install-tomcat-9-on-ubuntu/

 Now you can test Have tomcat create?
 
 Enter apache-tomcat9/bin to start and enter http://localhost:8080 
 
      ./startup.sh
 if you want stop tomcat, you can write this
 
       ./shutdown.sh
      
## Process your file

###### Export java server to war file
     
Export -> Web(WAR file) -> Finish

###### Enter your VM

    ssh ubuntu@10.xx.xx.xx
    
###### Move your war file from the desktop to the tomcat/webapps

     scp ~/Desktop/xxx.war ubuntu@10.xx.xx.xx:/usr/local/apache-tomcat9/webapps
 
Now Run Tomcat again if your file(apache-tomcat9/webapps) have unzip ,you successfull

## Install and Export SQL on VM

##### Install sql on VM(ubuntu)

     sudo apt-get update
     sudo apt-get install mysql-server

you need to move your .sql on VM

##### Import you .sql on VM

     mysql -u root -p
     mysql> use db_name;
     mysql> source xxxx.sql;
     
Now is finish, but be careful .war is the same as VM JAVA environment 
