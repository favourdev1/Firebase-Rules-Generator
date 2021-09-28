---
description: This page explains how firebase rules work
---

# Understanding How Firebase Rules Work

Firebase Security Rules work by matching a pattern against database paths, and then applying custom conditions to allow access to data at those paths. All Rules have conditional statement allowing read or write access. You must define Rules for each Firebase Location/path  you use in your app.

### For Realtime Database, JSON-based Rules use the following syntax:

{% code title="Realtime Database" %}
```text
{
  "rules": {
    "<<path>>": {
    // Allow the request if the condition for each method is true.
      ".read": <<condition>>,
      ".write": <<condition>>
    }
  }
}
```
{% endcode %}

 

There are three basic elements in the rule:

* **Path:** The database location. This mirrors your database's JSON structure.
* **Request:** These are the methods the rule uses to grant access. The `read` and `write` rules grant broad read and write access, while `validate` rules act as a secondary verification to grant access based on incoming or existing data.
* **Condition:** The condition that permits a request if it evaluates to true.

Rules are applied as `OR` statements, not `AND` statements. Consequently, if multiple rules match a path, and any of the matched conditions grants access, Rules grant access to the data at that path. Therefore, if a broad rule grants access to data, you can't restrict with a more specific rule. You can, however, avoid this problem by making sure your Rules don't overlap too much. Firebase Security Rules flag overlaps in your matched paths as compiler warnings.

![Firebase is a document-store database where data is stored in one big JSON tree](https://www.cloudsavvyit.com/p/uploads/2020/05/2d6280da.png?trim=1,1&bg-color=000&pad=1,1)

image from : [cloudsavvyit.com ](https://www.cloudsavvyit.com/p/uploads/2020/05/2d6280da.png?trim=1,1&bg-color=000&pad=1,1)



 **Data in Firebase is stored in one big JSON tree.** Each branch of the tree can be modified at will, and changes to specific branches \(such as `/users/anthony/`\) can be subscribed to, allowing the client to listen for updates.





More Information on how database rules work can be found here at [Firebase Docs](https://firebase.google.com/docs/rules/rules-behavior#:~:text=How%20rules%20apply%20to%20paths)

{% hint style="success" %}
This page will be updated from time to time.
{% endhint %}

