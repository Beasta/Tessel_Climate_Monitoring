# Tessel_Climate_Monitoring
Code for gathering temperature, humidity, light, sound data and sending it to keen.io for storage

##Getting Started
You will need to start by purchasing a tessel or [tessel 2](https://tessel.io/), the [ambient module](https://shop.tessel.io/Modules/Ambient%20Module%20(Light%20and%20Sound)), and the [climate module](https://shop.tessel.io/Modules/Climate%20Module).

Next, setup Git so that you can retrieve the code that will be installed on the Tessel. A good guide for getting Git setup can be found [here](http://burnedpixel.com/blog/setting-up-git-and-github-on-your-mac/). 

After you have the hardware, you will need to get it setup by following the instructions [here](http://start.tessel.io/install). Note that there are different instructions if you are setting up a [tessel 1](http://start.tessel.io/install) versus a [tessel 2](https://tessel.github.io/t2-start/). After you have got to the step of running `tessel update` you are ready to begin following these instructions.

1. Open the terminal and navigate to the desktop or the location you want to place your tessel program. ```cd Desktop`` Note that `cd` means "change directory".

2. Create a folder (also known as a directory) called Tessel. ```mkdir Tessel``` Note that mkdir stands for "make directory" and it creates a folder named after the command that is typed after it, in this case "Tessel".

3. Now that the folder has been created, navigate into it. ```cd Tessel``` 

4. Clone the repository of code for climate monitoring on the tessel. ```git clone https://github.com/Stegosaurius/Tessel_Climate_Monitoring``` This will copy the code found in the weblink and place it in the current folder.

5. Navigate into the newly created folder ```cd Tessel_Climate_Monitoring```

6. (Optional) Display the contents of the current folder ```ls``` This command stands for list and will show you the contents of the current directory.

7. Download all the code dependencies. ```npm install``` This command tells npm to install the code dependencies defined in the package.json file found in the current directory.

8. Make a copy of the keenConfigure.example.js file. ```cp keenConfigure.example.js keenConfigure.js``` The command `cp` stands for copy. It will create a copy of the file given after it `keenConfigure.example.js` to file given as a second command, `keenConfigure.js`. This particular file is where we will store the keys 

