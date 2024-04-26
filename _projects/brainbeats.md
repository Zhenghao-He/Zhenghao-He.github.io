---
layout: page
title: BrainBeats
description: Design and implement a portable single-channel EEG fatigue detection device.
img: assets/img/brainbeats/logo.png 
importance: 1
category: work
related_publications: true
---
<style>
/* CSS 样式定义 */
.container {
  display: flex;
  justify-content: center; /* 水平居中 */
  align-items: center; /* 垂直居中 */
}
</style>

<mark>
Collaborators:
<a href="https://github.com/Symphony-Yang">Jiening Yang</a>, 
<a href="https://github.com/wnksdxwg">Xuelin Ma</a>, 
<a href="https://github.com/Zmdrmyvyg">Zhengmiao Huang</a>, 
<a href="https://github.com/YayueHou">Yayue Hou</a>, 
<a href="https://github.com/GianmarcoFortunelli">Gianmarco</a>
</mark>

>This project was awarded as <a href="https://shcxcy.usst.edu.cn/Index">Shanghai Students' Innovation and Entrepreneurship Training Program</a>. And won the second prize in <a href="https://www.heywhale.com/home/competition/649fbd1be92928a38f0f2f50">2023 AI for Brain Science</a>. You can find more details in our <a href="https://github.com/Zhenghao-He/BrainBeats">Github</a> repository.


Brain fatigue is a common phenomenon that affects people's daily life. Being under fatigue not only easily leads to accidents, but may also have negative impacts on personal health. Therefore, accurate monitoring and timely intervention of individual fatigue status is of great significance for improving work efficiency, ensuring traffic safety, and maintaining physical health.

This work is a portable brain computer interface device used for fatigue detection. The device utilizes brain computer interface technology to study the brain waves of the human body during fatigue and wakefulness. 


    
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/brainbeats/logo.png" title="logo" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The logo of our device(The name brainbeats is inspired by its headphone like appearance).
</div>
The appearance of the device resembles a pair of headphones, ensuring both comfort and portability. Using a single channel post ear electrode for signal acquisition (T7/T8 channels according to international 10-20 system)
<div class="row">
    <div class="col-sm-6 mt-3 mt-md-0 container">
        {% include figure.liquid loading="eager" path="assets/img/brainbeats/appearance.png" title="device appearance" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The appearance of the device.
</div>

We use non-invasive dry electrodes as sampling electrodes. The OPA2333 chip is used as the original analog EEG signal amplifier, and the nRF24LU1 chip is selected as the main control MCU chip. This chip integrates a built-in ADC module, clock generator, and 2.4G RF transmitter, and supports multiple communication protocols. The amplified analog EEG signal is fed into the ADC input of the nRF24LU1 chip, and analog-to-digital conversion is achieved in this chip. The chip wirelessly sends digital data to the matching receiver device, and reads the digital EEG signal on the PC.

<div class="row">
    <div class="col-sm-8 mt-3 mt-md-0 container">
        {% include figure.liquid loading="eager" path="assets/img/brainbeats/circui_ connection_diagram.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The circuit connection design of the device.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0" >
        {% include figure.liquid loading="eager" path="assets/img/brainbeats/example_of bipolar_amplifier.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The bipolar amplifier design of the device.
</div>

We have also designed a front-end interface for this device, which facilitates users to observe their EEG data in real-time and enhances interactivity and fun.
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/brainbeats/frontend1.png" title="frontend image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/brainbeats/frontend3.png" title="frontend image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/brainbeats/frontend2.png" title="frontend image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The frontend of the device(currently, only mobile devices have been developed).
</div>
This project dataset uses data collected by [Tongji Affective Computing Lab](https://github.com/TJ-ACLAB). All members of this project also participated in data collection and preprocessing experiments. Thank you [Yayue Hou](https://github.com/YayueHou) for organizing the dataset. The specific experimental methods and datasets can be downloaded from TJ-ACLAB's Github [repository](https://github.com/TJ-ACLAB/FAT-WAKE).



<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/brainbeats/brainlink/brainlink1.png" title="brainlink image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/brainbeats/emotive/emotiv10.png" title="emotiv image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/brainbeats/umindlite/umindlite10.png" title="umindlite image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/brainbeats/umindsleep/umindsleep6.png" title="umindsleep image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The above figure shows the power spectrum characteristics of the subjects in two states, eyes open and eyes closed, based on EEG data collected from four different EEG devices(BrainLink, Emotiv Epoc+, UMindLite, UMindSleep).
</div>

The dataset for this project is fully open source and can be downloaded using the following instructions:

```
git clone https://github.com/TJ-ACLAB/FAT-WAKE.git
```
