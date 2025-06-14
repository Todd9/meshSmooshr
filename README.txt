meshSmooshr
=========================================
Created 2011
Use and modify freely.

What is it?
A utility to smoosh the vertices of a mesh around in TouchDesigner for projection-mapping alignment.

How is this different from camSchnappr?
camSchnappr is the best tool for mapping when you have a 3D model that would be cumbersome to map one polygon at a time. But it only works well when your physical object to be mapped matches your virtual 3D model. If there are discrepancies then camSchnappr won't produce a good result.

meshSmooshr is a 2D mapping tool that works on 2D and 3D meshes (SOPs). Even if your physical and virtual models are very different, you can freely move vertices around to get an alignment.

It can be more work to set each vertex, but it can guarantee a solution when all else fails.

You can also use camSchnappr to get it close, then use meshSmooshr to tweak the alignment into perfection.

Get TouchOSC here: https://hexler.net/touchosc
and load the provided tosc template.

In order to work, your tablet/phone and computer must be connected to the same network. Find the IP address of your tablet/phone and set it in TouchDesigner (in the parameters of the 'meshSmooshr' node). Then find the IP address of the computer and set it in TouchOSC (under Connections > OSC).  

If you don't know how to find your local IP address just google "find my ip address on the local network"

For phones, google "find my phone's ip address on the local network"

USAGE
The top slider selects the active vertex. Slide it all the way to the left to select nothing and hide the cursor. You can also step through each vertex with the arrow buttons below the slider. The vertex number should update when 2-way communication is working.

The trackpad drags the active vertex around, and the speed is affected by the fine/coarse slider.

The arrow buttons in the lower-left allow you to nudge the vertex one step at a time (also affected by the fine/coarse slider).

"Reset point" returns the vertex to its original position.

MORE NOTES
Vertices are moved in their X/Y plane, so position your camera on the positive Z axis looking toward the origin (like in the example toe file).

It's helpful to start with a view that shows all of your vertices reasonably close to their proper positions, otherwise it's possible to get the mesh tangled and lose track of what is supposed to go where.

After a new SOP is connected to meshSmoosher for the first time, pulse Reset once on the meshSmooshr node's parameters to initialize the model. 