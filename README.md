# Hubot

Originally forked from https://github.com/github/hubot

This version is adapted for the Calcentral XMPP server

## Creating the bot

1. Clone this repository
```bash
git clone git://github.com/christianv/hubot.git
```

2. Create the instance on heroku
```bash
heroku create etsdevbot --stack cedar
```

3. Adding the RedisToGo addon (you need a verified account)
```bash
heroku addons:add redistogo:nano
```

4. Setting heroku environment variables
```bash
heroku config:add HUBOT_XMPP_HOST=media.berkeley.edu
heroku config:add HUBOT_XMPP_PASSWORD=______
heroku config:add HUBOT_XMPP_PORT=5222
heroku config:add HUBOT_XMPP_ROOMS=calcentral@conference.media.berkeley.edu
heroku config:add HUBOT_XMPP_USERNAME=______@media.berkeley.edu
```

5. Push to heroku
```bash
git push heroku master
```

6. Start the app
```bash
heroku ps:scale app=1
```

## Extra settings

* [Uptime Robot](https://github.com/github/hubot-scripts/blob/master/src/scripts/uptime-robot.coffee) http://www.uptimerobot.com/
```bash
heroku config:add HUBOT_UPTIMEROBOT_APIKEY=______
```

More scripts at http://hubot-script-catalog.herokuapp.com/

## Issues along the way

* Creating the Procfile
* Only works with certain versions of node/npm and hubot
* Finding the right settings for XMPP
