---
description: Paths are location which holds information in your database.
---

# Adding Paths to Your Project

Each Path/location in your database contain various  information and may contain various degree of security . This is possible in the `Location Tile page.`

### Adding Location/Path

You can add paths/location with as much level deep as possible. How ever it is advisable to keep your database as flat as possible.

> Because the Firebase Realtime Database allows nesting data up to 32 levels deep, you might be tempted to think that this should be the default structure. However, when you fetch data at a location in your database, you also retrieve all of its child nodes. In addition, when you grant someone read or write access at a node in your database, you also grant them access to all data under that node. Therefore, in practice, it's best to keep your data structure as flat as possible

According to[ Firebase Docs](https://firebase.google.com/docs/database/android/structure-data).

When You create a location for your database, you can find few information such as the `project name`, the `current status` of such location\(`locked mode`, `Full Access` or `custom)` available. 

Each of this tells you the current status of such a location/path

For `locked mode`, it means that no one has any access to such a database location. This is the default mode during creation.

* For `locked Mode`, it means that no one has any access to such a database location. This is the default mode during creation.
* For `Full Access Mode`, it means that anyone can have access access to such a database location. to edit, delete and update all data in such a `location /path.`
* For  `Custom mode`, it means that you have set some security rules for such a `location/path.` 

### WildCard

If you want to use the location/path as a wild card, while creating it , put a $ _dollar sign_  in front of the location name. for example `$myLocation.`

 The _dollar sign_ in `$myLocation` indicates that it's a wildcard. You an name wildcards whatever you like.  You could have named it `$broccoli`... but then you'd have to refer to the wildcard as `$roccoli` in your condition statements :\)

### Adding Security Rules For A Path/Location

To add security rules to  a `path/location` click on the small option button beside the project. More information on adding security rules can be found [here!](adding-security-rules.md)

### Deleting Path/Location

To delete a `path/location` click on the small option button beside the project.



### Viewing Generated Rule on Path/Location

You can view generated rules in each location . In order to View the generate rules in each path/location, you must be signed up to do so.

 To View the generate rules in each path/location click on the small info button found beside the `path/location` name. 



### Searching A Path/Location

In some cases, You could have many `location/path` in a particular project and navigating between them could seem stressful, This is why we provided the big search button on the top left 



### Renaming A Path/Location

`//feature in progress`

