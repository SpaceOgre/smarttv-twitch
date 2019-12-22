## About
Unofficial app for legacy Samsung SmartTV's which plays Twitch live broadcasts.

## Installation

### Official Samsung instructions

[Testing Your Application on a TV for 2014](https://developer.samsung.com/tv/develop/legacy-platform-library/art00121/index)

[Testing Your Application on a TV for 2013](https://developer.samsung.com/tv/develop/legacy-platform-library/d20/index)

[Testing Your Application on a TV for 2011](https://developer.samsung.com/tv/develop/legacy-platform-library/art00013/index)

### Followed Channels (optional)

To get access your followed channels you have to unpack the Twitch_XX_YYYYMMDD.zip from releases and edit the app/script/config.js file and enter your username or userid. Then repack everything as Twitch_XX_YYYYMMDD.zip.

Replace spaceogre here with your username:
``` javascript
var Config = {
    data: {
        username: 'spaceogre',
        userid: ''
    },
    clientId: 'kimne78kx3ncx6brgo4mv6wki5h1ko',
    webRequestTimeout: 1000,
    //fileName: curWidget.id + "_config.db",
    version: '3.9.2'
};
```

_I'm planing to add support for this from inside the app in the future._

### Host the Zip file on a Computer

You have to run some kind of web server or a specific app for installing SmartTV apps like SammyWidgets.

_Note: I could not get SammyWidgets to work so I just used [IIS](https://en.wikipedia.org/wiki/Internet_Information_Services) and put the zip in inetput/wwwroot._

### On the TV

On your TV, go to Menu->Smart Features->Samsung Account and type name "develop".

Then go to SmartHUB, click "More Apps" button, then click "Options" button and choose "IP Setting", put the IP address of your web server and finally choose "Start App Sync" option. Twitch app has to be installed now.

For 2014 models "More apps" button might be absent, if so try: long press the enter button on any app, then the menu will pop up, select IP Settings, put in the IP, then long press enter again and then Start User Apps Sync.

For models released before 2013 you might want to use these instructions instead:
From the SmartHUB main screen, click the "Tools" button on the remote. Only from the "Tools" menu, navigate to "Settings", and from there to "Development". (You still have to be logged in as 'develop')

## About this fork

The original fork is https://github.com/nikitakatchik/smarttv-twitch

I created this fork to add support for Followed Channels since it is the way I use Twitch the most. Since then I have also upgraded to use the Twitch API v5 instead of v3 and some other small changes.

### Status

I am still working on this from time to time but because life situations I'm very limited in testing it on my TV, but if you want something fixed/added please add an issue and I can try to fix it and then you have to test it for me :)
