!devel /Materials/LinearSoilMaterial float=right width=auto margin=20px padding=20px background-color=#F8F8F8

# LinearSoilMaterial

!description /Materials/LinearSoilMaterial

## Description
A material for computed the shear-wave speed ($v_s$) based on a linear relationship between shear modules ($G$) and
density ($\rho$).

This material defines the shear-wave speed as:

$$
v_s = \sqrt{\frac{G}{\rho}}.
$$

The shear-wave speed may differ for different materials throughout the domain. Materials are defined by "layer ids"
using an elemental AuxVariable that defines a "layer id" for each element within the mesh. Thus, the layer variable
is a required parameter in the input.

Using the "layer id" to determine which value to utilize, this material will compute the shear-wave speed based on
the mapping of layer id to $G$ and $\rho$, as shown in the input snippet below.

!input tests/materials/linear_soil/linear_soil.i block=Materials

!parameters /Materials/LinearSoilMaterial

!inputfiles /Materials/LinearSoilMaterial

!childobjects /Materials/LinearSoilMaterial