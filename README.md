# NotificationsApp-bettween-Heroku-and-SFDC-console--

The following instant messaging app makes possible to send instant notifications between a heroku app (which sends notification messages)  and a console app (built with lightning components) in SFDC which will display such messages. 

To achieve this we need these steps:

1- Define an event call "Notification" which will post a notification message whenever the event occurs, this is done using the SFDC functionality called platform events (inspired in Apache kafka). See the screenshot in this GIT repository "define platform event called notifications" 

2- Build the console app using lightning components to display the notifications: 

notificationConsole.cmp (consisting on a header, counter of notifications, the buttons to delete or mute the notifications and the list
to display the notifications) 

notificationConsoleController.js (hard coded messages to indicate app starts, control to mute/unmute pop-ups when notifications arrive) 

notificationConsoleHelper.js (display the intermmitent pop-ups whne notifications arrive)

notificationConsole.css (dimensions of the console app)

3-Incorporate the CometD funtionality into the console app. THe CometD library enables to receive messages in a pub/sub way over the web, in this way the console will be able to display the messages. 

To do this the CometD client has to be downloaded and stored as part of static resources. Also we need to add the corresponding code to the different components of the console app (the component, controller and helper). This will allows to among other things:

-load the CometD library from static resources 
-configure the CometD client and connect it to SFDC
-subscribe to the event "Notifications"
-when an event is recieved extract the content to be displayed in the console app

4- On the other hand the Heroku app is already prepared to publish  the events in question called "Notifications"

5- The final result is: Whenever the Heroku app sends a message this is displayed in our console app. see file "msgHerokuapptoSFDC" uploaded in this GIT repository as an example.

