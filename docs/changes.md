## Main changes

### A new web page is avaialble! check it out at

### [https://vedo.embl.es](https://vedo.embl.es)

- python2 is no more supported
- A bug in `mesh.closestPoint(returnIds=True)` has been fixed
- [pymeshlab](https://github.com/cnr-isti-vclab/PyMeshLab) is now interfaced in `vedo`!

---
### `base.py`
- method `addPos()` (obsolete but still valid) renamed to `shift()`
- added shortcut to input the opacity with syntax `mesh.color("blue", 0.5)`
- arrays with name "Normals" are set as active normals automatically ( @theponpon )
- added keyword invert in `getTransform()` ( @Tai-Hsien )


---
### `addons.py`
- added mesh cutter with planes and spheres in addition to boxes ( @nantille )
- major revision of the `Axes` class. with new added feature like axes inversion, free rotations
- keyword `xFlipText` dispaered as is now substituted by `xLabelRotation`
  (this can affect @FedeClaudi @DeepaMahm  @jonnymaserati )
  Added `xyShift` to shift the whole cartesian plane along one axis ( @JGarrett7 )
- Axes can be flipped with their range with `xInverted` (caveat: this does not at all affect the world coordinate system!)


---
### `colors.py`
- `vedo` is now independent of matplotlib for colormaps
- added new bootstrap5 [color scheme](https://user-images.githubusercontent.com/98681/84801339-e5585680-afb3-11ea-8743-29647ff3f3a9.png)
(e.g. `c='red1', 'red2', ..., 'red9'`, or in short: `c='r1', 'r2', ..., 'r9'`)
Lower index means darker.
- added `rgb2hex()` and `hex2rgb()` functions


---
### `mesh.py`
- fixed bug in `splitByConnectivity()` ( @jsanchez679 )
- added method `addConnectivity()` to add a connectivity array to mesh points

---
### `plotter.py`
- improved `resetcam` behaviour
- passing camera no more empties the passed dictionary (thanks @icemtel )
- `verbose` keyword has been removed (as hard to maintain)
- mouse clicking can now pick `Picture` not only `Mesh`
- revised and improved callback functionality with `plotter.addCallback()`
  (see examples `mousehighligh`, `mousehover`)


---
### `picture.py`
- attribute `picture.shape` holds the shape of the picture in pixels


---
### `pointcloud.py`
- added `fitCircle()` to fit a circle to a line in 3D.


---
### `pyplot.py`
- a brand new function `fit()` to perform polynomial fitting to data with error bars in both x and y with correct estimation of error bands via bootstrap method (there are out there soo many wrong scripts in matplotlib!)
- added `pyplot.matrix()` to plot numpy matrices (eg. correlation/covariance matrix)

---
### `shapes.py`
- `Spline` can control the *easing*, the density of points along the line.
- support for closed splines.

---
### `volume.py`
- added `volume.shade()` which can be `True` or `False`. Disable by default (was previously enabled)
  to be used in conjunction with `volume.lighting()` to create a mesh-like rendering of the volume.
  (thanks to @nantille for debugging)


## New/Revised examples:
- `vedo -r colorcubes`
- `vedo -r cutter`
- `vedo -r fitPolynomial1`
- `vedo -r fitPolynomial2`
- `vedo -r spline_ease`
- `vedo -r gyroid`
- `vedo -r align6`
- `vedo -r colormap_list`
- `vedo -r customAxes2`
- `vedo -r customAxes3`
- `vedo -r glyphs3`
- `vedo -r bloch`
- `vedo -r slicePlane1`
- `vedo -r slicePlane2`
- `vedo -r np_matrix`
- `vedo -r pygmsh_cut`
- `vedo -r mousehighlight`
- `vedo -r mousehover`
- `vedo -r line2mesh_quads`
- `vedo -r line2mesh_tri`
- `vedo -r pointsCutMesh2`
- `vedo -r textLegend`
- `vedo -r fitCircle`
- `vedo -r pymeshlab1.py`










