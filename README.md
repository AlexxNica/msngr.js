# msngr.js
[![npm version](https://badge.fury.io/js/msngr.svg)](http://badge.fury.io/js/msngr) [![Bower version](https://badge.fury.io/bo/msngr.js.svg)](http://badge.fury.io/bo/msngr.js) [![Build Status](https://travis-ci.org/KrisSiegel/msngr.js.svg)](https://travis-ci.org/KrisSiegel/msngr.js/)

## What is msngr.js?
msngr.js is a small library for facilitating communication between components through abstract messages within the same application be it server or client side. It also provides binding messages directly to DOM elements and even sending payloads between browser tabs / windows.

The following example shows how to bind a message to a click event of a DOM element while gathering up the values in the related inputs for payload delivery.

```HTML
<input type="text" name="Username" value="Kris" />
<input type="password" name="Password" value="hunter2" />
<button>Submit</button>
```

```javascript
msngr("User", "Save")
    .bind("button", "click")
    .option("dom", ["input"])
    .on(function (payload) {
        console.log(payload.Username); // Prints "Kris"
        console.log(payload.Password); // Prints "hunter2"
    });
```

## Getting msngr.js
If you want to use msngr.js on the server-side via npm simply install it via ```npm install msngr```.

If you want to use it within a web browser then either install via ```bower install msngr``` or manually download msngr.js or msngr.min.js file(s) from this repository.

## Would you like to know more?
While msngr.js isn't very large the documentation has been split up for easy reading.

[Full API](docs/api.md) - This is the full, exposed API that msngr makes available. This includes the methods that can be used (it does not cover internal methods or objects since those are subject to change) and examples for each.

[Web browser niceties](docs/web browser niceties.md) - This covers binding msngr.js to elements and events, unbinding them, how to gather up values from various types of elements and cross-window communication.

[Extending and hacking](docs/extending and hacking.md) - Want to extend the capabilities of msngr.js? It's actually quite easy and this document covers it. Using msngr.js deep in a production system then suddenly find *something* that you need to change to avoid catastrophe? Hacking msngr.js is also covered for those times when you need *unorthodox* solutions :)

[Contributing](docs/contributing.md) - Want to contributed to msngr.js? There are a couple of things you should know before you submit that pull request to better ensure it gets accepted :)

## Getting in contact
For questions, news, and whatever else that doesn't fit in GitHub issues you can follow me [@KrisSiegel](https://twitter.com/KrisSiegel)

Copyright © 2014-2015 Kris Siegel
