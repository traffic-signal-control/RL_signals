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


| Method | Paper          | Published | Notes   | Code | Demo video | Poster|
| :------------- | :------------- | :-------- | :-----: | :-----: | :-----: | :-----: | 
| MPLight | [Toward A Thousand Lights: Decentralized Deep Reinforcement Learning for Large-Scale Traffic Signal Control](https://traffic-signal-control.github.io/a-thousand-lights.html) | AAAI'2020 | A combination of PressLight and FRAP  | - |[Demo](https://chacha-chen.github.io/files/chacha-AAAI2020.pdf) | -|
|CoLight |[CoLight: Learning Network-level Cooperation for Traffic Signal Control](https://sites.psu.edu/huawei/2019/09/15/colight-cikm-2019/) | CIKM'19 | Attention-based coordination| [Code](https://github.com/wingsweihua/colight) | N/A | [poster](https://github.com/traffic-signal-control/RL_signals/blob/master/posters/CIKM19-colight-poster.pdf)|
|PressLight|[PressLight: Learning Max Pressure Control to Coordinate Traffic Signals in Arterial Network](https://sites.psu.edu/huawei/2019/06/17/presslight-kdd-2019/)|KDD'19| Pressure-based coordination| [Code](https://github.com/wingsweihua/presslight) |[Demo](https://www.kdd.org/kdd2019/accepted-papers/view/presslight-learning-max-pressure-control-for-signalized-intersections-in-ar) | [poster](https://github.com/traffic-signal-control/RL_signals/blob/master/posters/KDD19-presslight-poster.pdf) |
| FRAP  | [Learning Phase Competition for Traffic Signal Control](http://www.personal.psu.edu/~gjz5038/paper/cikm2019_frap/cikm2019_frap_paper.pdf) | CIKM'19 | Our most powerful single intersectiton control model | [Code](https://github.com/gjzheng93/frap-pub) | N/A |[poster](https://github.com/traffic-signal-control/RL_signals/blob/master/posters/cikm2019_frap.pdf)|
| MetaLight |  MetaLight: Value-based Meta-reinforcement Learning for Traffic Signal Control |AAAI'2020 | Meta-RL for traffic signal control | [Code](https://github.com/zxsRambo/metalight) |-|-|
|DemoLight|[Learning Traffic Signal Control from Demonstrations](https://dl.acm.org/citation.cfm?id=3357384.3358079) |CIKM'19 | Learn from expert demonstrations | [Code](https://github.com/xyh97/DemoLight) |N/A| [poster](https://github.com/traffic-signal-control/RL_signals/blob/master/posters/cikm-demolight.pdf)|
| IntelliLight|[IntelliLight: A Reinforcement Learning Approach for Intelligent Traffic Light Control](https://www.kdd.org/kdd2018/accepted-papers/view/intellilight-a-reinforcement-learning-approach-for-intelligent-traffic-ligh) | KDD'18|First try on RL signal control. The base of all the methods| N/A | [Demo](https://www.kdd.org/kdd2018/accepted-papers/view/intellilight-a-reinforcement-learning-approach-for-intelligent-traffic-ligh)|[poster](https://github.com/traffic-signal-control/RL_signals/blob/master/posters/KDD18-intelliLight.pdf) |
| CityFlow |[CityFlow: A Multi-Agent Reinforcement Learning Environment for Large Scale City Traffic Scenario](https://arxiv.org/abs/1905.05217) | WWW'19 Demo| Simulator | [Code](https://github.com/cityflow-project/CityFlow)| [Demo](https://cityflow-project.github.io/) | N/A |


## Open datasets

We provide different traffic datasets, each includes both road network (roadnet.json) and traffic flow file (flow.json), whose formats are defined in [Roadnet File Format](https://cityflow.readthedocs.io/en/latest/roadnet.html) and [Flow File Format](https://cityflow.readthedocs.io/en/latest/flow.html) respectively.


 <section class="content-section " id="datasets">

<div class="container">

<div class="caption-content">

</div>

<div class="table-responsive" data-example-id="simple-table" style="overflow:scroll;">

<table class="table">

<caption>*All methods are measured in <a href="https://traffic-signal-control.github.io/TSCC2019/evaluation.html"> Average Travel Time</a> (in seconds) under <a href="https://cityflow-project.github.io/"> CityFlow</a> simulator.</caption>

<thead>

<tr>

<th>#</th>

<th>Dataset name</th>

<th>  
Number of  
Intersections  
</th>

<th>Time Span  
(Seconds)</th>

<th>Description</th>

<th>Referred result*</th>

<th>Referred method</th>

</tr>

</thead>

<tbody>

<tr>

<td>1</td>

<td><a
              href="https://github.com/traffic-signal-control/sample-code/tree/master/data/hangzhou_1x1_bc-tyc_18041607_1h"><span>hangzhou_1x1_bc-tyc_18041607_1h</span></a></td>
<td>1</td>

<td>3600</td>

<td rowspan="11">These datasets are based on camera data in Hangzhou.  
Due to the lack of records about turning vehicles, the turning ratios of each dataset are fixed, with 10% as turning left, 60% as going straight, and 30% as turning right. The turning-right vehicles are discarded since they are not under the control of traffic lights.  
There are one left-turn lane and one straight lane in each direction in each roadnet.</td>

<td>221.03</td>

<td ><a class="nav-link js-scroll-trigger" href="https://traffic-signal-control.github.io/code.html">SOTL</a></td>

</tr>

<tr height="30">

<td>2</td>
<td><a 
href="https://github.com/traffic-signal-control/sample-code/tree/master/data/hangzhou_1x1_bc-tyc_18041608_1h"><span>hangzhou_1x1_bc-tyc_18041608_1h</span></a></td>
    
<td>1</td>

<td>3600</td>

<td>334.72</td>

<td ><a class="nav-link js-scroll-trigger" href="https://traffic-signal-control.github.io/code.html">SOTL</a></td>

</tr>

<tr height="30">

<td>3</td>
<td>
                      <a href="https://github.com/traffic-signal-control/sample-code/tree/master/data/hangzhou_1x1_bc-tyc_18041610_1h"><span >hangzhou_1x1_bc-tyc_18041610_1h</span></a></td>

<td>1</td>

<td>3600</td>

<td>213.20</td>

<td ><a class="nav-link js-scroll-trigger" href="https://traffic-signal-control.github.io/code.html">SOTL</a></td>

</tr>

<tr height="30">

<td>4</td>

<td><a href="https://github.com/traffic-signal-control/sample-code/tree/master/data/hangzhou_1x1_kn-hz_18041607_1h"><span>hangzhou_1x1_kn-hz_18041607_1h</span></a></td>

<td>1</td>

<td>3600</td>

<td>72.48</td>

<td ><a class="nav-link js-scroll-trigger" href="https://traffic-signal-control.github.io/code.html">SOTL</a></td>

</tr>

<tr height="30">

<td>5</td>

<td><a href="https://github.com/traffic-signal-control/sample-code/tree/master/data/hangzhou_1x1_kn-hz_18041608_1h"><span>hangzhou_1x1_kn-hz_18041608_1h</span></a></td>

<td>1</td>

<td>3600</td>

<td>64.10</td>

<td ><a class="nav-link js-scroll-trigger" href="https://traffic-signal-control.github.io/code.html">SOTL</a></td>

</tr>

<tr height="30">

<td>6</td>

<td><a  href="https://github.com/traffic-signal-control/sample-code/tree/master/data/hangzhou_1x1_qc-yn_18041607_1h"><span>hangzhou_1x1_qc-yn_18041607_1h</span></a></td>

<td>1</td>

<td>3600</td>

<td>117.24</td>

<td ><a class="nav-link js-scroll-trigger" href="https://traffic-signal-control.github.io/code.html">SOTL</a></td>

</tr>

<tr height="30">

<td>7</td>

<td><a  href="https://github.com/traffic-signal-control/sample-code/tree/master/data/hangzhou_1x1_qc-yn_18041608_1h"><span>hangzhou_1x1_qc-yn_18041608_1h</span></a></td>

<td>1</td>

<td>3600</td>

<td>131.99</td>

<td ><a class="nav-link js-scroll-trigger" href="https://traffic-signal-control.github.io/code.html">SOTL</a></td>

</tr>

<tr height="30">

<td>8</td>

<td><a href="https://github.com/traffic-signal-control/sample-code/tree/master/data/hangzhou_1x1_sb-sx_18041607_1h"><span>hangzhou_1x1_sb-sx_18041607_1h</span></a></td>
<td>1</td>

<td>3600</td>

<td>173.85</td>

<td ><a class="nav-link js-scroll-trigger" href="https://traffic-signal-control.github.io/code.html">SOTL</a></td>

</tr>

<tr height="30">

<td>9</td>

 <td><a
                  href="https://github.com/traffic-signal-control/sample-code/tree/master/data/hangzhou_1x1_sb-sx_18041608_1h"><span>hangzhou_1x1_sb-sx_18041608_1h</span></a></td>
<td>1</td>

<td>3600</td>

<td>290.00</td>

<td ><a class="nav-link js-scroll-trigger" href="https://traffic-signal-control.github.io/code.html">SOTL</a></td>

</tr>

<tr height="30">

<td>10</td>

<td><a href="https://github.com/traffic-signal-control/sample-code/tree/master/data/hangzhou_1x1_tms-xy_18041607_1h"><span>hangzhou_1x1_tms-xy_18041607_1h</span></a></td>

<td>1</td>

<td>3600</td>

<td>214.77</td>

<td ><a class="nav-link js-scroll-trigger" href="https://traffic-signal-control.github.io/code.html">SOTL</a></td>

</tr>

<tr height="30">

<td>11</td>

<td><a href="https://github.com/traffic-signal-control/sample-code/tree/master/data/hangzhou_1x1_tms-xy_18041608_1h"><span>hangzhou_1x1_tms-xy_18041608_1h</span></a></td>
<td>1</td>

<td>3600</td>

<td>325.32</td>

<td ><a class="nav-link js-scroll-trigger" href="https://traffic-signal-control.github.io/code.html">SOTL</a></td>

</tr>

<tr height="30">

<td>12</td>

<td><a  href="https://github.com/traffic-signal-control/sample-code/tree/master/data/syn_1x1_uniform_200_1h"><span>syn_1x1_uniform_200_1h</span></a></td>
<td>1</td>

<td>3600</td>

<td rowspan="3">These datasets are generated artificially. The vehicles enter the road network uniformly with a fixed entering ratio chosen from 200, 400 and 600 vehicles per hour.</td>

<td>61.44</td>

<td ><a class="nav-link js-scroll-trigger" href="https://traffic-signal-control.github.io/code.html">SOTL</a></td>

</tr>

<tr height="30">

<td>13</td>

<td><a
                  href="https://github.com/traffic-signal-control/sample-code/tree/master/data/syn_1x1_uniform_400_1h"><span>syn_1x1_uniform_400_1h</span></a></td>

<td>1</td>

<td>3600</td>

<td>133.40</td>

<td ><a class="nav-link js-scroll-trigger" href="https://traffic-signal-control.github.io/code.html">SOTL</a></td>

</tr>

<tr height="30">

<td>14</td>

<td><a
                  href="https://github.com/traffic-signal-control/sample-code/tree/master/data/syn_1x1_uniform_600_1h"><span>syn_1x1_uniform_600_1h</span></a></td>

<td>1</td>

<td>3600</td>

<td>189.11</td>

<td ><a class="nav-link js-scroll-trigger" href="https://traffic-signal-control.github.io/code.html">SOTL</a></td>

</tr>

<tr height="30">

<td>15</td>

<td><a
                  href="https://github.com/traffic-signal-control/sample-code/tree/master/data/hangzhou_4x4_gudang_18010207_1h"><span>hangzhou_4x4_gudang_18010207_1h</span></a></td>
<td>16</td>

<td>3600</td>

<td>The road network contains 16 intersections in a 4x4 grid. Each intersection has four incoming approaches and four outgping approaches, and each approach has three lanes (left-turn, through and right-turn respectively).  
The traffic flow data is based on camera data in Hangzhou. Necessary simplification is done due to the low quality of the real-world data.  
• Traffic volume: the traffic volume is derived from camera data at Hangzhou.  
• Turning ratio: 10% (turning left), 60%(going straight) and 30% (turning right). This is synthesized from the statistics of taxi GPS data.</td>

<td>240.97</td>

<td>MaxPressure</td>

</tr>

<tr height="30">

<td>16</td>

 <td><a
                  href="https://github.com/traffic-signal-control/sample-code/tree/master/data/syn_1x3_gaussian_500_1h"><span>syn_1x3_gaussian_500_1h</span></a></td>
<td>3</td>

<td>3600</td>

<td rowspan="4">The road network contains 16 intersections in a 4x4 grid. Each intersection has four incoming approaches and four outgping approaches, and each approach has three lanes (left-turn, through and right-turn respectively).  
• Traffic volume: All the vehicles enter and leave the network from the rim edges.For each entering edge, the number of the vehicles generated is sampled from a Gaussian distribution with mean as 500 vehicles/hour/lane.  
• Turning ratio: 10% (turning left), 60%(going straight) and 30% (turning right)</td>

<td>422.95</td>

<td>MaxPressure</td>

</tr>

<tr height="30">

<td>17</td>

<td><a
                  href="https://github.com/traffic-signal-control/sample-code/tree/master/data/syn_2x2_gaussian_500_1h"><span>syn_2x2_gaussian_500_1h</span></a></td>
<td>4</td>

<td>3600</td>

<td>477.71</td>

<td>MaxPressure</td>

</tr>

<tr height="30">

<td>18</td>

<td><a  href="https://github.com/traffic-signal-control/sample-code/tree/master/data/syn_3x3_gaussian_500_1h"><span>syn_3x3_gaussian_500_1h</span></a></td>
<td>9</td>

<td>3600</td>

<td>631.75</td>

<td>MaxPressure</td>

</tr>

<tr height="30">

<td>19</td>

 <td><a
                  href="https://github.com/traffic-signal-control/sample-code/tree/master/data/syn_4x4_gaussian_500_1h"><span>syn_4x4_gaussian_500_1h</span></a></td>
<td>16</td>

<td>3600</td>

<td>689.68</td>

<td>MaxPressure</td>

</tr>

</tr>

<tr height="30">

<td>20</td>

 <td>Manhattan</td>
 <td>2510</td>

<td>3600</td>

<td></td>
<td></td>
<td></td>

</tr>

</tbody>

</table>

</div>

</div>

</section>



## Survey

[A Survey on traffic signal control](https://arxiv.org/abs/1904.08117)



<!--## How to contribute
-->


## Team

- [Zhenhui Jessie Li](https://faculty.ist.psu.edu/jessieli/Site/index.html) (Associate professor, Penn State)
- [Hua Wei](http://personal.psu.edu/hzw77/index.html) (PhD, Penn State University)
- [Guanjie Zheng](http://www.personal.psu.edu/~gjz5038/) (PhD, Penn State University)
- [Chacha Chen](https://chacha-chen.github.io/) (PhD, Penn State University)
- [Nan Xu](https://sites.google.com/site/xunannancy/home) (PhD, University of Southern California)
- [Yuanhao Xiong](https://xyh97.github.io/) (PhD, University of Los Angelos)
- Kan Wu (PhD, Penn State University)
- Xinshi Zang (Bachelor, Shanghai Jiao Tong University)
- Huichu Zhang (PhD, Shanghai Jiao Tong University)
- Jie Feng (PhD, Tsinghua University)


