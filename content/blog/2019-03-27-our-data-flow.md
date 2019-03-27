---
title: Our data flow
author: Julien Colomb
date: '2019-03-27'
slug: our-data-flow
categories:
  - data_analysis
tags: []
---

# From raw data to reproducible reports

## from raw to anonimised version
In this post, I want to present our data flow. We gathered response from a survey on  the one click survey website.

The data is downloaded as a .txt file (other exports are proposed, but only that one is working correctly, for instance the .csv export gives all values starting with "="). The file is then uploaded on the entreprise github page (private) in the "raw data" folder.

In the metadata folder, we produced a .csv file with correct headers name (i.e. unique, without any special characters & meaningfull).

One R script is reading these files and creating a tidy version of the raw file, a second file filtering entries with activity description and one third file sorting personal data out. This data without personal data but with an unique ID number allowing us to get back to personal data if necessary.
This file is also pushed to OSF to https://osf.io/aku9z/ for fruther use and maybe publication.

## Reproducible reports

We plan on using Rmd files in this website to produce reproducible analysis from the anonimised file (as well as other manual analysis results), and get other outputs from the personal data, to be published on osf.
