---
title: "Introduction"
permalink: /docs/introduction/
excerpt: "CathAction-A Benchmark for Endovascular Intervention Understanding."
redirect_from:
  - /theme-setup/
toc: true
---
We present CathAction, a <strong>large-scale<strong> dataset for endovascular intervention.

<p align="center">
  <img src="../../assets/images/TMI_intro.png" alt="samples" style="width: 100%;" />
</p>

## Data collection setup
<p align="center">
  <img src="../../assets/images/TMI_collect_phantom.png" alt="data_pipeline" style="width: 49%;" />
  <img src="../../assets/images/TMI_scanner_collect.png" alt="data_pipeline" style="width: 49%;" />
</p>

The data collection setup with human silicon phantoms in the operating room

## Dataset Comparison
<p align="center">
  <img src="../../assets/images/TMI-dataset-comparison.png" alt="dataset_comparison" style="width: 100%;" />
</p>

CathAction offers several a large-scale dataset encompassing several endovascular intervention tasks such as segmentation, collision detection, and action understanding. To our knowledge, CathAction represents the largest and most realistic dataset specifically tailored for surgical equipment catheter and guidewire tasks.

## Statistics

<p align="center">
  <img src="../../assets/images/TMI_distribution_class.png" alt="num-samples" style="width: 100%;" />
</p>

<p align="center">
  <img src="../../assets/images/TMI_distribution_Duration.png" alt="num-samples" style="width: 100%;" />
</p>

The distribution of action classes in both animal and phantom data of CathAction illustrates the variety of action segment lengths, showcasing the significant variability in segment duration.

<p align="center">
  <img src="../../assets/images/TMI_box_Statitics.png" alt="pos-tags" style="width: 100%;" />
</p>

The adaptation property of our CathAction datasets shared between the phantom data and the animal data. This distinctive domain gap feature
renders the CathAction dataset a formidable benchmark for evaluating domain adaptation.


## Demonstration
<video width="100%" controls>
  <source src="https://github.com/airvlab/grasp-anything/assets/140178004/7afc471e-385d-4aff-9940-a87fc3fe034e" type="video/mp4">
  Your browser does not support the video tag.
</video>

