# lidar_tools

[![Actions Status][actions-badge]][actions-link]

[actions-badge]:            https://github.com/uw-cryo/lidar_tools/workflows/Tests/badge.svg
[actions-link]:             https://github.com/uw-cryo/lidar_tools/actions

Tools to process airborne and satellite LiDAR point clouds

**Warning!** This package is under active development!

## Quickstart

We recommend using [pixi](https://pixi.sh/latest/) to install a locked software environment for executing code in this repository. Once installed, you can run scripts from a terminal:

```bash
git clone https://github.com/uw-cryo/lidar_tools.git
cd lidar_tools
pixi shell
pdal_pipeline notebooks/processing_extent.geojson notebooks/SRS_CRS.wkt notebooks/UTM_13N_WGS84_G2139_3D.wkt /tmp/dem
```

## Installation

By default, pixi only manages dependencies *required* to run scripts in this respository, such as [PDAL](https://pdal.io). However, you might also want to install optional libraries into the same environment such as [GDAL](https://github.com/OSGeo/gdal) command line tools:

```
pixi add gdal
```

Or [Ames Stereo pipeline](https://stereopipeline.readthedocs.io/en/latest/installation.html#conda-intro):
```
pixi project channel add nasa-ames-stereo-pipeline
pixi project channel add usgs-astrogeology
pixi add stereo-pipeline
```

### Using pip

If you already have an environment you can install just the code in this library with pip:

```
pip install git+https://github.com/uw-cryo/lidar_tools.git@main --no-deps
```
