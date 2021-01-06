# AOLE Project

![Project Image](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.youtube.com%2Fchannel%2FUCkWiZDPsajIeYHWgUsjYEag&psig=AOvVaw35I5g3usLV_jVViy76_Uaa&ust=1609980660477000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCPjJpL6Lhu4CFQAAAAAdAAAAABAD)

> AOLE (Aalto Factory of the Future in the Cloud) project proposes an idea of creating a virtual ecosystem of an automation-related setting (e.g. manufacturing, logistics) which can be assessed and interacted remotely. This idea can be further developed in both academia and industrial direction, with the purpose of validating new ideas or online training.

---

### Table of Contents
You're sections headers will be used to reference location of destination.

- [Description](#description)
- [Installation](#installation)
- [References](#references)
- [How To Use](#how-to-use)
- [License](#license)
- [Author Info](#author-info)

---

## Description

The scope of this project is to create a virtual representation of an automated production layout on Visual Components where users can interact, simulate and make modifications through a set of APIs. These APIs will be created based on the granular level of control, ranging from individual control to sequence control. The intercommunication between Visual Components and the middlewares involved is feasible via industrial communication protocol (OPC UA) and IoT messaging protocol (MQTT). The corresponding APIs can be called from OPC UA Server and the desired data of the simulation and layout can be visualized on OPC UA Client and on Cloud (ThingSpeak).

#### Requirements
To successfully compile and run all parts of the project the following software and environment must be installed and set up:
* Visual Components
* Beckhoff TwinCAT
* Mosquitto
* UaExpert
* ThingSpeak

[Back To The Top](#AOLE-Project)

---

## Installation

#### Visual Components (Simulation Environment)
* Install Visual Components ([Link to download](https://www.visualcomponents.com/products/downloads/))
    - Requires a license that supports modelling and the OPC UA connectivity feature
#### Beckhoff TwinCAT
* Install TwinCAT ([Link to download](http://www.beckhoff.com/TwinCAT/))
    - Requirements on all devices at least TwinCAT v.3.1.4022

#### Mosquitto (MQTT broker)
* Install OpenSSL (Win32OpenSSL-1_0_2n.exe) to root folder
    - On step “Select Additional Tasks” choose copy DLLs to /bin directory
* Installing mosquitto (mosquitto-1.4.15a-install-win32.exe)
* Put pthreadVC2.lib in mosquitto folder

#### UaExpert (OPC UA Client)
* Install UaExpert ([Link to download](https://www.unified-automation.com/downloads.html))

#### ThingSpeak (Cloud)



#### API Reference

```html
    <p>dummy code</p>
```
[Back To The Top](#AOLE-Project)

---

## How To Use

## References
Detailed information on mosquitto broker (https://mosquitto.org/)
To get API keys create an account on (https://thingspeak.com/)
[Back To The Top](#AOLE-Project)

---

## License

Apache License, Version 2.0

Copyright (c) [2021] [Duc Pham]

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

[Back To The Top](#AOLE-Project)

---

## Author Info

- Github - [reliumd](https://github.com/reliumd)
- LinkedIn - [Minh Duc Pham](https://www.linkedin.com/in/minh-duc-pham-468ba9a8/)

[Back To The Top](#AOLE-Project)
