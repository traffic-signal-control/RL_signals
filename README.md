# Reinforcement Learning for Traffic Signal Control

The aim of this repository is to offering comprehensive **dataset**, **simulator**, relevant **papers** and **survey** to anyone who may wish to start investigation or evaluate a new algorithm.



## Table of contents


- [Key paper list](#key-paper-list)
- [Open Datasets](#open-datasets)
- [Traffic Simulator](#traffic-simulator)
- [A comprehensive survey](#survey)



## Key paper list

<!--### Single intersection

| Method | Paper          | Published | Notes   |
| :------------- | :------------- | :-------- | :-----: |
| MetaLight |  [MetaLight: Value-based Meta-reinforcement Learning for Online Universal Traffic Signal Control]() |AAAI'2020 | |
|DemoLight|[Learning Traffic Signal Control from Demonstrations]() |CIKM'19 | |
| FRAP  | [Learning Phase Competition for Traffic Signal Control]() | CIKM'19 |  |
| IntelliLight|[IntelliLight: A Reinforcement Learning Approach for Intelligent Traffic Light Control]() | KDD'18|First try on RL signal control. The base of all the methods|

### Multi-intersection-->


| Method | Paper          | Published | Notes   |
| :------------- | :------------- | :-------- | :-----: |
| MPLight | [Toward A Thousand Lights: Decentralized Deep Reinforcement Learning for Large-Scale Traffic Signal Control]() | AAAI'2020 | A combination of PressLight and FRAP |
|CoLight |[CoLight: Learning Network-level Cooperation for Traffic Signal Control]() | CIKM'19 | Attention-based coordination| 
|PressLight|[PressLight: Learning Max Pressure Control to Coordinate Traffic Signals in Arterial Network]()|KDD'19| Pressure-based coordination|
| FRAP  | [Learning Phase Competition for Traffic Signal Control]() | CIKM'19 | Our most powerful single intersectiton control model |
| MetaLight |  [MetaLight: Value-based Meta-reinforcement Learning for Online Universal Traffic Signal Control]() |AAAI'2020 | Meta learning for universal traffic signal control |
|DemoLight|[Learning Traffic Signal Control from Demonstrations]() |CIKM'19 | Learn for demonstrations |
| IntelliLight|[IntelliLight: A Reinforcement Learning Approach for Intelligent Traffic Light Control]() | KDD'18|First try on RL signal control. The base of all the methods|


## Open datasets


<table class="table">
              <caption>All methods are measured in <a href="https://traffic-signal-control.github.io/TSCC2019/evaluation.html"> Average Travel Time</a> (in seconds).</caption>
              <thead>
                <tr>
                  <th>#</th>
                  <th>Name</th>
                  <th>Number of intersections</th>
                  <th>Referred Result</th>
                  <th>Refered method</th>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <th scope="row">1</th>
                  <td>hangzhou_1x1_bc-tyc_18041607_1h</td>
                  <td> 1 </td>
                  <td> 221.03 </td>
                  <td>  SOTL </td>
                    
                </tr>
                <tr>
                  <th scope="row">2</th>
                  <td>hangzhou_1x1_bc-tyc_18041608_1h</td>
                  <td> 1 </td>
                  <td> 334.72 </td>
                  <td> SOTL </td>
                </tr>
                <tr>
                  <th scope="row">3</th>
                  <td>hangzhou_1x1_bc-tyc_18041610_1h</td>
                  <td> 1 </td>
                  <td> 213.20 </td>
                  <td> SOTL </td>
                </tr>
                <tr>
                  <th scope="row">4</th>
                  <td>hangzhou_1x1_kn-hz_18041607_1h</td>
                  <td> 1 </td>
                  <td>  72.48 </td>
                  <td> SOTL </td>
                </tr>
                
                <tr>
                  <th scope="row">5</th>
                  <td>hangzhou_1x1_kn-hz_18041608_1h</td>
                  <td> 1 </td>
                  <td> 64.10 </td>
                  <td> SOTL  </td>
                </tr>
                
                <tr>
                  <th scope="row">6</th>
                  <td>hangzhou_4x4_gudang_18041610_1h</td>
                  <td> 16 </td>
                  <td> 240.97 </td>
                  <td> MaxPressure </td>
                </tr>
              </tbody>
            </table>



## Traffic simulator
We built our own simulator, **CityFlow**. 

CityFlow is an opensourced multi-thread traffic simulator, fast and light.

[Project website](https://github.com/cityflow-project/CityFlow)   
[Documentation and quick start](https://cityflow.readthedocs.io/en/latest/) 


<img src="https://user-images.githubusercontent.com/44251346/62375390-c9e98600-b570-11e9-8808-e13dbe776f1e.gif" width="400" />



<!--| Paper          | Published | Notes   |
| :------------- | :-------- | :-----: |
|[CityFlow: A Multi-Agent Reinforcement Learning Environment for Large Scale City Traffic Scenario](https://arxiv.org/abs/1905.05217) | WWW'19 Demo| Simulator |
-->

 
## Survey

[A Survey on traffic signal control]()

All Relative paper list










## How to contribute



## Team


