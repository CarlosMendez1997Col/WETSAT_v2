<h1 align="center">

  [![Typing SVG](https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=20&pause=500&color=F1F4F7&center=true&vCenter=true&multiline=true&width=550&height=80&lines=Welcome+to+WetSAT-ML;By+Stockholm+Environment+Institute+(SEI))](https://git.io/typing-svg) 
</h1>

<div align="center">
<table>
<tr>
<!-- Imagen izquierda -->
<td>
<img src="https://github.com/CarlosMendez1997Sei/WETSAT/blob/main/WETSAT-ML_icon.png" alt="Logo WetSAT-ML" width="120">
</td>
<!-- Texto central -->
<td align="center" style="vertical-align: middle; padding-left: 18px; padding-right: 18px; text-align: center;">
<!-- Título en Markdown dentro del HTML -->
<h1 style="margin-bottom: 6px; text-align: center;">
WetSAT-ML Version 2.0
</h1>
<!-- Frase original abajo --> <span style="font-size: 18px;">
<strong>W</strong>etlands flooding <strong>e</strong>xtent and
<strong>t</strong>rends using <strong>SAT</strong>ellite data and
<strong>M</strong>achine <strong>L</strong>earning Version 2.0</span>
</td>
<!-- Imagen derecha -->
<td>
<img src="https://github.com/CarlosMendez1997Sei/WETSAT/blob/main/LOGO_SEI.png" alt="Logo SEI" width="120">
</td>
</tr>
</table>
</div>

## Description and Methodology

WetSAT-ML 2.0 (Wetlands flooding extent and trends using SATellite data and Machine Learning) is an open-source in Google Colab package developed by SEI Latin America. It enables monitoring of wetland flooding dynamics using
Sentinel-1 radar imagery combined with machine learning algorithms.

<div class="figure" style="text-align: left">
<img src="https://github.com/sei-latam/WETSAT/blob/main/Methodology.png" alt="Figure 1. WetSAT-ML methodology workflow for generating wetland flooding extent and trends using Sentinel-1 data and machine learning." width="100%" />
<p class="caption">
Figure 1. WetSAT-ML methodology workflow for generating wetland flooding
extent and trends using Sentinel-1 data and machine learning.
</p>
</div>

The tool WETSAT_v2 allow users to:

- Generate wetland flooding extent maps.
- Produce water permanence maps.
- Extract flooded area time series.
- Quantify intra-annual and inter-annual wetland hydrological trends.

WetSAT-ML uses Sentinel-1 Synthetic Aperture Radar (SAR) data to map water extent, overcoming the limitations of optical data, which often fail in cloudy or dense vegetation conditions.

The algorithm combines radar backscatter from VV and VH polarizations with five radar-derived indices:

| Index | Formula |
|----|----|
| **PR - Polarized Ratio** | σ<sub>VH</sub><sup>0</sup> / σ<sub>VV</sub><sup>0</sup> |
| **NDPI - Normalized Difference Polarized Index** | (σ<sub>VV</sub><sup>0</sup> − σ<sub>VH</sub><sup>0</sup>) / (σ<sub>VV</sub><sup>0</sup> + σ<sub>VH</sub><sup>0</sup>) |
| **NVHI - Normalized VH Index** | σ<sub>VH</sub><sup>0</sup> / (σ<sub>VV</sub><sup>0</sup> + σ<sub>VH</sub><sup>0</sup>) |
| **NVVI - Normalized VV Index** | σ<sub>VV</sub><sup>0</sup> / (σ<sub>VV</sub><sup>0</sup> + σ<sub>VH</sub><sup>0</sup>) |
| **RVI - Radar Vegetation Index** | 4 · σ<sub>VH</sub><sup>0</sup> / (σ<sub>VV</sub><sup>0</sup> + σ<sub>VH</sub><sup>0</sup>) |

These indices characterize the scattering behavior of radar signals
under different wetland flooding conditions, enabling pixel-level water
detection.


<h2 align="center">
  
Master Script Code from Google Colab </a> <a href="https://colab.research.google.com/github/CarlosMendez1997Sei/WETSAT_v2/blob/main/2_Modelling_WETSAT_Google_Colab/Wetsat_Geoprocessing.ipynb" target="_blank" rel="noreferrer"> 
<img width="20" height="20" alt="image" src="https://uxwing.com/wp-content/themes/uxwing/download/brands-and-social-media/google-colab-icon.png" />
</h2>
  
```html
https://colab.research.google.com/github/CarlosMendez1997Sei/WETSAT_v2/blob/main/2_Modelling_WETSAT_Google_Colab/Wetsat_Geoprocessing.ipynb
```
## Use and install this repository

HTTPS
```html
https://github.com/sei-latam/WETSAT_v2.git
```

GitHub SSH
```html
git@github.com:sei-latam/WETSAT_v2.git
```

GitHub CLI
```html
gh repo clone sei-latam/WETSAT_v2
```
GitHub Codespaces

<a href='https://codespaces.new/sei-latam/WETSAT_v2?quickstart=1'><img src='https://github.com/codespaces/badge.svg' alt='Open in GitHub Codespaces' style='max-width: 100%;'></a>

## Libraries, Datasets and Frameworks

<h2 align="left">
  
![Static Badge](https://img.shields.io/badge/Google_Colab-darkorange) </a> <a href="https://colab.research.google.com/" target="_blank" rel="noreferrer"><img width="40" height="40" alt="image" src="https://uxwing.com/wp-content/themes/uxwing/download/brands-and-social-media/google-colab-icon.png" />
</h2>

```Python
###################################### Artificial Intelligence Frameworks #####################################################
# scikit-learn Framework
!pip install scikit-learn
###################################### Data, Geoprocessing and Graphics libraries #####################################################
!pip install rasterio
!pip install matplotlib
!pip install numpy
!pip install contextily
```

<h2 align="left">
  
![Static Badge](https://img.shields.io/badge/ScikitLearn-blue) </a><a href="https://scikit-learn.org/" target="_blank" rel="noreferrer"><img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" alt="scikit_learn" width="40" height="40"/> 
</h2>

```Python
from sklearn.ensemble import RandomForestClassifier
from sklearn.model_selection import GridSearchCV
from sklearn.model_selection import train_test_split
from sklearn.metrics import classification_report, confusion_matrix
from sklearn.svm import SVC
```

<h2 align="left">
  
![Static Badge](https://img.shields.io/badge/GitHub-gray) </a><a href="https://github.com/" target="_blank" rel="noreferrer"><img src="https://cdn-icons-png.flaticon.com/512/25/25231.png" alt="tensorflow" width="40" height="40"/> 
</h2>

```html
https://github.com/sei-latam/WETSAT_v2/tree/main/0_Original_Files/aoi1/aoi1/gamma_dB
https://github.com/sei-latam/WETSAT_v2/tree/main/0_Original_Files/aoi1/aoi1/gamma_power
https://github.com/sei-latam/WETSAT_v2/tree/main/0_Original_Files/aoi1/aoi1/points_AOI1_Mask
https://github.com/sei-latam/WETSAT_v2/tree/main/0_Original_Files/aoi1/aoi1/sigma_dB
https://github.com/sei-latam/WETSAT_v2/tree/main/0_Original_Files/aoi1/aoi1/sigma_power
```


## Versions and releases

Version `1.0`

```HTML
https://github.com/sei-latam/WETSAT
```

Version `2.0`

```HTML
https://github.com/sei-latam/WETSAT_v2
```



## Credits and repository of data

The original code, repositories and scripts used in this project, are available at:

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change. Please make sure to update tests as appropriate. 

## License

BSD 3-Clause License

Copyright (c) 2025, Stockholm Environment Institute - Latin America

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, this
   list of conditions and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright notice,
   this list of conditions and the following disclaimer in the documentation
   and/or other materials provided with the distribution.

3. Neither the name of the copyright holder nor the names of its
   contributors may be used to endorse or promote products derived from
   this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

