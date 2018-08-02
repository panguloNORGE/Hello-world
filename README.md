# NotificationsApp-bettween-Heroku-and-SFDC-console--

The following instant messaging app makes possible to send instant notifications between a heroku app (which sends notification messages)  and the console in SFDC (which will display such messages). 

To achieve this we need these steps:

1- Define an event which will post a notification message whenever the event occurs, this is done using the SFDC functionality called platform events (inspired in Apache kafka). See the 
2- Build the console app using lightning components to display the: 

notificationConsole.cmp (consisting on a header, counter of notifications, the buttons to delete or mute the notifications and the list
to display the notifications) 
notificationConsoleController.js (
notificationConsoleHelper.js
notificationConsole.css 

3-Use CometD into the lightning console app (CometD is a library to receive messages in a pub/sub 
download 
