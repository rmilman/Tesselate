# Tesselate
A pattern generating program


Tesselate FAQ

What does Tesselate do?
	It automatically generates seamless patterns for use in photoshop or design.

What do kind of things can tesselate?
	Only some shapes tesselate perfectly with no space in between, but Tesselate 
	can handle any image. It work by minimizing the distance between objects or minimizing the range of the space between two objects. 

Can I add my input if I don't like how it tesselates?
	Yes! You can specify a few features like minimim/maximum gap, how many different tesslations you you want, whether you allow scaling, rotations, and reflections. 
	You may also specify canvas size. If any of these aren't specified, they revert to defaults. If you are in a hurry, the algorithm also has a iteration limit.

How many images can I give Tesselate?
	Technically, as many as you want, but more images will take longer to generate a pattern. 

Tesselate Structure

Tesselate:
	Parses user commands and calls the other objects. Keeps track of images you already loaded as a list of filepaths to them. This list can be added to or subtracted from after initialization. You can "save work" but serializing the Tesselate object, but this is probably not worth it unless you have many images. 

ImageDraw: 
	Uses Java's StdDraw to put all the inputed images into the right places to form the image. This output can be saved with a generic name like "tesslate1" or a name you input. It is automatically saved to the place you have Tesselate, but this will soon be updated.

ImageGenerate:
	This does the main work for Tesselate - It tries the allowed transformations (scale, rotate, reflect) on a your requested pattern size. 


