# Mindset-UI5-Training
Collection of code and setup info for UI5 training by Mindset

## Prerequisites ##
### In-class portion ###
+ VPN setup
+ Account in Mindset demo system
+ Account in Mindset HCP system for Web IDE portion

### Play-at-home ###
+ Your own ABAP backend and Gateway systems (can be embedded or hub) 
+ A trial or your own HCP system with Web IDE service activated

## Setup ##
If you're in class, we'll do this together as well. Play-at-home: follow along here. 

### ABAP ###
+ Set up a simple plant DDIC structure. 

![alt text](https://raw.githubusercontent.com/paul-modderman/Mindset-UI5-Training/master/Plant_Entity_DDIC.png "Plant Entity")

+ Set up a maintenance request DDIC structure. 

![alt text](https://raw.githubusercontent.com/paul-modderman/Mindset-UI5-Training/master/MaintRequest_Entity_DDIC.png "MaintRequest Entity")

+ Create a project in SEGW. 
+ Import the plant DDIC structure into an entity/entityset called Plant/PlantSet. 
+ Import the maintenance request DDIC structure into an entity/entityset called MaintRequest/MaintRequestSet. 
+ Set update/create settings on MaintRequest

![alt text](https://raw.githubusercontent.com/paul-modderman/Mindset-UI5-Training/master/MaintRequest_Entity_CREATE_UPDATE.png "Create/Update Settings")

+ Plug methods in from the ABAP class file in this project. ABAP doesn't have a great git in-out system, so you'll have to just pick apart the methods in the file. 
+ Activate the class, and generate and activate the project in SEGW. 
+ Use /IWFND/MAINT_SERVICE to activate the service on the gateway system (hub or embedded). 

### Web IDE ###
+ Set up your SAP Gateway system on HANA Cloud Platform through the [HANA Cloud Connector](http://www.sdn.sap.com/irj/scn/go/portal/prtroot/docs/library/uuid/1019847e-e2aa-3210-6f97-93fbd76947ef?QuickLink=index&overridelayout=true&59983513326533). 
+ Open your Web IDE.
+ File...Import, and choose the .zip file.
+ Make sure to make the contents of the file the root of the project. So you'll have YOUR_PROJECT_FOLDER/webapp as the structure. 
+ You can use ZTRAINING_UI5_BASE_APP as the name of your project to keep things consistent in all the code. If not, you'll have some editing to do to match up with your environment. Namespaces, service references, and other things will need to be evaluated as well - manifest.json, index.html, Component.js, controllers, views will all need some tweaking if you have to use a different project structure. 
