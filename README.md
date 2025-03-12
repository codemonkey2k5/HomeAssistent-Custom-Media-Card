# HomeAssistent-Custom-Media-Card
A simple media player card for Home Assistant.  The default one is missing some buttons that I feel should be front and center.
This image is larger than what you will see on your dashboard.  The card is roughly the same size as the media card.  It can be scaled much larger.  
![image](https://github.com/user-attachments/assets/03815604-b80d-4aea-ac97-52b5c07aa3b2)

I have tested this card with Chrome and Microsoft Edge. It should work fine with a couple of very minor exceptions that I will mention below. 

Installation instructions:  (assumes you are using Studio Code Server)

First open Studio Code Server and find the WWW directory.  

Right click on WWW and create the File: music-assistant-controls.js

This will open up a blank file.  

Now copy the contents of Java Script Code for WWW to this blank file.  Do not save yet.

Find line 173: entity: "media_player.livingroom_chromecast",

Change the entity to match yours.  

Now save your file.  Almost done. :) 

Now go to SETTINGS, DASHBOARDS and click the 3 dots at the top right of the screen and click on RESOURCES.

At the bottom of the page, click on ADD RESOURCE.

Enter the following URL:     /local/music-assistant-controls.js

The type should be: JavaScript module

Save that.

Now you can add the card to your dashboard.

Do that by creating a new manual card and entering the following yaml code:  (make sure you enter the correct entity)  

-

type: custom:music-assistant-custom-card

entity: media_player.livingroom_chromecast

scale: 1

-

Use scale to scale the size of the card.  1 is 100%  1.1 is 110%.  The card will be clipped if you go below 1.  

You should now have a media player card that looks like the one above.  


This card has a couple small issues:
1. The mute button does not toggle.  It will mute, then you have to either hit + or - to unmute.  (If anyone can help me fix that I would be greatful.)
3. The shuffle button will change state one time, but not toggle.  (If anyone can help me fix that I would be greatful.) 
4. The album art insists on overlapping the lower portion of the card just a little. (If anyone can help me fix that I would be greatful.) 

I am not a coder, I bodged this together with a lot of AI assistance.  If you think you can improve on it, please feel free.  Just let me know please and I'll review your changes.  
Lastly, this is the first time I have ever put anything on GitHub, so if there is something I didn't do right, please let me know.  

Thanks!  




