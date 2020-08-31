### bmPushNotification

index.js
This is a small nodejs script that will connect to the Brandmeister server and send you a push notification for any new transmission.
A new transmission is defined as a transmission after X seconds of silence.  By default, X is 900 (15 minutes)

tg.js
This is a small nodejs script that connects to the Brandmeister server and outputs transmission information. This is a modified copy of index.js.
This can be used on PC or on Android using Termux.  

If you don't have nodejs installed, that will be step 1 (don't know if it's installed? Go to a command prompt and type `node`)

After cloning this repo and entering the folder, edit `index.js` and/or `tg.js` to define your preferred talkgroups and enter your pushover userkey & token (https://pushover.net/).  Supports more than one if you want to run this service for multiple users that want to be notified about the same talkgroup activity.

Android Instructions:
Install Termux from the F-droid repo.
Open Termux
install wget using `pkg install wget`
get the index.js script using `wget https://raw.githubusercontent.com/clewisit/bmPushNotification/master/index.js`
get the tg.js script using `wget https://raw.githubusercontent.com/clewisit/bmPushNotification/master/tg.js`
Install node.js using the command `pkg install nodejs`
run `npm install`
run `npm install socket.io-client`
run `npm install moment`
run `npm install node-cache`

Finally, run `node tg.js` or `node index.js` to start the program.  
