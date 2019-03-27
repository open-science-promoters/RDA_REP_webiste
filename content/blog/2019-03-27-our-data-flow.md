---
title: Our data flow
author: Julien Colomb
date: '2019-03-27'
slug: our-data-flow
categories:
  - data_analysis
tags: []
---

While planning the data analysis, we also planned how and in what format the data will be transformed and made available to the group and later published. 

## From raw to anonimised version
In this post, I want to present our data flow. We gathered response from a survey on  the one click survey website.

The data is downloaded as a .txt file (other exports are proposed, but only that one is working correctly, for instance the .csv export gives all values starting with "="). The file is then uploaded on the entreprise github page (private) in the "01_Raw_Data" folder. (https://ghe.phaidra.org/Engaging-Researchers/data_analysis/tree/master/Data/01_Raw_Data you need to be logged in to access this page).

In the metadata folder, we created a .csv file with computer and human readable headers name (i.e. unique, without any special characters, and meaningfull).

One R script is reading these files and creating a tidy version of the raw file, a second file filtering entries with activity description and one third file sorting personal data out. This last data file has no personal data but contain an unique ID number allowing us to get back to personal data if necessary. It is pushed to the 02_Anonimised_Data folder there and to
 OSF at https://osf.io/aku9z/, for fruther use and maybe publication.

## Reproducible reports

We plan on using Rmd files in this website to produce reproducible analysis from the anonimised file (as well as other manual analysis results), and get other outputs from the personal data, to be published on osf.
