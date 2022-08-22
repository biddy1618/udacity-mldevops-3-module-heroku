## Steps
* Install the Heroku CLI. I used the Ubunutu installation instructions: curl https://cli-assets.heroku.com/install.sh | sh
* Type 'heroku' to see the full list of commands.
* To create an app with a specific name and to specify it as Python app use: `heroku create name-of-the-app --buildpack heroku/python`
* * Note that manually specifying it as a Python app is not necessary. Heroku will automatically try and detect the language of your app. In the case of Python it searches for either a requirements.txt or setup.py.
* We can view our apps buildpacks using `heroku buildpacks --app name-of-the-app`.
* Now we'll initiate our folder as a git repository and commit it so we can connect it to our new Heroku app.
```bash
git init
git add *
git commit -m "Initial commit."
```
* Connect the repo to our new app: `heroku git:remote --app name-of-the-app`.
* * The app will launch after a few moments.
* Enter into the Heroku VM using: `heroku run bash --app name-of-the-app`.
* * There is not much to see here. Explore the various Unix commands such as `pwd`, and `ls`. Doing `ls ..` reveals many of the standard folders one would expect in a Unix environment. Note this is very lightweight, not even vi is included!