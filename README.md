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

### For loops in Python

`from random import randint
number = 600
for i in range(0,number):
    x = randint(-20,20)
    y = randint(-20,20)
    z = randint(-20,20)
    bpy.ops.mesh.primitive_monkey_add(location=(x,y,z))
`

