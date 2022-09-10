# Introduction
---
This repository contains the dataset collected from a Twizy electric vehicle in the roads of Rabat-Sale-Kenetra
(RSK), Morocco.
During the collect of the dataset (the collect process take place in different days, between March to July 2021), three main trajectories were selected; T1,T2 and T3.
* The **T1** trajectory is done mostly in an urban road with a segment in a ring road (**red** in the figure bellow).
* The **T2** trajectory is done in an urban road (**blue** in the figure bellow).
* The **T3** trajectory is done in a ring road (**black** in the figure bellow).


![used trajectories](trajectories.png)

# Collected data
---
The collected dataset contains the following fields:
* **Date** and **Time** : the date and time of the collect
* **SoC**: the battery state of charge of the battery
* **Speed**: the electric vehicle speed
* **Mode**: the driving mode (**N**eutral,**D**rive,**R**everse)
* **LAT**: latitude
* **LON**: longitude
* **ALT**: altitude
* **GpsSpeed**: the vehicle speed from the GPS
* **Temperature**: the ambient temperature
* **Humidity**: the air humidity
* **Weather**: the sky status (sunny, cloudy, rainy ...)
* **WindSpeed**: the speed of the wind
* **Traffic**: the traffic condition:
    * 0 : low traffic
    * 1 : medium traffic
    * 2 : high traffic
* **SpeedLimit**: the speed limit in a current road segment.



# License
This data-set is under the [CC-BY-4.0 license](./LICENSE.md).
