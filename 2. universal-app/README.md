#Universal app - React / Redux
Makes sure you have Node (>=6.x).
Uses `gulp`, not npm scripts, so make sure you have `gulp-cli` as a global node package (might require a new terminal session postinstall).
```bash
npm i -g gulp-cli
```


## Getting started
```bash
git clone https://github.com/este/este universal-app

cd universal-app
npm i
gulp
```


###Troubleshooting
Remember nvm?
```bash
nvm install v6.2.0
nvm use v6.2.0
rm -rf node_modules
npm cache clean
npm i # Again
gulp
```

#### Read more
See a bunch of other docs ↗️ [here](https://github.com/este/este).

#### Tip
BTW, this is just one of the boilers. There's a cool tool to find the right Universal React boiler: ↗️ [tool](http://andrewhfarmer.com/starter-project/). Feel free to try others.


## Requirements for curios students
`iOS`: you need a Mac & SDK (Xcode)

`Android`: you need Android SDK and a lot of patience

> *NBNBNB*: you absolutely need to set `node v6+` as a default in your shell. For example in zsh you can add `nvm use v6.2.0` to your zshrc file & `source ~/.zshrc` to reload it. 
> 
> For bash `nvm alias default v6.2.0` should work fine. See [this](http://stackoverflow.com/questions/24585261/nvm-keeps-forgetting-node-in-new-terminal-session) thread.


===========================================================


> Happily maintained dev stack and starter kit for React universal apps. One stack for browser, server, mobile. Forget about [evil frameworks](http://tomasp.net/blog/2015/library-frameworks/), use laser focused [libraries](https://github.com/este/este#libraries) and design patterns instead.
 
Read all the docs ↗️ [here](https://github.com/este/este).


## About

- Truly universal architecture
  - code shared across platforms (browser, server, native mobile)
  - server side rendering
  - universal data fetching (unique approach without react-router)
  - an optional rendering to HTML files (for static hostings)
  - universal internationalization with runtime language switching
  - universal crash reporting via Sentry
  - universal forms with universal validation (universal ftw, yeah)
- Functional works (immutability, hot reload, time traveling)
- Test driven development
- Advanced performance with pure components
- Well tuned dev stack (OS X, Linux, Windows)
- Firebase Redux integration ([este.firebaseapp.com](https://este.firebaseapp.com))
  - useful predefined actions
  - email and facebook login
  - declarative queryFirebase higher order component for Firebase imperative api
- Este is monorepo, [read](https://github.com/babel/babel/blob/master/doc/design/monorepo.md) [why](http://danluu.com/monorepo/).

## Libraries

- [react](http://facebook.github.io/react/) and [react native](https://facebook.github.io/react-native/)
- [redux](http://rackt.github.io/redux/)
- [babeljs](https://babeljs.io/)
- [immutablejs](http://facebook.github.io/immutable-js)
- [react-router](https://github.com/rackt/react-router)
- [react-router-redux](https://github.com/reactjs/react-router-redux)
- [react-intl](https://github.com/yahoo/react-intl)
- [redux-storage](https://github.com/michaelcontento/redux-storage)
- [webpack](http://webpack.github.io/)
- [expressjs](http://expressjs.com/)
- [eslint](http://eslint.org/)
- [formatjs](http://formatjs.io/) Universal internationalization.
- [react-helmet](https://github.com/nfl/react-helmet) A document head manager for React.
- [webpack-isomorphic-tools](https://github.com/halt-hammerzeit/webpack-isomorphic-tools)
- [chriso/validator.js](https://github.com/chriso/validator.js) For simple yet powerfull Este sync/async validation.
- [bluebird](https://github.com/petkaantonov/bluebird) Because it's better than native implementation.
- [mochajs](https://mochajs.org/) The fun, simple, flexible JavaScript test framework.
- SASS or plain CSS with [autoprefixer](https://github.com/postcss/autoprefixer)
- [shortid](https://github.com/dylang/shortid) Short id generator. Url-friendly. Non-predictable.
- [gulp](http://gulpjs.com/) Aren't NPM scripts better? [No](https://twitter.com/jaffathecake/status/700320306053935104).
- [raven-js](https://github.com/getsentry/raven-js) Crash reporting client for [Sentry](https://getsentry.com).
- [gulp-real-favicon](https://www.npmjs.com/package/gulp-real-favicon) Generate a multiplatform favicon with [RealFaviconGenerator](https://realfavicongenerator.net)
- And much more. Explore the repository.


## Start Development

- run `gulp`
- point your browser to [localhost:8000](http://localhost:8000)
- build something beautiful

React Native: [Getting Started](https://facebook.github.io/react-native/docs/getting-started.html)

## Dev Tasks

- `gulp` run web app in development mode
- `gulp ios` run iOS app in development mode
- `gulp android` run Android app in development mode
- `gulp -p` run web app in production mode
- `gulp mocha` run mocha unit tests
- `gulp mocha-watch` continuous test running for TDD
- `gulp eslint` eslint
- `gulp eslint --fix` fix fixable eslint issues
- `gulp messages-extract` extract messages for translation
- `gulp messages-check` check missing and unused translations
- `gulp favicon` create multiplatform favicon

## Production Tasks

- `gulp build -p` build app for production
- `npm test` run all checks and tests
- `node src/server` start app, remember to set NODE_ENV and SERVER_URL
- `gulp to-html` render app to HTML for static hosting like [Firebase](https://www.firebase.com/features.html#features-hosting)
- `gulp deploy-heroku` deploy [Heroku](https://www.heroku.com/) app
- `gulp deploy-firebase` deploy [Firebase](https://firebase.google.com/) app
- `gulp deploy-firebase-database` deploy Firebase database only

## Documentation

For absolute beginners, see: [react-howto](https://github.com/petehunt/react-howto).

So you've decided to give this web stack a chance, but where is the documentation? Code is documentation in itself as it illustrates various patterns, but to start with you should educate yourself on [React.js](http://facebook.github.io/react/) and [Redux](http://redux.js.org/). You should [learn ES6](https://babeljs.io/docs/learn-es6/) to refresh your knowledge about "new" JavaScript practices and syntax. This stack uses [immutable.js](http://facebook.github.io/immutable-js/) and class-less design for a [good reason](https://github.com/facebook/immutable-js/#the-case-for-immutability). [Express.js](http://expressjs.com/) is used on the [Node.js](http://nodejs.org/api/) based server. The application architecture is [universal](https://medium.com/@mjackson/universal-javascript-4761051b7ae9) so we can share code between the browser, server, & mobile platform easily. Congrats, you're Este.js expert level 1 now :-)


## Support Este development

<img alt="Support Este development QR code" src="http://i.imgur.com/btUZ0IU.png" width="115" height="115">

## Credit

<img alt="Este.js" src="https://cloud.githubusercontent.com/assets/66249/6515278/de638916-c388-11e4-8754-184f5b11e770.jpeg" width="200">

Made by Daniel Steigerwald, [twitter.com/steida](https://twitter.com/steida) and the community.
