# GitlabWebhook

Express MiddleWare for gitlab webhook.

## Install

```js
npm install GitlabWebhook
```

## Requirement

Node 6.6.x

## Usage

```js
const express = require('express');
const http = require('http');
const webhook = require('gitlab-webhook');

const app = express();
 
app.use(express.bodyParser());
app.use(express.methodOverride());
app.gitlab('/123-gitlab-hook', {
  exec: 'jake deploy',
  token: 'CA572F1C-7BEB-467E-B26F-8999AB09CD4C',
  branches: '*'
});

http.createServer(app).listen(3000);
```
