# 3dpart-blender-python

# Learning to create 3d parts with blender using Python

## Source

https://www.youtube.com/watch?v=gVUvnSJ-t3M

## Tips

### Main steps to use Python

Use text editor to add main code

`import bpy`

### Select and Remove objects 

`bpy.ops.object.select_all(action='SELECT')`
`bpy.ops.object.delete(use_global=False)`

### Add objects

`bpy.ops.mesh.primitive_monkey_add(location=(0,0,0))`

### Find and copy code to the script

* Set up the 'info' tab in the right window
* Make actions by hand
* Note the change of code and copy that

### Apply smooth operations to the objects

`bpy.ops.object.shade_smooth()`

### For loops in Python

`from random import randint
number = 600
for i in range(0,number):
    x = randint(-20,20)
    y = randint(-20,20)
    z = randint(-20,20)
    bpy.ops.mesh.primitive_monkey_add(location=(x,y,z))

`
## Create 3D parts 

Functions help:

https://docs.blender.org/api/2.81/bpy.ops.mesh.html

### Add cylinder
bpy.ops.mesh.primitive_cylinder_add(radius=0.0105, 
                                    depth = 0.022,
                                    enter_editmode=False,
                                    location=(0,0,0.045))

### Adds cube with custom size

bpy.ops.mesh.primitive_cube_add(size = 0.012, enter_editmode=True, location=(0, 0, 0.055))

### How to rotate things

1. add radians function

from math import radians

2. Rotate using radians(90)

bpy.ops.mesh.primitive_cylinder_add(radius=0.0025, 
                                    depth = 0.022,
                                    enter_editmode=False,
                                    location=(0,0,0.015),
                                    #align='VIEW',
                                    rotation=(0,radians(90),0))

