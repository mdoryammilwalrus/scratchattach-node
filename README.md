Scratch API wrapper with support for almost all site features - ported to NodeJS

This library can set cloud variables, follow Scratchers, post comments and do so much more! It has special features that make it easy to transmit data through cloud variables.

**Some functions require logging in to Scratch.**
**You also need to have NodeJS installed on your device.**
*Download NodeJS here if you don't have it: [https://nodejs.org](https://nodejs.org)*

The project was made by TimMcCool for Python and ported to NodeJS by me

# Installation

Run the following command in your command prompt / shell:
```
npm install github:mdoryammilwalrus/scratchattach-node
```

# Logging in  `scratch3.Session`

**Logging in with username / password:**

```js
const scratch3 = require('scratchattach-node')
session = scratch3.login("username", "password")
```

`login()` returns a `Session` object that saves your login

**Logging in with a sessionId:**
*You can get your session id from your browser's cookies. [More information](about:blank)*

```js
const scratch3 = require('scratchattach-node')
session = scratch3.Session("sessionId", username="username")
```

**Attributes:**
```js
session_id // Returns the associated session id
session.['user']['token'] // xtoken
session.['user']['username'] // Returns the username of the account
session.['user']['email'] // Returns the email address associated with the account
session.['user']['banned'] // Returns True if the associated account is banned
session.['permissions']['new_scratcher'] // Returns True if the associated account is a New Scratcher
session.['permissions']['mute_status']
```

# Cloud variables  `scratch3.CloudConnection`
*Make sure you're using the latest scratchattach version. Scratchattach will tell you in the console if there is a update. Update scratchattach with `npm update scratchattach-node`*
