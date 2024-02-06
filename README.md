# FabricISSTracking
This is a step-by-step guide to create a near-real time system to track the current location as well as the astronauts aboard the International Space Station in Fabric. 

Inspired and adapted from [Anshul Sharma's blog] and [Tales from the Field's Youtube Tutorial].

[Anshul Sharma's blog]: https://www.linkedin.com/pulse/real-time-monitoring-international-space-station-microsoft-sharma/
[Tales from the Field's Youtube Tutorial]: https://www.youtube.com/watch?v=-HhU7yLyuUU

## Services Used:
1. Logic Apps:
2. Event Stream:
3. KQL Database:
4. PowerBI: to visualize the incoming data

## Part One: Collecting the Data 
### 1. Create a Logic App (in Azure):
* Log into the Azure Portal
* In the search bar, search for Logic App. On the Logic App menu click on "Create".
* In the setup box for the Logic App, create a new resource group and name it "ISSTrackingSystem"
* Choose a name for the Logic App, e.g. "LocationTrackerLA" (The suffix "LA" stands for Logic App).
* In the "monitoring" tab, turn off the monitoring (not necessary for this project as it is not in production).
* Keep all the other default settings as they are. Click on Review + Create --> Create. This process may take a few minutes.
* Repeat all these steps to create another logic app in the same resource group (ISSTrackingSystem), with the name "AstronautTrackerLA".  

### 2. Create a KQL Database (in Fabric):
* In a separate tab, log into Microsoft Fabric (www.app.powerbi.com).
* On the menu bar located on the left of the screen, click on "Create" --> "See All" (under "Other Items You Can Create with Fabric") --> Scroll down to the Real-Time Analytics tab and select KQL Database.
* Name the KQL Database as "ISSTrackerDB" and click on "Create".
* This KQL Database will be used to store the real-time data of both the location of the ISS, as well as the astronauts aboard.

### 3. Create an Eventstream (in Fabric):

## Part Two: Visualization in PowerBI
