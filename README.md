driebit/node
============

A Docker image for compiling frontend assets. 

Usage
-----

Add some scripts to your project’s `package.json`:

```json
{
    "name": "your-project",
    "scripts": {
        "start": "webpack --config config/webpack.dev.js --watch --progress --profile --bail",
        "build": "webpack --config config/webpack.prod.js --progress --profile --bail"
    },     
}
```

Then run this container. Make sure to mount your project directory into `/app`,
which will run npm install and npm run:

```bash
docker run -it -v `pwd`:/app driebit/node 

npm info it worked if it ends with ok
...

```
