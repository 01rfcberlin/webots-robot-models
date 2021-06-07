# webots-robot-models

The exported [Webots](https://github.com/RoboCup-Humanoid-TC/webots) robot models of 01. RFC Berlin.

On the left is the RFCRobot2016.proto Model and on the right the RFCRobot2016SimplifiedVisuals.proto

![RFCRobot2016](/preview/RFCRobot2016.png)
![RFCRobot2016SimplifiedVisuals](/preview/RFCRobot2016SimplifiedVisuals.png)

Docker image
------------

You can start 4 of our robots like this:

```
docker run -it --rm -eROBOCUP_SIMULATOR_ADDR=172.17.0.1:10001 -eROBOCUP_ROBOT_ID=1 ghcr.io/01rfcberlin/rfc-robot
docker run -it --rm -eROBOCUP_SIMULATOR_ADDR=172.17.0.1:10002 -eROBOCUP_ROBOT_ID=2 ghcr.io/01rfcberlin/rfc-robot
docker run -it --rm -eROBOCUP_SIMULATOR_ADDR=172.17.0.1:10003 -eROBOCUP_ROBOT_ID=3 ghcr.io/01rfcberlin/rfc-robot
docker run -it --rm -eROBOCUP_SIMULATOR_ADDR=172.17.0.1:10004 -eROBOCUP_ROBOT_ID=4 ghcr.io/01rfcberlin/rfc-robot
```
