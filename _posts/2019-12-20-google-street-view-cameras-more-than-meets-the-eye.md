---
date: 2019-12-20
title: "Google's Street View Cameras - More Than Meets the Eye"
description: "Street View cameras rigs do much more than just take photos."
categories: updates
tags: [Street View]
author_staff_member: dgreenwood
image: /assets/images/blog/2019-12-20/google-street-view-2017-camera-mounted.jpg
featured_image: /assets/images/blog/2019-12-20/google-street-view-2017-camera-mounted-sm.jpg
layout: post
published: true
---

**Lasers, gyroscopes, accelerometers...**

[Last month I looked at the history of the Street View camera](/blog/2019/history-of-street-view-cameras), from the early versions in 2007, to the drastically improved cameras Google now uses.

Many of you followed up, asking me about the lasers I mentioned fleetingly in that post.

Well, here's more about the lasers, and the many other sensors that make up the Google Street View Camera rigs.

### Positioning

Street View imagery must be associated with accurate positioning.

[Each camera is equipped with a combined DGPS](https://books.google.co.uk/books?id=dGpQDwAAQBAJ&pg=PA83&lpg=PA83) (Digital Global Positioning System) / IMU (Inertial Measurement Unit) system [from Topcon](https://www.topconpositioning.com/mapping), together with a wheel mounted odometer that, in conjunction with the IMU (accelerometers and gyroscopes), can help establish a position where GPS coverage is poor or has been lost in tunnels or within high-rise urban areas.

As part of the Street View processing pipeline, the company uses an open-sourced algorithm they developed, the [Google Pose Optimizer (GPO)](http://code.google.com/p/gpo/wiki/GPO).

The GPO creates a reconstruction of the pose of a sensor platform (i.e. its position and orientation over time) based on information from the sensors.

Once the pose is computed, Google aligns or snaps the pose to a map of the road (or path) network in Google Maps.

### Range

<img class="img-fluid" src="/assets/images/blog/2019-12-20/google-street-view-sick-lms-291.jpg" alt="Google Street View Sick AG LMS 291" title="Google Street View Sick AG LMS 291" />

As mentioned in my [history of the Street View camera](/blog/2019/history-of-street-view-cameras), even the prototype Street View cars had side and front-facing laser scanners installed to measure depth.

[All Street View cameras since the R5 (2008)](https://books.google.co.uk/books?id=dGpQDwAAQBAJ&pg=PA83&lpg=PA83) feature a pair of [$6000 Sick AG LMS 291](https://www.sick.com/gb/en/detection-and-ranging-solutions/2d-lidar-sensors/lms2xx/lms291-s05/p/p109849) laser profilers that are attached to the mast and continually measure a series of range or elevation profiles on either side of the mapping vehicle. A third SICK LMS291 profiler measures the road surface in front of the vehicle.

The laser range scanners, measure up to 50 meters in the front of the vehicle with a 180 degree range. These are used for recording the actual dimensions of the space being photographed, for example the distance was between the camera and the facades of the buildings. 

That spacial recognition is what helps Google patch all of its images together and give them a 3D feel.

### Depth

<img class="img-fluid" src="/assets/images/blog/2019-12-20/google-street-view-lidar-velodyn.jpg" alt="Google Street View LIDAR scanners from Velodyn" title="Google Street View LIDAR scanners from Velodyn" />

<img class="img-fluid" src="/assets/images/blog/2019-12-20/google-street-view-camera-lidar-output.jpg" alt="Google Street View LIDAR render" title="Google Street View LIDAR render" />

LIDAR scanners from Velodyne were added to the latest cameras.

These are the ubiquitous [Velodyne VLP-16 "Puck" sensors](http://velodynelidar.com/products.html), allowing the to car "see" in 3D in 360 degrees. These $8,000 Lidar sensors are most commonly used in autonomous car prototypes

Mounted at 45° to capture 3D depth information, and used for additional positional information.

### Air quality

<img class="img-fluid" src="/assets/images/blog/2019-12-20/google-street-view-aclima-air-quality.jpg" alt="Google Street View Aclima air quality sensors" title="Google Street View Aclima air quality sensors" />

<img class="img-fluid" src="/assets/images/blog/2019-12-20/google-street-view-aclima-air-quality-map.png" alt="Google Street View Aclima air quality map" title="Google Street View Aclima air quality map" />

[In September 2018](https://techcrunch.com/2018/09/12/google-street-view-cars-are-now-roaming-around-the-planet-checking-our-atmosphere-with-these-sensors/), Google announced it would integrate air quality sensors from [Aclima](https://aclima.io/#products) into its global fleet of Street View vehicles.

The Aclima sensors will capture air quality data by generating snapshots of carbon dioxide (CO2), carbon monoxide (CO), nitric oxide (NO), nitrogen dioxide (NO2), ozone (O3), and particulate matter (PM2.5) while the Google cars roam the streets.

## Trek Pack

We believe air quality sensors are really important sensors to keep track of the health of our environment, and are already forming plans to retrofit them to the [Trek Pack](/trek-pack).

Imagine being able to compare air quality at different locations or altitudes on a hike, and on different days or times!

If you know of any cheap, low-powered, yet fairly accurate air quality sensors we could potentially use, [please contact us](/contact).