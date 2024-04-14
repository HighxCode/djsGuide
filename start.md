# discord.js@13 شرح كامل

## مقدمة:
**Introduction:**
discord.js is a JavaScript library for building Discord applications using Node.js. It allows you to create and manage bots and interact with the Discord API easily.

## التثبيت:
**Installation:**
To install discord.js@13, you can use npm or yarn:

```bash
npm install discord.js@13
```

Or

```bash
yarn add discord.js@13
```

## التوثيق:
**Documentation:**
There is official documentation for discord.js@13 available at the following link:
[discord.js Documentation](https://discord.js.org/#/docs/main/stable/general/welcome)

## المثال:
**Example:**
Let's create a simple bot that responds to "hello" messages with "world":

```javascript
const { Client, Intents } = require('discord.js');

const client = new Client({ intents: [Intents.FLAGS.GUILDS, Intents.FLAGS.MESSAGE_CREATE] });

client.on('ready', () => {
  console.log(`Logged in as ${client.user.tag}!`);
});

client.on('messageCreate', message => {
  if (message.content === 'hello') {
    message.reply('world');
  }
});

client.login('YOUR_TOKEN_HERE');
```

## شرح الكود:
**Code Explanation:**

### 1. Importing Required Modules:
We import the necessary modules from discord.js.

### 2. Creating a Client Instance:
We create an instance of the Client class with specific intents to listen for guild events and message creations.

### 3. Handling the 'ready' Event:
When the bot is ready, it logs a message to the console indicating its successful login.

### 4. Handling Message Events:
We listen for message events, and if the message content is 'hello', the bot replies with 'world'.

### 5. Logging In:
The bot logs in using its token.
