# katwekibs-letter-avatar
A simple JavaScript library that makes creating letter avatars like that of Google's gmail a piece of cake.

Just down load the letter avatar file and include it in your HTML files. 
Before the </body> closing tag of your HTML page, initialize the katweKibsAvatar object like bellow. 
    
    KatweKibsAvatar.init(); 

As basic as that code looks, the JavaScript part is almost done. Unless of course if you want to pass some settings. Read on. 

Now in your HTML page provide a canvas element with a class of "user-icon" and property called "data-name". Just as shown below. 

    <canvas class="user-icon" data-name="Chris Brown" width="200" height="200" data-chars="1"></canvas> 
    

There are two ways to provide settings for the katwekibs letter avatar. 
One from the canvas element. 
two from the initialization code. 
Any settings provided from the canvas element overrides the settings provided from the initialization code.


Data-name is a required property. 
It holds the names of the user from which katwekibs letter avatar javascript will populate the initials it will use to create the avatar. Without the data-name property in the canvas element, katwekibs letter avatar JavaScript won't work. 


User-icon is the default selector that tells katwekibs letter avatar JavaScript the canvas element to draw the avatar to, of course user-icon class name can be changed from the initialization code as shown in the initialisation code at the bottom. 


You can provide the width and height from the canvas element.  


DataChars determines the number of characters that will be shown as initials in the avatar image. 


If you want to change the default selector from user-icon to one of your choice, you need to change that from the initialization code as shown in the code below. 
a selector can be an id, or a class attribute. For example 
    
    katweKibsAvatar.init({
        selector:".your choice" // this is a class selector 
    });
    
    katweKibsAvatar.init({ 
        selector:"#your choice" // this is an id selector 
    }); 
    
Below is the initialization code. 
Settings provided here are overiden by the settings provided in the canvas element. 
Take note of spelling dataChars setting in the initialization code, it is different from that of data-chars in the canvas element      
    
    katweKibsAvatar.init({
        dataChars: 2, 
        width:100, 
        height:100, 
        selector:user-icon 
    });

    
