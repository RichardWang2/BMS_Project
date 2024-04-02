# Streamlined Image Processing for Protein Crystallization

This is a project I collaborated with Bristol Myers Squibb in a Capstone Project during my last semester in Carnegie Mellon University's Masters of Science in Data Analytics program.

## Overview

The end goal of the project is to create a phase diagram that shows the concentration type which inhibits protein crystallization for every protein type. The approach is to use a image classification model to classify a protein as the following classes: **pure crystal, empty drop, clear drop** and **others**. 

**Drop examples**

![image](https://github.com/RichardWang2/BMS_Project/assets/41966482/934357ce-af91-41cb-b091-1710ace811b3)

**Phase Diagram Example**

![image](https://github.com/RichardWang2/BMS_Project/assets/41966482/58b98532-f3f8-420b-83f1-c4118db41a75)

## Phase 1: Droplet Selection

To avoid bias and improve model accuracy, we first use **OpenCV** methods to select the drop portion of the image. We used OpenCV's **findContour** method to select the drop, and then crop the image based on the drop.

**Selection**

![image](https://github.com/RichardWang2/BMS_Project/assets/41966482/2ed52475-45a9-4945-9628-f245d3d1a2fe)

**Crop**

![image](https://github.com/RichardWang2/BMS_Project/assets/41966482/70b8350b-fb1a-4b3b-97a4-ddf8098619f6)


## Phase 2: Model Training (Current Phrase)

We're currently testing different pre-trained models. We only have ~1000 images so we decided to use **transfer learning**. We are in the phase of testing different model from **pytorch**, **huggingface**, etc., and using **tensorboard** for visualizations, monitoring, and parameter tuning.

## Phase 3: Phase Diagram and Report

This will be the final phrase where we organize a phase diagram using the model's predictions, like shown above, and a presentation for the end of semester.
