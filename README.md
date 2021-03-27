# nostalgia-box
An extension of the neural style algorithm

This is a prototype of an extension on the paper A Neural Algorithm of Artistic Style by Leon A. Gatys, Alexander S. Ecker, and Matthias Bethge.  Nostalgia Box is a continually shifting soup of it's user's memories.  Images, curated by the user for their nostalgic emotional impact, and dreamed over one another using a neural style algorithm.  The resulting images are then overlaid into a video which never fully solidifies into any one image, but instead is always several at once.  The user themselves are able to recognize what they see, but after losing track of what images they've entered, should lose their certainty in their identifications.  A stranger should see only a haze of vague shapes which occasionally contains the suggestion of a face.  This is machine learning, stripped of the elements of spam.  You controlled what information went into it, you can understand what is being created with it, and no one is trying to sell you anything.  It is usually running at https://nostalgia-box.glitch.me/

It contains 58 images created using https://deepdreamgenerator.com/ .  It uses a Javascript animation to fade through these images.    

Currently, it can be modified via adding and removing images from both the final_order folder, and to the html file.  The speed of the animation, and the extent to which images overlap, can be controlled via variables at the top of the animation.js file.  

No image in this final version is of the original content.  This was created by taking a starter image, and using it as our content image, along with a simple picture of water as our style image.  This image of water can be seen throughout the animation.

This does not, itself, result in a properly obscured image.  Most images in have been run through the deep dream generator 3-4 times.  

The general procedure for adding a new image is to use it as the content image, and the image preceding it as the style image.  Variety in the settings used creates more visually interesting work, but, in general, keeping Enhance, Depth, and Style-Weight all the way up will result in the proper level of obfuscation in fewer iterations.  Vary the style-scale.  The image which is produced should then be used as the new content image, with the previous image as the style again.  One or two more iterations of this process should result in images which look right to complete the fade.  In general, a good fade from one image of pure content to another will require 3-5 images total, to create an appropriately smooth fade.  
Graphic match is an essential part of making the fade from one image to the next turn out smoothly.  Graphic match involves visual elements of one image lining up with visual elements of the next.  

Keep graphic match in mind when choosing the order of your images.  You will want to be certain that all of your images are the same size, and can use the process of cropping and re-sizing images to line up major graphic details.  If image aren’t looking the way you intend for the them to, adding an image from much earlier in the project to your process as a style image can help.  
How it could work:

Ideally, this process wouldn’t need to be done by hand.  The eventual goal of this project is to fully automate the process, such that someone unfamiliar with machine learning could still take advantage of it.   The user should be able to upload a few images, and more at a later time if they so choose, and nostalgia box itself should take care of the rest.

It should maintain a database of images which the user initially uploaded as content, and images which have been generated previously.  It should continually select two images at random, run neural style with one image as the style and the other as the content, return the result to the pile of images, and fade that image in, slowly, over the currently displayed image. 

Nostalgia Box was created by Aubrey Simonson  as a Spring 2018 UROP project 
at the MIT Media Lab with Manuel Cebrian and the Scalable Cooperation group.  
For more information, contact asimonso@mit.edu.
