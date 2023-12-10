# tomcat-project
how to deploy .war file on tomcat server via amazon linux

first download tomcat by below website link :
https://downloads.apache.org/tomcat/tomcat-9/v9.0.83/bin/

wget https://downloads.apache.org/tomcat/tomcat-9/v9.0.83/bin/apache-tomcat-9.0.83.tar.gz
------------------------------------------------------------------------------------------
tar -xvf
-------------------------------------
step 1) 
cd webapps/manager/META-INF/context.xml
line number 21 & 22 ----> delete
-----------------------------------------------------------------------------------------------
step 2)
cd conf/    ----> folder
tomcat-users.xml  ----> file edit 

<role rolename="manager-gui"/>
<role rolename="manager-script"/>
<user username="adi" password="123456" roles="manager-gui,manager-script"/>
--------------------------------------------------------------------------------------
step 3)
cd bin/     ----> directory
./shutdown.sh
./startup.sh
-------------------------------------------------------
