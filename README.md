# AOLE Project

> AOLE (Aalto Factory of the Future in the Cloud) project proposes an idea of creating a virtual ecosystem of an automation-related setting (e.g. manufacturing, logistics) which can be assessed and interacted remotely. This idea can be further developed in both academia and industrial direction, with the purpose of validating new ideas or online training.  

![Architecture](https://user-images.githubusercontent.com/63422870/103788345-660d9b80-5047-11eb-95bc-bb0c2cbbc77d.PNG)  

First of all, I would recommend you to read the project report. Then you can follow the README files for installation and how to use the software. Finally you check out this tutorial [video](https://youtu.be/iiVabQawqck) I created. Have fun!!!

---

### Table of Contents
You're sections headers will be used to reference location of destination.

- [Description](#description)
- [Installation](#installation)
- [How To Use](#how-to-use)
- [References](#references)
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
* Install VC2OPCUA ([Link to download](https://github.com/SintefManufacturing/vc2opcua))

#### Beckhoff TwinCAT
* Install TwinCAT ([Link to download](http://www.beckhoff.com/TwinCAT/))
    - Requirements on all devices at least TwinCAT v.3.1.4022

#### Mosquitto (MQTT broker)
* Installation file and guide can be found under IoTTask folder
* Install OpenSSL (Win32OpenSSL-1_0_2n.exe) to root folder
    - On step “Select Additional Tasks” choose copy DLLs to /bin directory
* Installing mosquitto (mosquitto-1.4.15a-install-win32.exe)
* Put pthreadVC2.lib in mosquitto folder

#### UaExpert (OPC UA Client)
* Install UaExpert ([Link to download](https://www.unified-automation.com/downloads.html))

#### ThingSpeak (Cloud)
* Create an account or sign in with MATLAB account ([Log in here](https://thingspeak.com/login))

[Back To The Top](#AOLE-Project)

---

## How To Use

#### Visual Components
* Open Visual Components file named "Layout.vcmx" (under Visual Components folder)
![Layout](https://user-images.githubusercontent.com/63422870/103789610-e54f9f00-5048-11eb-8b9d-be63f795fc88.png)
* Set up OPC UA connection to TwinCAT and UaExpert
![VC2OPCUA](https://user-images.githubusercontent.com/63422870/103790474-eaf9b480-5049-11eb-9fb2-6b972687f026.PNG)
![VC-TwinCAT](https://user-images.githubusercontent.com/63422870/103791345-03b69a00-504b-11eb-8f67-0436d8bd39e2.png)
* Create Variable Pairs with TwinCAT
![Paired variables](https://user-images.githubusercontent.com/63422870/103791580-47a99f00-504b-11eb-9567-86f55389d950.png)
* Run simulation

#### Beckhoff TwinCAT
* See "installationGuide.pdf" in the IoTTask folder for more information
* Open "IotMqttSampleUsingQueue.sln" file (can be found in TwinCAT folder)
* Remember to change your IP address and port info
![IP address and port](https://user-images.githubusercontent.com/63422870/103790988-930f7d80-504a-11eb-8c4f-b2d24ebaedf4.png)

#### Mosquitto (MQTT broker)
See "installationGuide.pdf" in the IoTTask folder for more information

#### UaExpert (OPC UA Client)
Discover the server address in UaExpert. If it cannot detect the server, manually connnect it through the server address "opc.tcp://localhost:51210/UA/VcOpcUaServer"

#### ThingSpeak
* Log in to ThingSpeak
* Create channel and field, ([guide](https://www.youtube.com/watch?v=sBAuexThr30))
* Make private channel and field
* Create Write API Key
* Replace these values of API key in TwinCAT code
![API key](https://user-images.githubusercontent.com/63422870/103790777-52176900-504a-11eb-95b9-58852edecb04.png)

## References
Detailed information on mosquitto broker (https://mosquitto.org/)  
To get API keys create an account on (https://thingspeak.com/)  
Tutorials on Visual Components (https://academy.visualcomponents.com/)

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
