* Register [heroku](https://www.heroku.com/), [LINE](https://developers.line.me/), [OLAMI](https://www.olami.ai/), [KKBOX](https://developer.kkbox.com/) Developer account
* Log into [LINE](https://developers.line.me/) admin console
    * Messaging API -> Start now
    * Add new provider -> Input [Provider name] -> Confirm -> Create
    * [Provider name] -> Messaging API
    * Fill the Channel settings & Issue new Channel access token 
    * Plan => Free (Not Developer Trial)
    * copy the Channel secret & Channel access token
* Log into [OLAMI](https://www.olami.ai/) admin console
    * 建立新應用 -> Fill the app infomation
    * App -> 變更設定 -> check the music NLI
    * copy the App Key/Secret
* Log into [heroku](https://www.heroku.com/) account
    * create new app
    * App Page -> Reveal Config Vars
    * Setup vars in blow
        * FLASK_ENV = production
        * LINE_CHANNEL_ACCESS_TOKEN = [YOU_LINE_CHANNEL_ACCESS_TOKEN]
        * LINE_CHANNEL_SECRET = [YOUR_LINE_CHANNEL_SECRET]
        * OLAMI_APP_KEY = [YOUR_OLAMI_APP_KEY]
        * OLAMI_APP_SECRET = [YOUR_OLAMI_APP_SECRET]
    * App Page -> Deploy
    	* Heroku Git
* Local Terminal console
    * Install Heroku CLI tools
	* Clone the GitHub repo. & publish the repo. to Heroku

```
$ git clone https://github.com/johnliu55tw/music-line-bot.git
$ cd music-line-bot
$ heroku login
$ heroku git:remote -a [YOUR_HEROKU_APP_NAME]
$ git push heroku master
```

* Log into [LINE](https://developers.line.me/) admin console
    * Use webhooks => Enable
    * Webhook URL => https://YOUR_HEROKU_APP_NAME.herokuapp.com/message
    * Auto-reply messages => Disable


