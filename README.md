# What is ExpressErr?

ExpressErr is a plugin for the Express framework that handles some of the most common error codes. 


## What can I do with ExpressErr?

You can choose to pass in the path to your custom error page or leave it blank and this function will return a default error message.

The following status codes are supported:

  * err400(errorpage) - *Bad Request*: Usually due to a client side error.

  * err401(errorpage) - *Unauthorized*: User is not authorized to view this page.

  * err403(errorpage) - *Forbidden*: User is not authorized to view this page or requires other permissions.

  * err404(errorpage) - *Not Found*: The requested resource cannot be found.

  * err408(errorpage) - *Request Timeout*: The server timed out waiting for the request.

  * err418(errorpage) - *I'm a teapot*: I'm a teapot!.

  * err500(errorpage) - *Internal Server Error*: Given when an unexpected condition was encountered and no more specific message is suitable.

  * err503(errorpage) - *Service Unavailable*: The server is currently unavailable.


## Useage

  In your app.js file:

```javascript
//Using from NPM
const expresserr = require('@boccinfusot/expresserr');

//Using raw files
const expresserr = require('path/to/expresserr.js');

// In your Route handling section 
app.use(function (req, res, next) {
  expresserr.err404();
});
```
