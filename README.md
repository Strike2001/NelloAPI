# NelloAPI
The nello public API enables nello users to use nello functionalities programmatically. This API is designed to help nello users manage their nello ones using third-party apps.

#nello auth
https://nelloauth.docs.apiary.io/#reference

#nello public api
https://nellopublicapi.docs.apiary.io/#reference


```Java
NelloAPI api = new NelloAPI();
String token = api.requestTokenClientCredentials("<YOUR CLIENT ID>", "<YOUR CLIENT SECRET>");
List<Location> locations = api.getLocations(token);
if (locations != null) {
  api.setWebhook(token, locations.get(0), "<YOUR WEBHOOK URL>");
  api.deleteWebhook(token, locations.get(0));
  api.openDoor(token, locations.get(0));
}
```
