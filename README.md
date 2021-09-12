# Tutorial no 1
In this Tutorial we will make basic codes for bot and we will host Bot 24hr for free!

# Requirements 
```
1. Node v16
2. Npm v7
3. A code editor / online code editor (replit, glitch)
4. Terminal
```
# Checking Things/Stuffs
Before starting the project we have to first check our versions.
<br />
Let's check node version.(Remember that discord.js v13 uses node v16 and will not work if you have node v12 or lower than 16)
<br  />

# Checking Node version
If you are using private code editor like vscode, then follow the step;
```
1. Open your terminal 
2. Type "node -v" (remember you must have installed node v16)
```
If it shows `node v16.something`, then you have your node version updated to node v16!
<br />
If not then follow the steps ;
```
1. Delete your previously installed node(If you haven't installed before then skip)
2. Open Chrome and type 'node.js'.
3. Go to the official site of node.js and install the latest version
```

Now if you are using online code editor like replit.com, then follow the steps to check version;

```
1. Open shell 
2. Type node-v
```
If it shows node v12, then your repl not updated to node v16.
<br />
So for updating the things in replit.com , I have made the video on youtube! You can also check out the guide;
<br /> 
👉 Guide :- [[Guide Github]](https://github.com/CrauxDEV/Replit-upgradation-)
 
# Let's start 
After checking and updating to everything , now let's make bot's basic code, you can check out the files for better code!
<br />
First open code and editor and make a new file named `index.js`, if you have already this file then skip.
<br />
Now copy and paste the following codes / you can read and write;
```js
const { Discord, Client, Intents, Collection } = require('discord.js');

const fs = require('fs');
const client = new Client({
    intents: [
        "GUILDS",
        "GUILD_MEMBERS",
        "GUILD_BANS",
        "GUILD_INTEGRATIONS",
        "GUILD_WEBHOOKS",
        "GUILD_INVITES",
        "GUILD_VOICE_STATES",
        "GUILD_PRESENCES",
        "GUILD_MESSAGES",
        "GUILD_MESSAGE_REACTIONS",
        "GUILD_MESSAGE_TYPING",
        "DIRECT_MESSAGES",
        "DIRECT_MESSAGE_REACTIONS",
        "DIRECT_MESSAGE_TYPING",
    ],
});

client.commands = new Collection();
client.aliases = new Collection();

const express = require('express');

const app = express();

app.get('/', (req, res) => {
  res.send('Hello Express app!')
});

app.listen(3000, () => {
  console.log('server started');
});

client.once('ready', () => {
  console.log(`${client.user.tag}`)
});

client.login('token');
```
If you are using some online code editor,  then modify small things in code. First make a new file named `.env`, you can check the files given above for syntaxes.
```js 
const { Discord, Client, Intents, Collection } = require('discord.js');

const fs = require('fs');
const client = new Client({
    intents: [
        "GUILDS",
        "GUILD_MEMBERS",
        "GUILD_BANS",
        "GUILD_INTEGRATIONS",
        "GUILD_WEBHOOKS",
        "GUILD_INVITES",
        "GUILD_VOICE_STATES",
        "GUILD_PRESENCES",
        "GUILD_MESSAGES",
        "GUILD_MESSAGE_REACTIONS",
        "GUILD_MESSAGE_TYPING",
        "DIRECT_MESSAGES",
        "DIRECT_MESSAGE_REACTIONS",
        "DIRECT_MESSAGE_TYPING",
    ],
});

client.commands = new Collection();
client.aliases = new Collection();

const express = require('express');

const app = express();

app.get('/', (req, res) => {
  res.send('Hello Express app!')
});

app.listen(3000, () => {
  console.log('server started');
});

client.once('ready', () => {
  console.log(`${client.user.tag}`)
});

client.login(process.env.TOKEN);
```
