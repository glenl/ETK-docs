.. index:: Generators; Grid
.. _etk-generators-grid:

*****
 Grid
*****

.. figure:: /images/nodes-grid.png
   :align: right

   The ETK_Grid node.

The **Grid** node outputs a 3D grid. It can be used to create a plane or a
2D grid as well but if a 3D grid is required it can do that. Rather
than a subdivided cube which just has points on the surface, the **Grid**
node will generate points throughout the volume as well.


Inputs
=======

|INTEGER| X Count
    Integer value for number of vertices in the X axis.

|INTEGER| Y Count
    Integer value for number of vertices in the Y axis.

|INTEGER| Z Count
    Integer value for number of vertices in the Z axis.

|VECTOR_FIELD_SINGLE| Size
    The overall size of the grid in metres.

|BOOLEAN_FIELD_SINGLE| Use Spacing
    Toggle to change the **Size** from overall size to the spacing between
    points.

|FLOAT_FIELD_SINGLE| Randomise
    Maximum distance to randomise position by.

|INTEGER_FIELD_SINGLE| Seed
     The seed for the randomisation.

|BOOLEAN_FIELD_SINGLE| Centred
    A toggle to choose if the grid is centred on the origin or aligned
    on the bottom left corner.


Outputs
========

|GEOMETRY| Geometry
    The generated geometry.

|INTEGER| Size
    The total number of points generated.

|FLOAT_FIELD| X Fac
    A 0-1 gradient across the points in the X axis.

|FLOAT_FIELD| Y Fac
    A 0-1 gradient across the points in the Y axis.

|FLOAT_FIELD| Z Fac
    A 0-1 gradient across the points in the Z axis.


Examples
========

.. figure:: /images/nodes-grid_basic.png
   :width: 800
   :align: center

   Instancing cubes on a 3 x 3 **ETK_Grid**.


.. figure:: /images/nodes-grid_basic02.png
   :width: 800
   :align: center

   This example builds a 3D grid out of which some interior instances
   are removed then joined with a cube.
