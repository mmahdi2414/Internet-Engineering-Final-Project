#Internet Engineering Final Project
Here is the specification of final project. 
## General Idea 
The idea is to write an application that can be used in case of emergency situations. It suppose to help the team involved in the disaster situation such as earthquake to fill out reports about the situation and give a realistic view to the operation centres. 

As the impact of situations such as earthquake or flooding is spread across a large geographical space, it is crucial to have a realistic view of the situation to give effective help to people in crisis. 

For example questions like below are very important to be answered within hours of the start of the crisis: 
* What are the main help that they need? 
  * Food 
  * Water
  * Blanket
  * First aid supply 
  * Warmers 
  * Tent 
  * .... 
* And how much of each they need? 
* What is the number of injured or dead people in the region ? 
* What is the number of injured people in critical situation ? 
* How many injured must be carried with ambulance? 
* .... 

Answer to any of the above questions can save lots of life and help to quickly help humans in crisis. 

In this project you re going to write such application. 

## Main Application Users
### Field Agents 
These users are  in the field and there are many of them. Most of them have smart phone and no laptop is available for them. So for these users you have to create a mobile web or native application. What they are working with, is very similar to what you have done in your second Homework. 

They normally fill out report forms and send critical information to control centre. 

### Control Centre Agent 
These users are interested to get the reports from Field Agents and see the consolidation of those  reports over their dashboards. This will help them to properly distribute the help to the crisis region. 

### System Administrator
This user sets up the system 

## How should it work
### System Admin
 creates a number of dynamic forms (As you have seen in the Homework 2). Sys admin does not have a user interface but there should be a REST API to let sys admin manage (CRUD) following entities: 
* Forms 
* Areas:  Regional Polygons (Similar to what you did in HW1) 


### Field agents 
They open the application and start to fill the forms (HW2)  and submit their forms to server.
*  The server must preserve their filled forms.
*  For each GeoLocation field the system should find all of the areas that location is inside and store that information against the record 
### Control Centre Agents 
They should get a summary report on what has been submitted by Field agents. For each form they should be able to fulfil following use cases: 
* See list of forms in the system 
* If they click on each form they should be able to: 
  * See all of the responds to that form(records) in human readable form (Table) Including the name of the areas that the geo-location fields reside in 
  * See the details of one record if click on the row 
  * For numerical fields  show the sum  of the column in last row 
  * Filter the report by geo-locations. They have to first select a geolocation field and then select a predefined area and the report must be filtered to show the records that the selected geolocation field is inside that area 
  * Being able to export the result of report to CSV file 
## General Authentication 
Authentication and Authorization is in scope of project. That means users must login to the system and system detect their role and show them right pages.  User management is out of scope for this projec. 

For additional points you can integrate with a service like [Auth0](https://auth0.com/) it will give you User Management and Single Sig-on 

 ```
 Please note that API calls also should also be protected 
 that means all API must be protected
 ```
## Deployment 
You should deploy your application on Heroku  and use Mongo MLab Cloud provider to showcase your application. I want to see a running application LIVE!
## Extra Points
If you implement any of following features you will get extra point: 
* Write a Native/Hybrid/React-Native application to support the Field Agents 
* Adding offline feature to the web frontend for field agents (PWA/HTML5)
* Graphical Dashboards for Control Centre Agent 
* Integration with  Auth0 
* Filtering ability for other fields (Numeric / Date / String)
* Unit Test / Integration Test 
* Integration with Gitlab CI 
* Use of one of the Web frameworks 
* Using GraphQL 
## Documentation 
You should have a documentation on your project source code. Your documentation should contain Architecture of the project. Something like following information: 

* Development View 
  * Source Code Structure 
  * Git structure and branching 
  * You code components 
  * Technologies and libraries used. 
  * The database system that is used and resoning behind it 
* Process view: 
  * How the processes are seprated 
  * Communication mechanisnm 
* Physical View 


