# NotificationsApp-bettween-Heroku-and-SFDC-console--

The following instant messaging app makes possible to send instant notifications between a heroku app (which sends notification messages)  and the console in SFDC (which will display such messages). 

To achieve this we need these steps:

1- Define an event to send a notification message , this is done using SFDC platform events (inspired in Apache kafka)
2- Build the console app using lightning components: 

notificationConsole.cmp (consisting on a header, counter of notifications, the buttons to delete or mute the notifications and the list
to display the notifications) 
notificationConsoleController.js (
notificationConsoleHelper.js
notificationConsole.css 
