# Live Timeline

**A Facebook-like timeline**

This tutorial will guide you through the development of the app.

We will be introducing new concepts on each step, so make sure you understand what's going on before going further!
If you have any doubts, please ask your coach for help.

## Setup your Firebase
You need to create a new app on [Firebase](https://www.firebase.com/) (the Free Plan is enough) and you need to configure it.
### Firebase rules

```
{
 "rules": {
  ".read": true,
  ".write": true,
  "posts": {
    "$post": {
    ".validate": "newData.hasChildren(['title', 'body']) && newData.child('title').isString() && newData.child('body').isString() && newData.child('title').val().length > 1 && newData.child('body').val().length > 1",
    ".read": true,
    ".write": true
    }
  }
 }
}
```

## Key concepts

During the workshop we will be covering the following concepts:

### JavaScript
  * Base values: `String`, `Number`, `Boolean`, undefined values
  * Variables and functions
  * Compound values: `Array` and `Object`
  * Language Structure: `if`, `return`
  * Global methods: `setInterval`
  * Array methods: `forEach`
  * HTTP-related methods: `fetch`

### The DOM
  * `Element` and some of its properties and methods (`querySelector`, `innerHTML`)
  * The events and the event object main properties (`target`, `preventDefault`)
