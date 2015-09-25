# RH-MAP-Tech-Talk-Lab
Red Hat Mobile Tech Talk Lab will guide the user through creating a simple JavaScript Hybrid App, a Cloud App and an MBaaS that uses google geocoding API and the Dark Sky weather service to provide the current temperature for city and state input.

##Requirements:
* node.js version 0.10.3
* fhc version 1.1.5
* grunt
* openshift.feedhenry.com account
* google geocoding API key
* Dark Sky Weather API key
* Text editor of your choice

##Instructions
* Go to your openshift.feedhenry.com account and create a new Project using the 'Hello World Project' as your template.
* Add your ssh key to your user profile (http://openshift.feedhenry.com/docs/dev_tools/local/ssh_keys.html)
* Create a directory on your local machine, move into that directory.
* run fhc target [https://Yourdomain.openshift.feedhenry.com]
* run fhc login
* run fhc projects to list your project(s)
* Copy the ID of the project you would like to clone
* run fhc projects clone [Your copied project id]
![alt tag](https://raw.github.com/jimdillon/RH-MAP-Tech-Talk-Lab/edit/master/lab_fhc.jpg)
* Open the Hybrid client in your favorite editor and head to the client instructions. https://github.com/jimdillon/RHMAP_Lab_Client
* When you are finished with the client open the Cloud App in your favorite editor and head to the cloud instructions. https://github.com/jimdillon/RHMAP_Lab_Cloud
* When it's time to create the MBaaS go back to your openshift.feedhenry domain and create an MBaaS using the 'New MBaas Service' Template
* Go to your local directory that contains the client and cloud Apps and run git clone [Git URL on MBaaS Detail Page]  It wil be something like git@git.openshift.feedhenry.com:yourdomain/projectname
* Then open the cloned project in your editor and head to the instructions https://github.com/jimdillon/RHMAP_LAB_MBaaS
* Once you finish your MBaaS, head back to the Cloud App to hook it up to your new MBaaS.
* Get everything working locally, and then push the 3 Apps to the platform, set up your environmental variables, deploy and enjoy.
