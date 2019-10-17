# Welcome to XYZProject
# <img src="http://homepages.cae.wisc.edu/~ece533/images/fruits.png" width="50">  ABC_COMPANY
## A SOME_ABC Company Pvt Ltd employee management app

App Name : ABC Rocket

Customer : SOME_ABC Company Pvt Ltd

Development Team : 

John Dev (Android developer : May 2018 - June 2019), 

Jane Dev (Android developer : June 2019 - till date), 

Jonah Dev (Backend developer : May 2016 - till date)

Design Team : Wan Chung, Lee Chi

Management : Nikola Tisola (Sr Manger : May 2012 - June 2016), Thomas Eden (Sr Manger : July2016 - till date)

Web URL : http://ROCKETAPP.SOMECOMPANY.COM

---

**About this file**  
The purpose of this file is to provide overview, setup instructions and background information of the project. If you have joined this project as a part of the development team, please ensure this file is up to date.  
  
**Note : Any dependencies added / modified to this project which affect the running of the code in this git repository must be listed in this file. All developers must ensure that the instructions mentioned in this file are sufficient to enable a new developer to obtain a executable copy of the lastest code in this repository, without involvement from any other human assistance.**

---

**Tools and Hardware Requirements Declaration**

I) Software requirements
1) Ubuntu OS
2) Maven
3) JDK
4) Camera drivers
5) Web Cam Device
6) Http Server
7) MySQL and MySQL drivers

II) Hardware requirements
1) Minimum 8 GB RAM
2) Minimum 12 GB Available Disk Space
3) Wifi Availablility
4) Web Camera

---

**Project Technical Specifications**

* This project is a cordova based project which uses Angular 7   
  framework.  
* The angular code is first compiled using angular-cli commands,    
  then the output is moved to the cordova www directory. After which   
  the cordova build command generates final android / iOS output.   
 * The API is provided from customer  
* The design for reference is from XYZ Company Pvt Ltd Mumbai design    
  Team.

---

**Setup Instructions**  
As mentioned earlier , this is a cordova-angular project,  
The below mentioned steps may vary significantly across various operating systems, please follow them accordingly.

These instructions are aimed at a developer who has been added to the project team, after the project development has already been initiated,

Therefore the aim is to get the code from the git repository to run on the developer's system, so as to allow him / her to continue with further development.

---
**Clone the repository from GitLab :**  

```git clone git@gitserver.abccompanygit.com:root/rocket.git```

**Change current working directory to Project directory**

```cd Rocket```

( This is the cordova as well as the angular root folder. )

**Checking out the latest development branch**

As of writing this guide the main branch used for development is : develop  
To switch to this branch run : 

```git checkout develop```

**Installing dependencies**  
This project requires cordova for running,
You can install it by referring to the official cordova page : [[https://cordova.apache.org/](https://cordova.apache.org/)]

The cordova version used at the time of writing this file is : ```8.1.2```
You can check the installed version using ```cordova -v```

The config.xml file contains the list of all cordova plugins and platforms used for this project.
Please ensure this file is updated incase any plugin is added / removed.

Please follow below steps for installation :

Install Angular and Cordova NPM Dependencies

```npm i```

Next install cordova platforms and plugins

```cordova prepare```

Incase you get errors as : ```Current working directory is not a Cordova-based project.```

The www folder used by cordova cli to detect a cordova project might be missing
Simply make an empty www folder via file manager or via commandline as :

```mkdir www```

Install cordova android platform

```cordova platform add android```

---

**Start the http and mysql xampp server :**  
xampp http start  
xampp mysql start  
sudo service kurento-media-server-6.0 start

---
**Note for future developers**

Home is an addon module which adds search by name functionality to the core code
The files in the above directory when included in the index file overwrites methods, variables, css in the core code
and manipulates the DOM at runtime by adding / removing elements.
Thus the entire search logic is separated and can be included on demand,
This is the first attempt of adding additional features as modules
Future features if any should also be done in the same way,
The core code should only be modified for bug fixes or core updates
Any new feature either core or customer specific should be implemented as a pluggable module in the  `/project_directory/src/main/resources/static/addons/`  directory
