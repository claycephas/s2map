# s2map

s2map is a simple geo visualizer. [source code on gitbhub](https://github.com/blackmad/s2map).

I find I have one or more lat/lngs, and I want to put them on a map and not worry about formatting, writing a file, etc, so I just paste it into s2map.com

* [example of pasting in a bounding box from some json](http://cl.ly/image/1n2o1p0Y2e0A)
* [using it via url params (doesn't support all the options yet)](http://s2map.com/#40.74,-74,40.75,-74.05)
* [rendering some geojson coordinates in lng/lat format](http://cl.ly/image/1s12263h0X3r)

I'm curious if other people find this useful or have feature suggestions.

Oh, and just for kicks alt/ctrl/meta+click pops up a balloon with lat/lng info.

Additionally, s2map demonstrates the power of google's s2 (spherical geometry library) available for [C++](http://code.google.com/p/s2-geometry-library/) (which doesn't compile publicly, the version in [my github repo](https://github.com/blackmad/s2map) does) and [java](http://code.google.com/p/s2-geometry-library-java/) (in extensive use at [foursquare](http://foursquare.com)). We use it as a very robust geohashing library with a number of great properties (skip-level indexing, prefix parents). Read the code, it's beautiful and well documented and a pretty good intro to the concepts. [Presentaion](https://docs.google.com/presentation/d/1Hl4KapfAENAOf4gv-pSngKwvS_jwNVHRPZTTDzXXn6Q/view?pli=1#slide=id.i0) on the algorithms and features.

* [Generating the default s2 covering for a bounding box](/img/demo/default_covering.png)
* [S2 covering with 100 cells](/img/demo/100cells.png)
* [Polygons work too!](/img/demo/polygon_covering.png)
* [Visualizing some cell ids (tries to guess if you're visualizing cell ids or tokens)](/img/demo/cells.png)


## Running locally

Prerequisites: python 2

From terminal:
```
virtualenv venv
source venv/bin/activate
python app.py
```

Open http://localhost:5000 in your browser