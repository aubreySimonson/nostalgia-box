# nostalgia-box
An extension of the neural style algorithm

This is a prototype of an extension on the paper A Neural Algorithm of Artistic Style by Leon A. Gatys, Alexander S. Ecker, and Matthias Bethge.  Nostalgia Box is a continually shifting soup of it's user's memories.  Images, curated by the user for their nostalgic emotional impact, and dreamed over one another using a neural style algorithm.  The resulting images are then overlaid into a video which never fully solidifies into any one image, but instead is always several at once.  The user themselves are able to recognize what they see, but after losing track of what images they've entered, should lose their certainty in their identifications.  A stranger should see only a haze of vague shapes which occasionally contains the suggestion of a face.  This is machine learning, stripped of the elements of spam.  You controlled what information went into it, you can understand what is being created with it, and no one is trying to sell you anything.  It is running at http://cs.wellesley.edu/~asimonso/nostalgiabox/

It contains 58 images created using Deep Dream Generator.  It uses a Javascript animation to fade through these images.    

Currently, it can be modified via adding additional images to both the final_order folder, and to the html file.  The speed of the animation, and the extent to which images overlap, can be controlled via variables at the top of the animation.js file.  

Ideally, this project will include a it’s own Tensorflow implementation of neural-style, and additional code to maintain a collection of uploaded images, as well as previously generated images, which it will randomly select new content and style images from.  Check back for updates!
