# Dreamforce'16 
##IOT Cloud & Heroku Enterprise: *Robotics Service Fault Ingestion App*

**How to Deploy & Configure the Demo**

* Ensure you have a [Heroku Account](https://signup.heroku.com) and are signed into it
* Click the Deploy to Heroku Button below
* Leave the pre-populated Configuration Vars as-is, unless asked to modify them
* Confirm the Deploy
* Watch the magic of IOT Cloud & Heroku together!

**What the Configuration Variables mean**

- `robotID` - identifies the Heroku App to IOT Cloud as a "unique Robotics Device" and must be unique
- `iotToken` - allows IOT Cloud to authorize incoming messages to its Endpoint
- `endpointURL` - URL the Heroku App uses to send "Robot Arm & Controller Fault data" (aka the IOT Endpoint)
- `IRON_MQ_PROJECT_ID` - allows the Heroku MQ listener to know where incoming messages should be stored (where its queues live)
- `IRON_MQ_TOKEN` - allows the Heroku MQ to authorize incoming messages from IOT Cloud to its Queue Endpoint
- `queueURL` - URL the IOT Cloud Orchestration uses to send "Robot Arm & Controller Fault data" (aka the Heroku App Endpoint)

**Technologies Used in this Demo**

1. Heroku Enterprise: *used to generate large amounts of real-world data & send it to the IOT Cloud endpoint*
2. IOT Cloud: *handles message ingestion, orchestration & business workflow for the 'Heroku IOT Demo App'*
3. Heroku MQ (Message Queue) Add-On: *used to handle UX change responses from IOT Cloud to the Heroku App*
4. ASP.NET Core: *language the Heroku App was written in (refer to [.NET Buildpack Support](http://www.dotnetbuildpacks.com))*

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/heroku-softtrends/DF-Robot)

**What to Expect Once Deployed**

![alt text](https://s3.amazonaws.com/herokumximages/heroku-robot.png "Heroku IOT Cloud Robotics Monitoring App")

1. Click *"Start Sending Data"* to begin sending *"No Fault"* sensor data
2. To generate a Robotics Arm Fault, click the *"Simulate Robot Arm Fault"* checkbox; you will see the visual monitor change to reflect the current fault
3. To generate a Robotics Controller Fault, click the *"Simulate Controller Fault"* checkbox; similar visual monitor change will occur
4. To generate a complete Robotics Failure, click both of the Fault checkboxes; you will see similar visual monitor changes
5. To return the Robotics Fault Monitor to normal, uncheck both Fault checkboxes and click *"Stop Sending Data"*

**Support or Questions**

* Contact [us](mailto:david@heroku.com) if you have any questions about this Dreamforce'16 IOT Cloud & Heroku Demo
