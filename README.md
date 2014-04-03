# rDVR

The rDVR package provides an R wrapper to a REST API for a video server. The REST API is written in JAVA and is a modified version of [VideoRecorderService](https://github.com/tuenti/VideoRecorderService). This video server relies on the screen recorder included in the great Monte Media Library developed by Werner Randelshofer (http://http://www.randelshofer.ch/monte/). It has been modified to run as a background process and record for up-to 10 minutes. An extra method /rec/closeserver has been added to the REST API to enable shutting down of the service. It has been tested on Ubuntu 12.04, Windows 8.1 and OSx 10.9 mavericks. 

### USAGE

Using `rDVR` is straightforward. The main object is a reference class which controls the video service.
There are utility functions to start the service and to download a compiled server.
```
require(rDVR)
startVServer() # utility function to start a video server
DVR <- rDVR()
DVR$start()
# Do your thing for upto 10 minutes
DVR$save()
DVR$closeServer()
```
### Getting started
To install `rDVR` you will need the devtools package. If necessary (install.packages("devtools")) and run:
```
devtools::install_github("rDVR", "johndharrison")
```

### Record Selenium tests

`rDVR` can be used to record your Selenium tests ran with [RSelenium](http://johndharrison.github.io/RSelenium/). Check the sample clip produced with `rDVR` at http://johndharrison.github.io/rDVR/. There is a package vignette available at [rpubs](http://rpubs.com/johndharrison/15176) also.


<iframe width="560" height="315" src="//www.youtube.com/embed/XvVBT-rojz0" frameborder="0" allowfullscreen></iframe>

### Support or Contact

Having trouble with rDVR? We would love to help you at https://github.com/johndharrison/rDVR. File an issue and help us to improve rDVR.