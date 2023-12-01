# qiskit.visualization.plot\_bloch\_vector

<span id="undefined" />

`plot_bloch_vector(bloch, title='', ax=None, figsize=None, coord_type='cartesian')`

Plot the Bloch sphere.

Plot a sphere, axes, the Bloch vector, and its projections onto each axis.

**Parameters**

*   **bloch** (*list\[double]*) – array of three elements where \[\<x>, \<y>, \<z>] (Cartesian) or \[\<r>, \<theta>, \<phi>] (spherical in radians) \<theta> is inclination angle from +z direction \<phi> is azimuth from +x direction
*   **title** (*str*) – a string that represents the plot title
*   **ax** (*matplotlib.axes.Axes*) – An Axes to use for rendering the bloch sphere
*   **figsize** (*tuple*) – Figure size in inches. Has no effect is passing `ax`.
*   **coord\_type** (*str*) – a string that specifies coordinate type for bloch (Cartesian or spherical), default is Cartesian

**Returns**

A matplotlib figure instance if `ax = None`.

**Return type**

Figure

**Raises**

**ImportError** – Requires matplotlib.

## Example

```python
from qiskit.visualization import plot_bloch_vector
%matplotlib inline

plot_bloch_vector([0,1,0], title="New Bloch Sphere")
```

![../\_images/qiskit.visualization.plot\_bloch\_vector\_0\_0.png](/images/api/qiskit/0.26/qiskit.visualization.plot_bloch_vector_0_0.png) ![../\_images/qiskit.visualization.plot\_bloch\_vector\_0\_1.png](/images/api/qiskit/0.26/qiskit.visualization.plot_bloch_vector_0_1.png)