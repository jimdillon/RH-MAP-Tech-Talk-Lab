# RH-MAP-Tech-Talk-Lab
Red Hat Mobile Tech Talk Lab will guide the user through creating a simple JavaScript Hybrid App, a Cloud App and an MBaaS that uses google geocoding API and the Dark Sky weather service to provide the current temperature for city and state input.

##Requirements:
* node.js version 0.10.3 - https://nodejs.org/en/download/releases/
* fhc version 1.1.5 - https://www.npmjs.com/package/fh-fhc
* grunt - https://www.npmjs.com/package/grunt
* git - https://git-scm.com/downloads
* openshift.feedhenry.com account - https://openshift.feedhenry.com/
* Add your ssh key to your openshift.feedhenry.com account - http://openshift.feedhenry.com/docs/dev_tools/local/ssh_keys.html
* google geocoding API key - https://developers.google.com/maps/documentation/geocoding/get-api-key#key
* Dark Sky Weather API key - https://developer.forecast.io/
* Text editor of your choice (I'm enjoying atom with the vim extension at the moment.  Others enjoy Sublime Text.)

#Instructions
## Go to your openshift.feedhenry.com account and create a new Project using the 'Hello World Project' as your template.
  * Login
  
  * Click the Projects Button
![alt tag](https://raw.github.com/jimdillon/RH-MAP-Tech-Talk-Lab/master/create_project_0.jpg)
  
  * Click the New Project Button
![alt tag](https://raw.github.com/jimdillon/RH-MAP-Tech-Talk-Lab/master/create_project_1.jpg)
  
  * Choose the Hello World Project
![alt tag](https://raw.github.com/jimdillon/RH-MAP-Tech-Talk-Lab/master/create_project_2.jpg)
  
  * Name your Project and Click Create
![alt tag](https://raw.github.com/jimdillon/RH-MAP-Tech-Talk-Lab/master/create_project_3.jpg)
  
  * Click Finish
  ![alt tag](https://raw.github.com/jimdillon/RH-MAP-Tech-Talk-Lab/master/create_project_4.jpg)


## Create a directory on your local machine, move into that directory.
## Clone your Project

  * fhc target [https://Yourdomain.openshift.feedhenry.com]

  * fhc login

  * fhc projects to list your project(s)

  * Copy the ID of the project you would like to clone

  * Run fhc projects clone [Your copied project id]
![alt tag](https://raw.github.com/jimdillon/RH-MAP-Tech-Talk-Lab/master/lab_fhc.jpg)

## Open the Hybrid client in your favorite editor and head to the client instructions. https://github.com/jimdillon/RHMAP_Lab_Client

## When you are finished with the client, open the Cloud App in your favorite editor and head to the cloud instructions. https://github.com/jimdillon/RHMAP_Lab_Cloud

## When it's time to create the MBaaS, go back to your openshift.feedhenry domain and create an MBaaS using the 'New MBaas Service' Template

* Click Services & APIs and then click Provision MBaaS Service API
![alt tag](https://raw.github.com/jimdillon/RH-MAP-Tech-Talk-Lab/master/create_MBaaS_0.jpg)

* Choose New MBaaS Service
![alt tag](https://raw.github.com/jimdillon/RH-MAP-Tech-Talk-Lab/master/create_MBaaS_1.jpg)
* Name the Service and click Next
![alt tag](https://raw.github.com/jimdillon/RH-MAP-Tech-Talk-Lab/master/create_MBaaS_2.jpg)
* Once the Service has been created, click Finish
![alt tag](https://raw.github.com/jimdillon/RH-MAP-Tech-Talk-Lab/master/create_MBaaS_3.jpg)

## Go to your local directory that contains the client and cloud Apps and run git clone [Git URL on MBaaS Detail Page]  It wil be something like git@git.openshift.feedhenry.com:yourdomain/projectname
![alt tag](https://raw.github.com/jimdillon/RH-MAP-Tech-Talk-Lab/master/create_MBaaS_4.jpg)
![alt tag](https://raw.github.com/jimdillon/RH-MAP-Tech-Talk-Lab/master/create_MBaaS_5.jpg)

## Then open the cloned project in your editor and head to the instructions https://github.com/jimdillon/RHMAP_LAB_MBaaS

## Once you finish your MBaaS, head back to the Cloud App to hook it up to your new MBaaS.

## Get everything working locally, and then git push the 3 Apps to the platform, set up your environmental variables, deploy and enjoy.
```
git add -A
git commit -m 'I made some changes and want to push them to the Red Hat Mobile Application Platform'
git push origin master
```
## Once you've pushed your changes to the cloud you'll need to deploy your changes.
* Open your MBaaS, click the Deploy icon and then click Deploy
* Open your Cloud App, click the Deploy icon and then click Deploy
* Now you can open your Clien App and run your App in the App Preview

# Extra Credit for those with Android Phones
Deploy your App to your Android Device

* Open your Client App
* Click the Build Icon

In the Build A Binary Screen

* Platform: Android
* Git Branch/Tag: master
* Build Type: Debug
* Select Cloud App: Select your Cloud App
* Click the Build Button
* Scan the QR Code that pops once the build is finished and enjoy your new mobile temperature app.
