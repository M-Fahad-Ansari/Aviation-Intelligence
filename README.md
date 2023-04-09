# Aviation-Intelligence
Data analytics solution on an aviation industry by comparing characteristics of flights 


Objectives:
 To heel and deals with charges airline have to give.<br>
 To estimate fuel consumption and many other factors.<br>
 To develop a business model to reduce effort of particular airline.<br>
 To examine causes for flight delays.<br>
 To optimize flight operations.<br>
 To reduce further economic loss for airlines.<br>
 To lessen inconvenience occurred to people at airport.

Benefits:<br>
 Provide user with report beneficial to optimize and overcome their operation
problems.<br>
 Improve company revenue and lower costs.<br>
 Help in decision making.<br>
 Cut down the overall cost and create a better environment.

Picture of real time ADSB API data:<br>
![image](https://user-images.githubusercontent.com/21281540/230773062-5ab1409e-4437-4d15-9e96-9d1e3e0b2c9a.png)

Workflow DFD:<br>
![image](https://user-images.githubusercontent.com/21281540/230773101-f226c97d-4803-4302-9d9c-e2a0710bfaf9.png)


Research: <br>
The research phase is basically “how” the objectives are going to be achieved, how we can accomplish the set goals. The goal of project can be describing as the proof of concept of to what person understands from the problem, but the problem is not solved by statement but its need to be validated learned throughout the time, which needs sincere dedication towards the understanding and time to gradually increase in phases but not atomic. This research is divided into three research phases including:

First Phase: Feature extraction and pre-processing<br>
Second Phase: Search of technique to calculate fuel consumption<br>
Third Phase: Search of technique to estimate charge<br>
Fourth Phase: Research on how to track flights<br>

Project Modules: <br>
Module I- Fuel consumption based:
In this module, we calculate fuel of the aircraft from the preprocessed data we alread developed. The attributes that are required for calculating fuel are already present in that data.

Module II- Charge Estimation:
The flow of charge estimation works in a way that it acquires the arrival and departure of flight takes, afterwards, it sends value to python script from UI to Python script with the help of Flask server, which calculates charge estimates from going one country to another, we can expect, the given source to any country between source and destination. After calculations, results are thrown towards UI via Flask server. With charge estimated, all statistics related to that flight, which is paying charge are shown in tabular form.

Module III- Real-time Flight Tracking:  
In this module, ADS-B’s API is being loaded which gives real-time data of every flight in air. The ID which was sent from JavaScript is searched in that real-time data and its current speed, destination, current altitude, current latitude & longitude is extracted. Now, these attributes are sent back to JavaScript where we calculate the miles left to reach the destination, using haversine formula that needs 4 coordinates: current latitude and longitude and destination latitude and longitude. A google maps function is being used to find the latitude and longitude of the destination from its name, then these coordinates are passed to
the haversine formula for calculation of miles.

Module VI- Comparison of flights:
For comparison of two flights,
we have taken two airlines which we need to be compared, going on the same source and destination taken as well. After taken all inputs, the results contain two separate cards (a sort of div) which shows the short statistics of flights Upon expanding, can get full statistics in tabular form.

Module V- MIS Report Generation: 
By passing the type of report user want, he/she can have complete performance features of a flight. When user selects from dropdown, the data is sent to script, by which corresponding data is retrieved, group by the input, and then showed on UI summed up.
