# MomentTensorSum
### Interactive Moment Tensor Summation code
<figure>
    <img src="https://github.com/chelle0425/MomentTensorSum/assets/128195508/8ebd9f10-9202-45df-8d3e-877ffb60fe85"
         width="836"
         alt="Figure 3. Northwestern North-American seismic deformation">
</figure>

<figure>
    <img src="https://github.com/chelle0425/MomentTensorSum/assets/128195508/7b106463-5cdd-4c51-a63b-f98a7196d3f8"
         width="485"
         alt="Figure 4b. Subplot around the Fairweather-Queen Charlotte Fault region.">
</figure>

https://github.com/chelle0425/MomentTensorSum/assets/128195508/c04ffbf8-6f20-4646-9fc9-6faac54afdd4


## Table of Contents
- [About the Project](#about-the-project)
- [Getting Started](#getting-started)
  - [Installation](#installation)
  - [Usage](#usage)
- [Examples](#examples)
  - [Output](#output)
  - [GMT plotting](#gmt-plotting)
- [To Do](#to-do)
- [Meta](#meta)
  - [Acknowledgments](#acknowledgements)
 
## About the Project
A Jupyter Notebook based on Google Colab that takes in (1) Harvard CMT Moment Tensor information for a given region stored in the user's google drive, (2) basemap image and coordinates of the selected region, (3) an interactively selected "box" (sub-region), (4) an interactively selected earthquake "fault", (5) inputted dip and depth (optional) information of the fault and does the following:
1. Performs Kostrov moment tensor summation for the selected "box" and plots it as a "beach ball" focal mechanism
   * Also calculates the seismic consistency for earthquakes within the "box" - a measure of the similarity of earthquakes within a group (Frohlich & Apperson (1992))
2. Plots a comulative log(frequency)-magnitude plot for the selected "box" with a line of best-fit according to the Gutenberg–Richter law
3. Calculates average strain and velocity rates
   * Outputs surface projection of T-P strain crosses for GMT plotting
   * Unfortunately velocity vectors still rely on the MTTK program for dip information (computed from the summed Kostrov moment tensor) - this code only outputs average velocity rates as magnitudes without vector direction

The program also takes in optional earthquake depth and type filters.

## Getting Started
### Installation
### Usage

## Examples
### Output
Sample Kostrov moment tensor summation output
<figure>
    <img src="https://github.com/chelle0425/MomentTensorSum/assets/128195508/788082fc-e986-43c9-aacc-ee4cfca5f0c7"
         width="358"
         alt="Figure 1. Sample Kostrov moment tensor summation output">
</figure>
<br />
<em>Sample Kostrov moment tensor summation output</em>
<br />
<figure>
    <img src="https://github.com/chelle0425/MomentTensorSum/assets/128195508/c7665819-d190-4150-ab22-e62bfc5c2d1c"
         width="605"
         alt="Figure 2. Frequency-magnitude plots for box 1, box 3, box 12 and
box 13 from my Independent Geophysics Project. See Figure 3 for box directions.">
</figure>
<br />
<em>Sample freqency-magnitude plots with line of best-fit according to the Gutenberg–Richter law</em>

### GMT plotting
This code is best used in conjunction with the Generic Mapping Tools (GMT) for plotting. The following figures are sexamples from my 3rd year Independant Geophysics Project demonstrating ways of which this code can be used to constrain tectonic deformation.

<figure>
    <img src="https://github.com/chelle0425/MomentTensorSum/assets/128195508/8ebd9f10-9202-45df-8d3e-877ffb60fe85"
         width="836"
         alt="Figure 3. Northwestern North-American seismic deformation">
</figure>
<br />
<em>Summed Kostrov moment tensor for each region of coherent deformation presented as "beach ball" focal mechanisms, of the Northwestern North-America region. Numbers by the focal mechanism indicates which box it is associated with, whereas summed moment tensor magnitude can be seen by the size of the focal mechanism. Kostrov summation can be easily performed for each region of coherent deformation using this code.</em>
<br />
<figure>
    <img src="https://github.com/chelle0425/MomentTensorSum/assets/128195508/5463b45a-ae92-4a90-bea8-0d599e628462"
         width="750"
         alt="Figure 4a. Subplot around the Aleutian-Alaskan region.">
</figure>

<figure>
    <img src="https://github.com/chelle0425/MomentTensorSum/assets/128195508/7b106463-5cdd-4c51-a63b-f98a7196d3f8"
         width="485"
         alt="Figure 4b. Subplot around the Fairweather-Queen Charlotte Fault region.">
</figure>

<br />
<em> Purple arrows are velocity vectors, whereas magenta-cyan, red-blue and orange-purple are extensional-compressional (T-P) strain crosses of magnitude 10−7, 10−8 and 10−9 respectively. Grey arrows are plate velocity vectors of the Pacific plate with respect to the NA plate from the MORVEL model of DeMets et al. (2010). Velocity vectors and T-P strain crosses for each region of coherent deformation can be easily computed using this code.</em>
<br /><br />

All of the figures above are produced with the Generic Mapping Tools (GMT) using seismicity from the Harvard CMT catalogue (Dziewonski et al. (1981), Ekstr ̈om et al. (2012), https://www.globalcmt.org/.). Major and minor faults (red) are after Bird (2003) and Styron & Pagani (2020) respectively; whereas slab contours (red in a. and purple in b & c.) are from the slab model of Hayes et al. (2018).




## To Do
### Data-processing improvements
 - Higher-order information from summed Kostrov moment tensor:
    - Dip information originally computed from MTTK
    - Fault slip azimuth information to calculate vector directions for average velocity rates
 
### Migrate from Google Colab to an independent Jupyter Notebook that can be displayed on Binder
 - Taking real-time data directly from the Harvard CMT catalogue and importing them for a selected region
    - Automatically seperate moment tensors into their respective earthquake types
 - Ask for inputed coordinates of a selected region
 - Generating basemap image based on said inputed coordinates
 - Overlapping generated basemap with seismicity from the Harvard CMT catalogue
 - Host this on a website somehow??

### Misc
- Finish the [Getting Started](#getting-started) and [Output](#output) section of the README

## Meta
This project was submitted as part of coursework for the 3rd year undergraduate module *EART60001b Independent Project - Geophysics* in the Department of Earth Science and Engineering at Imperial College London.

This project may be freely copied and distributed provided the source is acknowledged explicitly. Please consult your module coordinator before using this code as part of your coursework.

### Acknowledgements
I would like to thank the Department of Earth Science and Engineering at Imperial College London for providing us with the project requirements, in particular Dr Ian Bastow for providing the module handout and his valuable guidance throughout the project. 

Additionally, this code would not have been possible without guidance from Rebecca Colquhoun from the department and the amazing GTAs for this module, who helped fix crucial bugs and provided helpful comments and feedback.

*Version 1.1*

<rochelle.pun@gmail.com>, 2023
