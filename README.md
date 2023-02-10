# 01. RFC Berlin's Docker image and Webots robot model

The 01. RFC Berlin participated in the [RoboCup Humanoid League 2021](https://humanoid.robocup.org/hl-2021/teams/) and the [RoboCup Humanoid League Virtual Season 21/22](https://humanoid.robocup.org/hl-vs2022/teams/).
In these competitions robots play soccer autonomously.
Because of covid they only took place virtually.

This repo contains:

* our exported [Webots](https://github.com/RoboCup-Humanoid-TC/webots) robot model, following the [Robot Model Specification](https://cdn.robocup.org/hl/wp/2021/06/v-hsc_model_specification_v1.05.pdf)
* our Docker image, following the [Server Specification](http://humanoid.robocup.org/wp-content/uploads/v-hsc_server_specification_v1.03.pdf)
* our team.json, following the [API Specification](https://cdn.robocup.org/hl/wp/2021/06/v-hsc_simulator_api_v1.01.pdf)

Webots robot model
------------------

Our RFCRobot2016.proto model in blue looked like this rendered inside Webots:

![RFCRobot2016](/preview/RFCRobot2016.png)

Docker image
------------

You can start 4 of our robots like this:

```
docker run -it --rm -eROBOCUP_SIMULATOR_ADDR=172.17.0.1:10001 -eROBOCUP_ROBOT_ID=1 -eRFC_ARGS="--record.active false" ghcr.io/01rfcberlin/rfc-robot
docker run -it --rm -eROBOCUP_SIMULATOR_ADDR=172.17.0.1:10002 -eROBOCUP_ROBOT_ID=2 -eRFC_ARGS="--record.active false" ghcr.io/01rfcberlin/rfc-robot
docker run -it --rm -eROBOCUP_SIMULATOR_ADDR=172.17.0.1:10003 -eROBOCUP_ROBOT_ID=3 -eRFC_ARGS="--record.active false" ghcr.io/01rfcberlin/rfc-robot
docker run -it --rm -eROBOCUP_SIMULATOR_ADDR=172.17.0.1:10004 -eROBOCUP_ROBOT_ID=4 -eRFC_ARGS="--record.active false" ghcr.io/01rfcberlin/rfc-robot
```

Simulate a game against the 01. RFC Berlin
------------------------------------------

In our blog we made a step-by-step write-up on how you can use the files in this repository to simulate a game against us:
https://01.rfc-berlin.de/en/blog/simulating-a-game-against-rfcberlin/
