# Frontend Starter
This is frontend starter template for the html team

## Requirements
- Nodejs (https://nodejs.org/en/download/)
- On Windows - Install C++ Build Tools for Windows (run command with administrator)
```sh
      npm install --global --production windows-build-tools
```

- Node.js native addon build tool (https://github.com/nodejs/node-gyp)
- Install the `Gulp CLI` command (optional):
```sh
      npm install --global gulp-cli

```

## Install
```sh
  git clone https://github.com/khacthienonline/template-frontend.git <projectname>
  cd <projectname>
  npm install

```
## Configuring the git and githook
###### Changing the origin
```sh
  git remote set-url origin https://bitbucket.org/<NEW_GIT_REPO>.git
  git checkout -b html
```
###### Installing the githook (comming soon)

The `husky` module will install git hook for you and when you run git command, the husky will run the npm script for you

```sh

  npm install husky --save-dev

```

## Development

###### Starting the server in development mode
```sh

  npm start

```
###### Installing the custom frontend component
```sh
  npm run install-module -- -p <componentname>  # for example: componentname is fc8-footer

```

###### Generating pages

```sh
# creating `src/html/{home.html, about-us.html, contact.html}`
  npm run create-page -- -p 'home about-us contact'

```
###### Generating modules (html and css)

```sh
 # creating `src/html/modules/banner.html` `src/stylesheets/module/_banner.scss`
 # and `src/html/modules/user.html` `src/stylesheets/module/_user.scss`
  npm run create-module -- -m 'banner user' # seperating by comma

```
###### Generating module javascript

```sh
 # creating `src/javascripts/modules/Banner.js` `src/javascripts/modules/User.js`
  npm run create-js -- -m 'banner user' # seperating by comma

```

###### Javascript Linter

```sh

  npm run standard

```
###### SCSS Linter

```sh

  npm run stylelint

```
## Production
###### Build
```sh

  npm run build

  # starting demo server
  npm run demo

```


## Pushing to the bitbucket
######
```sh

  git add .
  git commit -m "message"  # NOTE `PRECOMMIT HOOK` WILL RUN TO CHECK `JS LINT` AND `STYLELINT`
  git push origin html

```
