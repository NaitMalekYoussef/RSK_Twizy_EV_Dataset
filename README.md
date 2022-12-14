# Introduction 
---
[![DOI](https://zenodo.org/badge/529137067.svg)](https://zenodo.org/badge/latestdoi/529137067) [![License: CC
BY
4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
![GitHub repo size](https://img.shields.io/github/repo-size/NaitMalekYoussef/RSK_Twizy_EV_Dataset) ![GitHub
release (latest
SemVer)](https://img.shields.io/github/v/release/NaitMalekYoussef/RSK_Twizy_EV_Dataset?sort=semver)

This repository contains the dataset collected from a Twizy electric vehicle in the roads of Rabat-Sale-Kenetra
(RSK), Morocco.
During the collect of the dataset (the collect process take place in different days, between March to July 2021), three main trajectories were selected; T1,T2 and T3.
* The **T1** trajectory is done mostly in an urban road with a segment in a ring road (**red** in the figure
  bellow), it is 48 Km long with an average driving time of 1h30minutes.
* The **T2** trajectory is done in an urban road (**blue** in the figure bellow), is is also 48 Km long, with
  an average driving time of 1h40minutes.
* The **T3** trajectory is done in a ring road (**black** in the figure bellow), it is 16 Km long, with an
  average of 18 minutes.


![used trajectories](./figures/trajectories.png)

# Collected data
---
The dataset is composed of raw dataset and analyzed dataset.
The analyzed dataset contains the following fields:
* **Date** : The date of the driving cycle (**M**onth/**D**ay/**Y**ear).
* **Time** : The time during the driving cycle (**H**ours:**M**inutes:**S**econds) .
* **SoC**: The battery State of Charge (**%**).
* **Speed**: The vehicle speed  (**Km/h**).
* **Mode**: The driving mode (**N**eutral,**D**rive,**R**everse)
* **LAT**: The vehicles' latitude (°).
* **LON**: The vehicles' longitude (°).
* **ALT**: The vehicles' altitude related to the sea (**m**).
* **GpsSpeed**: The vehicle speed acquired from the GPS module (**Km/h**).
* **Temperature**: The external ambient temperature (°C).
* **Humidity**: The external relative humidity (\%).
* **Weather**: The weather status (**cloudy**, **sunny**, **raining ...).
* **WindSpeed**: The average wind speed (**m/s**).
* **Traffic**: the traffic condition:
    * **0** : low traffic
    * **1** : medium traffic
    * **2** : high traffic
* **SpeedLimit**: The speed limit in the current road segment (**Km/h**).

I addition to those fields, the raw data contains the following fields:
* **Odometer** : The distance traveled by the EV (**Km**).
* **ExactSpeed** : The exact EV speed, this value is collected directly from the EV using the CAN Bus like the EV speed, but sometimes their values are not equal. (**Km/h**).
* **Id** : The id of the CAN Bus message.
* **Data** : The collected data messages from the CAN Bus in Hex values.
# Data collection system
---
The data collection system is composed of an embedded system that is deployed in a Renault Twizy. The embedded
system is composed of an NVIDIA Jetson nano, and Arduino micro, a CAN bus protocol module, a GPS module, a boost converter to power the system from the
auxillary battery and a tablet holder which act as a user interface.
![Data collection system](./figures/electronic_card.png)
![Data collection system](./figures/deployed_system.png)
![Data collection system](./figures/monitoring_system.png)

# Data simple
---
The figure bellow present a data simple of each trajectory. The data presented in the figure are just the vehicle speed, the road speed limit and the battery SoC.
![Data collection system](./figures/speed_profiles.png)

# References
* NaitMalek, Y., Najib, M., Bakhouya, M., & Essaaidi, M. (2021). Multivariate deep learning approach for  electric vehicle speed forecasting. Big Data Mining and Analytics, 4(1), pp. 56-64. [https://doi.org/10.26599/BDMA.2020.9020027](https://doi.org/10.26599/BDMA.2020.9020027).
* NaitMalek, Y., Najib, M., Bakhouya, M., Gaber, J., & Essaaidi, M. (2022). Embedded Real-time Speed Forecasting for Electric Vehicles: A Case Study on RSK Urban Roads. IEEE Access, vol. 10, pp. 126412-126428. [https://doi.org/10.1109/ACCESS.2022.3225643](https://doi.org/10.1109/ACCESS.2022.3225643)
* NaitMalek, Y., Najib, M., Lahlou, A., Bakhouya, M., Gaber, J., & Essaaidi, M. (2022). A Hybrid Approach for State-of-Charge Forecasting in Battery-Powered Electric Vehicles. Sustainability, 14(16), 9993. [https://doi.org/10.3390/su14169993](https://doi.org/10.3390/su14169993).


# License
This data-set is under the [CC-BY-4.0 license](./LICENSE.md).
