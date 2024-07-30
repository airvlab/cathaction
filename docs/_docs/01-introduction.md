---
title: "Introduction"
permalink: /docs/introduction/
excerpt: "CathAction-A Benchmark for Endovascular Intervention Understanding."
redirect_from:
  - /theme-setup/
toc: true
---
We present CathAction, a large-scale dataset for endovascular intervention.

<p align="center">
  <img src="/assets/images/TMI_intro.png" alt="samples" style="width: 100%;" />
</p>

## Data Collection
<p align="center">
  <img src="/assets/images/TMI_collect_phantom.png" alt="data_pipeline" style="width: 49%;" />
  <img src="../../assets/images/TMI_scanner_collect.png" alt="data_pipeline" style="width: 49%;" />
</p>

The data were collected using a human silicon phantom in a operating room.

## Dataset Comparison
<p align="center">
  <img src="/assets/images/TMI-dataset-comparison.png" alt="dataset_comparison" style="width: 100%;" />
</p>

CathAction represents one of the largest dataset specifically tailored for catheter and guidewire tasks.

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
