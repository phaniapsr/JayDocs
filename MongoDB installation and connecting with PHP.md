###### Prepared By: Phani Kumar Chinta
###### Date  : 06 Apr 2016


#### Overivew
This document explains the installation steps of MongoDB in windows and connecting with PHP installed with XAMPP build.

#### Step1: 
For downloading MongoDB exe go to this url https://www.mongodb.org/downloads#production and install this in the local machine

#### Step2:
For downloading php DLL file go this url https://github.com/maryo/php-5.5-windows-extensions/blob/master/php_mongo-1.4.5-vc11-x86/php_mongo.dll
In this page click on the 'view raw' link for downloading.

#### Step 3:
Now place this downloaded DLL file in the path xampp/php/ext directory. (Assuming you are using xampp and in my case it is D:\xampp\php\ext).

#### Step 4: 
Now edit php.ini file in the path xampp/php/php.ini and put the line 

```
extension=php_mongo.dll

```
in the extensions section and restart the apache. After restarting you should see mongo exension in your phpinfo().

#### Step 5:
Now open two command line windows and go to the bin directory in both windows where the MongoDB was installed. In my case it is "C:\Program Files\MongoDB\Server\3.2\bin"

#### Step 6: 
Now create a folder for storing the data of MongoDB any where out side the windows installation directory. In my case i have created at "E:\mondodb\data".

#### Step 7: 
Run the follwoing command - This is for running the MongoDB server.
```
mongod.exe --dbpath E:\mondodb\data
```
#### Step 8: 
Now in the other cmd window run the following command - This is the client.
```
mongo --port 27017
```
#### Step 9:
Now you can run any PHP code connecting with MongoDB and see the result in client cmd window.
