# Lidar-Landsat-data-fusion
A collection of R scripts to import, manipulate and sample iteratively large-scale Lidar and Landsat data

## Table of Contents

1. [Introduction](#Introduction)<a name="Introduction"></a>
2. [Rationale](#Rationale)
3. [What does it do](#Learning_outcomes)
4. [Development team](#Development_team)
5. [Key documents](#Key_documents)
6. [Licenses](#Licenses)

## Introduction

Welcome to Lidar-Landsat-data-fusion repository!. Here you can find important information on the development and use of the repository, including the latest updates to the content. This repository has been developed as a part of the project: "Scaling up monitoring effort of restored forest habitats from sites to landscapes in a megadiverse country". This project was made possible by a grant from Microsoft’s [AI for Earth program](https://www.microsoft.com/en-us/ai/ai-for-earth). AI for Earth is a $50M, 5-year program that brings the full advantage of Microsoft technology to those working to solve global environmental challenges.

**STATUS**: LIVE

The first release for this repository has been published on Zenodo: [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.1434288.svg)](https://doi.org/10.5281/zenodo.1434288)

Feedback and contributions of any form are welcomed. If you feel that any control flow constructs or piece of code can be improved and/or optimized, feel free to [contact us](https://github.com/jmrmcode) and contribute.

## Rationale <a name="Rationale"></a>

Airborne light detection and ranging (lidar) data have great potential to map vegetation structure at a fine resolution, including estimating carbon stocks, canopy closure, and tree height. While airborne lidar-derived vegetation structural measurements could play an important role in ecological restoration monitoring, these data are limited to only a tiny fraction of the earth’s surface. Data fusion to combine high-resolution lidar data with medium resolution satellite data (such as Landsat imagery) represents one way to extend the spatial and temporal reach of airborne data. This repository will provide the necessary workflow required for iteratively importing, manipulating and sampling large-scale Lidar and Landsat data for the purpose of a subsequent fusion between Lidar-derived canopy height data and Landsat-derived vegetation indices.

## What does it do<a name="Learning_outcomes"></a>

- Import and unpack Lidar images from the [G-LiHT NASA server](https://glihtdata.gsfc.nasa.gov/).
- From [Amazon Web Services](https://registry.opendata.aws/landsat-8/) public data sets, access to Landsat 8 images that spatially overlap with the Lidar images.
- Randomly extract and export points sampled from 1x1 m Lidar pixels nested in 30x30 m Landsat pixels according to the following design:
![Sampling design](https://github.com/jmrmcode/Lidar-Landsat-data-fusion/blob/master/general.png)
*Legend: Lidar image of canopy height acquired at NASA's G-LiHT Data Center (background image); 30x30 m Landsat pixels (in purple); 50 meters buffer to discard missing data (outer line in red); Landsat pixels reduced by 5 m (in green) to avoid edge effect. Sampling points (in orange).*

- Request and import Landsat-derived vegetation indices from [Google Earth Engine](https://earthengine.google.com/) using the points sampled earlier.
- Extract Lidar-derived canopy height data using the points sampled earlier.

## Development team <a name="Development_team"></a>

- [Juan Miguel Requena Mullor](https://github.com/jmrmcode), Boise State University, USA.
- [Trevor Caughlin](http://www.trevorcaughlin.com/), Boise State University, USA.

## Key documents <a name="Key_documents"></a>

[Import&UnpackLidarImages](Import&UnpackLidarImages) - Import and unpack Lidar images
[]() - 
