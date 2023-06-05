<details open="open">
  <summary><h2 style="display: inline-block">Table of Contents</h2></summary>
  <ol>
    <li> <a href="#running-the-project-locally-for-developers">Running the Project Locally (developer)</a></li>
    <li><a href="#updating-the-google-sheets-services-call-developers-and-client">Updating the google Sheets Services call (developer / client)</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#template-sheets-for-client">Google Sheet Templates</a></li>
  </ol>
</details>
<br/>
<br/>

## RUNNING THE PROJECT LOCALLY (FOR DEVELOPERS)

### STEPS ###
  1. Fork or clone the Repo to your local machine
  
  2. Once the project is on your computer go on to terminal and go to where the project is saved, once there run the command
  * ```npm install```    
  
  3. Once all packages have been installed run the command
  * ```npm run dev```
  
  4. The Local server has now been started, in your web browser go to ```localhost:3000``` to view the web app
  
  ![](https://github.com/DDSkunkworks/ButcheryFundamentals/blob/main/readmeassets/openterminal.gif)

<br/>
<br/>


## UPDATING THE GOOGLE SHEETS SERVICES CALL (DEVELOPERS AND CLIENT)
> Make sure that the [Google sheets](#template-sheets-for-client) are copied onto the account you'd like to google services to use
> > have these's google sheets open in another tab as we will be using them in later steps

### STEPS ###
1. Go to [Google cloud services](https://console.cloud.google.com)
2. In the top left corner where it says ```Select a project``` press and select  ```New Project``` in the new window
3. After naming the project press the ```create``` button
 * once pressed a process will start where it creates the portal platform for the project (press the ```go to dashboard``` once process is finished)
4. in the top left inside of the dashboard section press the ```Go to project settings``` button
![](https://github.com/DDSkunkworks/ButcheryFundamentals/blob/main/readmeassets/goToProjectSettings.png)
 
<br/>
<br/>

5. once inside project setting section press ```Service Accounts  -> CREATE SERVICE ACCOUNT (on top bar)``` 
![](https://github.com/DDSkunkworks/ButcheryFundamentals/blob/main/readmeassets/serviceAccount.png)

6. Name the service account name whatever you'd like and press ```done```
7. Once the account has been created press the ```Actions``` button and then ```Manage Details```
![](https://github.com/DDSkunkworks/ButcheryFundamentals/blob/main/readmeassets/manageDetails.png)

<br/>
<br/>

8. In this new screen press ```Keys``` and ```Add key -> Create new key``` 
![](https://github.com/DDSkunkworks/ButcheryFundamentals/blob/main/readmeassets/keys.png)

<br/>
<br/>

9. select the ```JSON``` option in the window that popsup and press ```create``` doing this step will then save a .JSON file to your computer
10. open this .JSON file with some text editor of your choice and copy the value that is associated with the key ```client_email``` (do not destroy the .json file as we will be needing it for future steps)
> for example `"client_email": "gbc-butchery-api@gbc-butchery-388911.iam.gserviceaccount.com",`

| Key        | value           |
| ------------- |-------------  |
| client_email     | `gbc-butchery-api@gbc-butchery-388911.iam.gserviceaccount.com` |

11. in the google sheets that you made a copy of earlier in the steps press the ```share``` the button and paste the email that you copied from the previous step
![](https://github.com/DDSkunkworks/ButcheryFundamentals/blob/main/readmeassets/sharegmail.gif)

<br/>
<br/>

12. using [Base code 64](https://www.base64encode.org/) copy all of the contents from that .json file and paste into the encoder section of the web application, once pasted press the ```encode``` button and save the results to  a file for later use

For Developers 
---
13. Copy the id of both google sheets from the url and paste the values to the respective spots inside the .env file of the project 
* DO NOT CHANGE THE SECRET_COOKIE_PASSWORD
> for example: `https://docs.google.com/spreadsheets/d/11SijW8y4XHpFQGwHfL4sOjC9yIZ1slH5cKcrUBWIvWg/edit#gid=0`
>> id: 11SijW8y4XHpFQGwHfL4sOjC9yIZ1slH5cKcrUBWIvWg
>>> GOOGLE_LOGIN_SHEET = 11SijW8y4XHpFQGwHfL4sOjC9yIZ1slH5cKcrUBWIvWg
14. for the value ```GOOGLE_SERVICE_KEY``` paste the result from step 12
15. your application is now ready to test local or be uploaded


For Client 
---
13. follow the steps as outlined in the [uploading to vercel steps](#uploading-to-vercel-for-client)


<br/>
<br/>

## UPLOADING TO VERCEL (FOR CLIENT)

### STEPS ###
1. 
2. Go to [Vercel](https://vercel.com/) and login or signup (it's is reccom)
3. once on the dashboard press the ``add new`` button in the top right hand corner
4. select the ``project`` option
5. 
<br/>
<br/>

## TEMPLATE SHEETS (FOR CLIENT)

THE FOLLOWING SHEETS ARE MEANT TO BE USED AS A COPY FOR YOUR VERSION OF THE APPLICATION 
  * to create a copy of the sheet do the following steps in the google sheet tab you have open
    * ```File -> Make a copy```

![](https://github.com/DDSkunkworks/ButcheryFundamentals/blob/main/readmeassets/copysheet.png))

#### Results Sheet  (used for display all of the students scores of all test) #### 
* [Results Sheet](https://docs.google.com/spreadsheets/d/1BEvpO5J6H6vDXG1E_EH8fYfJsqAMZVVJRsSHdE3Mp1o/edit?usp=sharing )

#### Login Sheet  (used for determining what students are logged in) #### 
* [Results Sheet](https://docs.google.com/spreadsheets/d/1BEvpO5J6H6vDXG1E_EH8fYfJsqAMZVVJRsSHdE3Mp1o/edit?usp=sharing )
