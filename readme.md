###bs-snippet-injector-eb
Write & Remove the BrowserSync Snippet to a file (Fork from https://www.npmjs.com/package/bs-snippet-injector to support using a `<!--BS:SNIPPET-->` comment instead of the end `</body>` tag)

This is an alternative to using the BrowserSync proxy.

##Install 

```bash
$ npm install browser-sync bs-snippet-injector-eb
```

###Example

```js
// requires version 1.3.3 of BrowserSync or higher.
var browserSync = require("browser-sync");

// register the plugin
browserSync.use(require("bs-snippet-injector-eb"), {
    // path to the file containing the closing </body> or <!--BS:SNIPPET--> tag
    file: "app/design/frontend/project/template/page/1column.phtml" 
});

// now run BrowserSync, wathching CSS files.
browserSync({
  files: "skin/frontend/project/assets/css/*.css"
});
```
