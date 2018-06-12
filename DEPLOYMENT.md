* register [heroku](https://www.heroku.com/), [LINE](https://developers.line.me/), [OLAMI](https://www.olami.ai/), [KKBOX](https://developer.kkbox.com/) Developer account
* login heroku account
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