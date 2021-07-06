# vimeo-blob-upload
Vimeo nodejs client to upload videos from blob.

# Install

Using npm in Node.js project
> npm install vimeo-blob-upload

# Setup

Once the module is installed in your project, you must import it to be able to use it.

```javascript
const vimeo = require('vimeo-blob-upload');

var vimeoClient = new vimeo(clientID, clientSecret, accessToken);
```

# Upload from video file (blob)


```javascript
const vimeo = require('vimeo-blob-upload');


var vimeoClient = new vimeo(clientID, clientSecret, accessToken);

//Call the uploader
var params = {
    video: file,
    name: 'name',
    description: 'description',
    folder: 'vimeo folderID' //Optional if you want to upload the file to a specific folder
};

//Return a promise
vimeoClient.uploadFromBinary(params).then(res => {
    console.log(res);
}).catch(err => {
    console.log(err);
});

```