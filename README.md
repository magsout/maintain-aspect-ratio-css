# Maintain aspect ratio css

[Demo](https://dl.dropboxusercontent.com/u/92935009/aspect-ratio/index.html)

Maintain fluid aspect ratio with css : image, iframe, element


## How to Use It

1. Install with [Bower](http://bower.io/ "BOWER: A package manager for the web"):
   `bower install maintain-aspect-ratio-css --save-dev`

2. Import the partial in your Sass files

3. Example

	`.ratio` is the main class. You must declare ratio class (example: .ratio--16_9):

	```html
	<div class="ratio ratio--16_9">
		<iframe width="560" height="315" src="//www.youtube.com/embed/4SH6ghURstg" frameborder="0" allowfullscreen></iframe>
	</div>
	```
	
4. Ratio

	```
	//ratio
	.ratio--16_9 {
		@include mr($ratio: 1.77);
	}
	
	//Calculate ratio
 	.example {
 		@include mr($rtWidth : 800px, $rtHeight: 600px);
 	}
 	```
 	
 	```
 	//Compiled :
 	
	.ratio--16_9:before
	{
		padding-top:56.49%;
	}
	
	.example:before
	{
		padding-top:75.18%;
	}	
	```

	
5. Width

Change width and height will adapt automatically to keep aspect ratio

		.test1
		{
			width:20%;
		}
		.test2
		{
			width:30%;
		}
		.test3
		{
			width:50%;
		}
		
		
	<div class="ratio ratio--16_9 test1">
		<iframe width="560" height="315" src="//www.youtube.com/embed/4SH6ghURstg" frameborder="0" allowfullscreen></iframe>
	</div>
	<div class="ratio ratio--16_9 test2">
		<iframe width="560" height="315" src="//www.youtube.com/embed/4SH6ghURstg" frameborder="0" allowfullscreen></iframe>
	</div>
	<div class="ratio ratio--16_9 test3">
		<iframe width="560" height="315" src="//www.youtube.com/embed/4SH6ghURstg" frameborder="0" allowfullscreen></iframe>
	</div>
		

![result](ex.jpg)	
	

## Demo
	1. cd into the `test` folder
	2. launch `index.html`
	3. or  https://dl.dropboxusercontent.com/u/92935009/aspect-ratio/index.html
