# pa_reconstruction
### Introduction

This is a python implementation of the following paper:

> Xu M, Wang L V. Universal back-projection algorithm for photoacoustic computed tomography[J]. Physical Review E, 2005, 71(1): 016706.

The back-projection algorithm is used for two-dimensional photoacoustic reconstruction. It is extended to the three-dimensional case.

### Getting started

##### Environment

+ python >= 3.5 (numpy, scipy, matplotlib)

+ mayavi is used to visualize the 3d surface. Besides, qt5 is required for mayavi.

  To install both, use

  ```
  pip install mayavi
  pip install PyQt5
  ```

##### Usage

To run the program, use

```
python pa_tom_sim.py [-p]
```

This generates a simulated pa signal and reconstruct it on 2d plane.

By default, it shows the plane with z-axis equals 15mm, which is the center plane of the model. It also shows an amplitude figure along both x and y axis to display the resolution.

To change the z-axis, e.g. set the reconstruction plane at z = 13, use

```
python pa_tom_sim.py -p -t 13
```



To get a 3d reconstruction, use

```
python pa_tom_sim.py -v
```

By default, the range of z-axis is set to 11-19mm, which just contains the model. 

To change the range of z-axis, e.g. , set the range to [9,21], use

```
python pa_tom_sim.py -v -r 9 21
```

You would see some artifacts above and under the big sphere.

