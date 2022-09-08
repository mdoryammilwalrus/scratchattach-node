<div align="center">

<h1>Scratchattach</h1>

<h3>Scratch API wrapper with support for almost all site features - ported to NodeJS</h3>
 
<a alt="Made with NodeJS"><img src="https://img.shields.io/badge/Made%20with-Node.JS-6DA55F?style=for-the-badge&logo=node.js&logoColor=white"></a> 
<a href="https://github.com/mdoryammilwalrus/scratchattach-node/issues/" alt="GitHub issues"><img src="https://img.shields.io/github/issues/mdoryammilwalrus/scratchattach-node?style=for-the-badge"></a>
<a href="https://github.com/mdoryammilwalrus/scratchattach-node/graphs/contributors/" alt=""><img src="https://img.shields.io/github/contributors/mdoryammilwalrus/scratchattach-node?style=for-the-badge"></a>

</div>

This library can set cloud variables, follow Scratchers, post comments and do so much more! It has special features that make it easy to transmit data through cloud variables.

**Some functions require logging in to Scratch.**
**You also need to have NodeJS installed on your device.**
*Download NodeJS here if you don't have it: [nodejs.org](https://nodejs.org)*

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
*You can get your session id from your browser's cookies. [More information](#get-your-session-id)*

```js
const scratch3 = require('scratchattach-node')
session = scratch3.Session("sessionId", "username")
```

**Attributes:**
```js
session.session_id // Returns the associated session id
session.xtoken // xtoken
session.username // Returns the username of the account
session.email // Returns the email address associated with the account
session.banned // Returns True if the associated account is banned
session.new_scratcher // Returns True if the associated account is a New Scratcher
session.mute_status
```

# Cloud variables  `scratch3.CloudConnection`
*Make sure you're using the latest scratchattach version. Scratchattach will tell you in the console if there is a update. Update scratchattach with `npm update scratchattach-node`*

# Get your Session ID

This section explains how to get your Scratch session id from your browser cookies.

<h2 style="color:red">STOP!</h2>
Your session id allows anyone who has it full control over your Scratch account, delete all of your projects, or do many other harmful things! Never share your session id with anyone!

## For most browsers

1. Open scratch.mit.edu in your browser
2. Click the 🔒 icon in the URL bar, then click "Cookies"
3. Then find a cookie called `scratchsessionid` (in the "scratch.mit.edu" » "Cookies" folder). The content of this cookie is your Scratch session id

![Cookies Chrome](https://scratch3-assets.1tim.repl.co/template/cookies.png)

## For Firefox and other browsers

1. Open scratch.mit.edu in your browser
2. Open DevTools by holding CTRL + Shift + I
3. Click the Storage tab, then click "Cookies" to expand it. There will be a table that looks like this:

|Name             |Value   |
|-----------------|--------|
|permissions      |PERMS   |
|scratchcsrftoken |TOKEN   |
|scratchsessionsid|TOKEN   |

4. Triple-click on the value for "scratchsessionsid" and then hold CTRL + C to copy it

# Contributors

-   Almost all code by TimMcCool (https://github.com/TimMcCool/)
-   Ported to NodeJS by mdoryammilwalrus (https://github.com/mdoryammilwalrus)
-   Siddhesh (creator of scratchconnect) for some help and the profile comments API
-   DatOneLefty for ScratchDB which is used to fetch stats and ranks
-   Lynx for ScratchData (https://sd.sly-little-fox.ru/api/v1/search?q=)
