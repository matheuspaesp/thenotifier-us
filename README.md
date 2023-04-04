# thenotifier-us
Inspired in [us-visa-bot](https://github.com/jeangnc/us-visa-bot), this bot notifies you the interview date for a US visa.
The audio notification will work if you're using macOS system and the script sends a Telegram message.

## How it works

The bot is quite simple. You provide some informations for the bot to sign in in your behalf on https://ais.usvisa-info.com/, and then he checks the nearest dates every few seconds, and when it finds a closer date it will send a notification.

## Installing

You'll need node 16+ to run the bot. Also, you'll have to install some dependencies:

```sh
npm install
```

## Usage

You need to create .env file like below:
```.env
USERNAME='<your username>'
PASSWORD = '<your password>'
SCHEDULE_ID = '<schedule id from appointment>'
FACILITY_ID = '<facility id form, use 56 for SP>'

BOT_ENABLED=false
BOT_TOKEN=<Telegram BOT token>
CHAT_ID=-<Chat ID from Telegram>
```

If you want to enable a specific bot in Telegram, modify tag BOT_ENABLED to true and add your token and chat ID to delivery a message when the script finds a closer date.

Then run 
```
./index.js <your current interview date, ex: 2023-01-01>
```

