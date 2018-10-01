
# Introduction
E-Monitor is the Realtime MQTT based monitoring system which helps the user to have a web interface for their IOT projects.
It is easy to use and easy to set up.
Requires minimal lines of code to be changed OR `NONE`.

NOTE: NO History is maintained of Logged data.

###
> Please Set your MQTT Credentials.
> Read the Docs and then jump to Demo.

Demo is @ [E-monitor](https://mohinishsharma.github.io/E-monitor)

## Steps to Implement

To use this Realtime Monitoring system.

1. You need to set your MQTT Credentials. Click on the gear button on the top right corner.
    + You will need:
      - `Hostname`
      - `username`
      - `password`
      - `port number` (Secure port is Recomended)
      - `Device id` (Its an arbitrary `name` to uniquely identify IoT device.)
    + After entering data click on `Set & Connect`.
2. From your IoT device Publish all the data to the topic name `Device_id/info`.
    + Data should be in Valid JSON format
      ```json
      {
        "Sensor1": 25,
        "Sendor2": 1,
        ...
      }
      ```
    and the table will be automatically populated.
3. All the Input from `Command` Input is published out on MQTT topic `Device_id/cmd` and the output of the Command is subscribed on `Device_id/cmdout` MQTT topic.
