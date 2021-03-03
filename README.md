inkscape-chain-paths
===================

An inkscape extension to combine paths. Like really combining path snippets
into longer paths. The stock inkscape path operation "combine" does not do that.
It only creates a single path object consisting of multiple distinct segments.

Many commercial CAD packages create object contours consisting of separate path snippets using adjacent end points. Such objects cannot be used in path operations like "add", "intersect", "difference", as they are technically a set of objects, rather than a single stroke.

This extension forms a longer path from multiple shorter path segments. It is irrelevant if the path segments are separate path objects in inkscape, or if the path segments belong to the same path object.
If two path segments have an end point in common, or if their end points are close together, they are linked together to form a longer path.  It is optional weather the linking end points meld into a single common point, or if an optional straight line ('chain link') fills the gap, if any. The maximum distance for end points is a user setting. Usually a fraction of a millimeter works fine.


Usage
-----
Select multiple pathlike objects. If the status line shows you different object types,
then use "Path -> Object to Path". This is needed as we operate only on paths only. 
Then select "Extensions -> Modify Path -> Chain Paths" to open the settings dialog.
You can choose the maximum endpoint distance for path ends to be linked, and the combination method: snap the points together, or create a linking path segment.

Note, that paths never fork. This means, that if there are three or more path ends at the same location, only two are chained together. The others are left unchanged.


Installation
------------

Copy the two files chain_paths.inx and chain_paths.py into the directory specified at Inkscape Preferences > System: User extensions. After a restart of Inkscape, the new extension will be available.

To get the files, you can right click on the 'RAW' button and use your file managers 'save as' function.
Please check the size of the files. If the chain_paths.inx file is more than 1kb, or has more than 33 lines, you probably saved the webpage containing the file, instead of the file itself.



