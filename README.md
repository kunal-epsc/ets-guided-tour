Library: ngx-guided-tour
Version: 2.0.1
License: MIT

Demo: https://lsqlabs.github.io/ngx-guided-tour/

.....................................................................................................................................................

Original Features:

1) Next Button: Go to next step
2) Back Button: Go to previous step
3) Skip Button: Exit the tutorial
4) Step Counter: Indicates the current step number / Total steps
5) Dialog Box + Greyed out backdrop


New Features:

1) Edit button: For interacting with the application mid workflow.
2) Light and Dark theme support
3) Customization of step dialog box in terms of colors and button positioning


Modified Features:

Since we want to give the user an option to interact with the application during the tour, some of features 
innate to the library have been modified. 

1) Back Button: The back button has been reimplemented. The new back button implementation includes a callback 
	function for performing certain tasks when clicked
2) Step Counter: We are not using the original version of the step counter. Originally the library was handling the step count, but now this is
	handled in the application and then the library code is updated about the changes


Note: 

1) The library has been modified to serve our needs. 
2) We are currently using the latest version of the library.
3) Due to the heavy customizations that has been made, it can be challenging to update the library in the future (It is not impossible, just tedious).
4) Since this is a customized version, we will need think of a way to mantain the library. We can either host it on npm or keep it as a github repository

.....................................................................................................................................................

How it works?


PART 1: 

A basic framework has been added to the source code. This code does the following:

a) Tour Service: This is the main controller and is responsible for handling the workflow.
b) Change Detection: If the user make any changes, let's say in an input field, code has been added to signal the tour service.

----------------------------------

PART 2: 

ngx-guided-tour (customized version)

a) This library can be thought of as the view. 
b) This library does all the heavy lifting and is responsible for displaying the dialog box and the backdrop.

----------------------------------

PART 3:

product-tour.json

a) This is the heart of the whole module and can be considered as the model.
b) When the application boots up, the code looks for this particular file. 
c) If the file is present the option to start the product tour is display and nothing without.

----------------------------------



