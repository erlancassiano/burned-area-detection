
<br>
<p align="center">Detection of burned areas using deep learning from satellite images and vectorization.</p>

<p align="center">
  <img height="300" widht="500" src="img/burn.jpg">
</p>

<p  align="center">
• <a  href="#-description">Description</a> •
<a  href="#notebook-notebooks">Notebooks</a> •
</p>

The burned-area-detection project aims to identify and analyze the affected
areas after a fire incident. It allows us to understand incident behavior to
take action shortly.

This project uses public satellite images allowing the study of the affected area's and measure the area affected for futher apllicattions, as enviromental warnings.
The process to identify and vectorize burned area consume a great amount of time and the analist need experience in order to increase the efficiency.
The aim is to process more than 80% of the area in at maximi 1/10 of the usual time a and use the visual experience of the analist to check and refine the delivery.

### Normalized Burn Ratio (NBR)

The Normalized Burn Ratio (NBR) is an index that highlights burnt areas in
large fire zones. The formula combines the near-infrared (NIR) and shortwave
infrared (SWIR) wavelengths.

Healthy vegetation shows a very high reflectance in the NIR, and low
reflectance in the SWIR portion of the spectrum, (see figure below). The
contrary happens for areas destroyed by fire; recently burnt areas show a low
reflectance in the NIR and high reflectance in the SWIR. Therefore, the
normalized difference between the NIR and the SWIR is a good discriminant for
this kind of phenomenon.
<p align="center">
  <img widht="500" src="img/Spectral_responses.jpg">
</p>


### Burn Severity

The difference between the pre-fire and post-fire NBR obtained from the images
is used to calculate the delta NBR. A higher value of dNBR indicates more
severe damage, while areas with negative dNBR values may indicate regrowth
following a fire.

Uses [satproc](https://pypi.org/project/satproc/),
[unetseg](https://github.com/dymaxionlabs/unetseg),
[rioxarray](https://github.com/corteva/rioxarray),
[xarray](https://docs.xarray.dev/en/stable/), and
[geopandas](https://geopandas.org/en/stable/), Python packages.


## 	:notebook: Notebooks

This repository contains a set of Jupyter Notebooks describing the steps for
building a semantic segmentation model based on the U-Net architecture for
detecting burned areas from fires from optical satellite imagery.

1. [Pre-process](pre-process.ipynb): Image and ground truth data preprocessing and dataset generation
2. [Training](training.ipynb): Model training and evaluation
3. [Prediction](prediction.ipynb): Prediction
4. [Post-process](post-process.ipynb): Post-processing of prediction results(refining, visual check and vectorization)
