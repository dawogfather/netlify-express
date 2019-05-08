# Express.js on Netlify Example

[![Deploy to
Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/neverendingqs/netlify-express)

[![Netlify Status](https://api.netlify.com/api/v1/badges/e0dfb81b-1382-4f4b-b9df-80c1ef4aafe2/deploy-status)](https://app.netlify.com/sites/upbeat-shaw-840f8b/deploys)

An example of how to host an Express.js app on Netlify using
[serverless-http](https://github.com/dougmoscrop/serverless-http). See
[express/server.js](express/server.js) for details, or check it out at
https://netlify-express.netlify.com/!

[index.html](index.html) simply loads html from the Express.js app using `<object>`, and the
app is hosted at `/.netlify/functions/server`. Examples of how to access the
Express.js endpoints:

```sh
curl https://netlify-express.netlify.com/.netlify/functions/server
curl https://netlify-express.netlify.com/.netlify/functions/server/another
curl --header "Content-Type: application/json" --request POST --data '{"json":"POST"}' https://netlify-express.netlify.com/.netlify/functions/server
```
