After you have the hardware, you will need to get it setup by following the instructions [here](http://start.tessel.io/install). Note that there are different instructions if you are setting up a [tessel 1](http://start.tessel.io/install) versus a [tessel 2](https://tessel.github.io/t2-start/). After you have got to the step of running `tessel update` you are ready to begin following these instructions.

1. Open the terminal and navigate to the desktop or the location you want to place your tessel program.
    ```bash
    cd Desktop
    ```
    Note that `cd` means "change directory".

2. Create a folder (also known as a directory) called Tessel. 
    ```bash
    mkdir Tessel
    ```
    Note that mkdir stands for "make directory" and it creates a folder named after the command that is typed after it, in this case "Tessel".

3. Now that the folder has been created, navigate into it. 
    ```bash
    cd Tessel
    ``` 

4. Clone the repository of code for climate monitoring on the tessel. 
    ```bash
    git clone https://github.com/Stegosaurius/Tessel_Climate_Monitoring
    ``` 
    This will copy the code found in the weblink and place it in the current folder.

5. Navigate into the newly created folder.
    ```bash 
    cd Tessel_Climate_Monitoring
    ```

6. (Optional) Display the contents of the current folder.
    ```bash
    ls
    ``` 
    This command stands for list and will show you the contents of the current directory.

7. Download all the code dependencies. 
    ```bash
    npm install
    ```
    This command tells npm to install the code dependencies defined in the package.json file found in the current directory.

8. Make a copy of the keenConfigure.example.js file. 
    ```bash
    cp keenConfigure.example.js keenConfigure.js
    ``` 
    The command `cp` stands for copy. It will create a copy of the file given after it `keenConfigure.example.js` to file given as a second command, `keenConfigure.js`. This particular file is where we will store the keys for accessing the keen database that the Tessel will upload to. In a later step, this file will be opened so that user specific keys can be added to it.

9. Make a copy of the wifiConfigure.example.js file.
    ```bash
    cp wifiConfigure.example.js wifiConfigure.js
    ```
    This file is where the wifi connection SSID name and password will be setup.  One might wonder at this point why there would need to be a copy of this file (or the file in the previous step). The reason for this is version control (git). Git has been configured (by modifying the .gitignore file) to ignore files named keenConfigure.js and wifiConfigure.js. Because of this, Git will not send sensitive passwords and keys to GitHub if a pull request is made.

10. Leave the terminal (but don't close it) and open Finder. Navigate to the folder that the Tessel repo was cloned into (it'll be on the desktop if the above commands were followed). Open keenConfigure.js in a text editor (TextEdit or notepad will work but if you're thinking about doing more coding in the future, try getting Sublime). Grab the `writeKey` from the top of this setup page, delete the "xxxxxxxxxxxxxxxxxx" and paste the key. The key should be in quotes `"theKeyHere"`. Also change `"username: "xxxxxxxxxxxxxxxx"` by deleting the x's and replacing them with the username found on your profile page.

11. Use the text editor to open wifiConfigure.js. Replace the x's after the SSID with the name of the wifi network. Replace the x's after the password with the wifi network password that the Tessel will be using.

12. Return to the terminal. Run 
    ```bash
    tessel run index.js -l
    ```
    This will compile the Tessel code and load it into the tessel. It will begin executing and sending data to Keen after the code has been compiled and sent to the tessel. The console will also begin loggin data for the Tessel (to stop the logs from streaming, press `ctrl+c`) Every time power is supplied to the Tessel it will load up the code and begin executing it again.


