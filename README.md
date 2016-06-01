# Prerequisites 🤕
- [Vue app](./1. vue-app) -> Node (>=4.x)
- [Universal app](./2. universal-app) -> Node (>=6.x)


## How to Node.js like a boss 👸
The Node release cycle is impressive to say the least. In order to not get caught with your pants down, use [nvm](https://github.com/creationix/nvm).

Don't believe me? Most projects I've started on went through `v0.12.0` → `v4.0.0` → `v5.0.0` → `v6.0.0` → ~~💩~~ / 🔥


### nvm 101 
```bash 
# Install nvm ☁️
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.31.1/install.sh | bash

# Install a node version ☁️ (might require a new terminal session)
nvm install v6.2.0 

# Use a node version ⬡
nvm use v6.2.0

# Revert to system node ⬡
nvm deactivate
```
Remember, you need to do this for each new terminal session (incl. new tabs).

ProTip™: Configure your shell to use a certain nvm version so you have new versions as default.
There are also some cool plugins, like [avn](https://github.com/wbyoung/avn), to *automagically* switch the node version per project. In theory it should make your life easier, but you might find yourself manually switching just to have more control.


## JavaScript frameworks: love & hate 💔 
1. Accessibility, semantic structure (proper HTML) ↗️ [read](http://alistapart.com/article/let-links-be-links)
youre-missing-the-point-of-server-side-rendered-javascript-apps/)
2. Hard to progressively enhance ↗️ [read](http://alistapart.com/article/interaction-is-an-enhancement)
3. Slow first render 🔄 ↗️ [read](http://tomdale.net/2015/02/
4. Not friendly with 🤖

###1 & 2. Common examples
```html
<span ui-sref="read-more" class="btn">Read more</span>

<!-- Or even worse -->
<span ng-click="goToReadMore()" class="btn">Read more</span>

<!-- Instead of -->
<a href="read-more" ui-sref="read-more" class="btn">Read more</a>
```

```html
<form>
  <input type="text" ng-model="email"/>
  ...
  <button ng-click="signUp()">Sign up</button>
</form>

<!-- Instead of -->
<form ng-submit="signUp()">
  <input type="text" ng-model="email"/>
  ...
  <button>Sign up</button>
</form>
```

###3 & 4. Solutions
Don't be ↗️ [Virgin america](https://www.virginamerica.com/).

🌠 Meteor [Spiderable](https://atmospherejs.com/meteor/spiderable)

A more general solution is [Prerender](https://github.com/prerender/prerender). The difference between a [JS site](https://www.hopper.dk/mekaniker/brondby/es-motor) vs a [prerendered site](https://www.hopper.dk/mekaniker/brondby/es-motor?_escaped_fragment_=)


But there's a [better way](./2. universal-app)...


##Troubleshooting
Things keep breaking? Feel free to [open an issue](https://github.com/danmindru/frameworks-demos/issues).