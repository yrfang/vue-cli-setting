# vue-cli-setting

> A Vue.js project support pug、sass/scss

## Using vue-loader to build .vue components
[vue-cli](https://github.com/vuejs/vue-cli) allows you to setup a basic Webpack + `vue-loader` project for you, with `.vue` files and hot-reloading working out of the box!

for example with mac command line:
```javascript=
//global setting to setup vue-cli
$ npm install -g vue-cli

//build up a vue project and its project name/description
$ vue init webpack your-vue-project

//cd the directory to your-vue-project
$ cd your-vue-project

//Start installing the dependencies by using npm again
$ npm install

//start the web server in development mode by using npm
$npm run dev
```
After running the web server, your-vue-project will start start the server on port 8080. The browser is ready.

![](http://i.imgur.com/ggJ6rRg.png)

## pug
Because we want to compile our pug to html on the brower. We use npm to install pug into our project.

```javascript=
$ npm install pug --save-dev
```

Then find your text editor and open the file: `your-vue-project/src/App.vue`, You will see the template with html as below:

```javascript=
<template>
  <div id="app">
    <img src="./assets/logo.png">
    <hello></hello>
  </div>
</template>
```

Let's use specify pug in template:

```javascript=
<template lang="pug">
#app
    img(src='./assets/logo.png')
    hello
</template>
```

Also, in the file: `your-vue-project/src/components/Hello.vue`:

```javascript=
<template lang="pug">
.hello
  h1 {{ msg }}
  h2 Essential Links
  ul
    li
      a(href='https://vuejs.org', target='_blank') Core Docs
    li
      a(href='https://forum.vuejs.org', target='_blank') Forum
    li
      a(href='https://gitter.im/vuejs/vue', target='_blank') Gitter Chat
    li
      a(href='https://twitter.com/vuejs', target='_blank') Twitter
    br
    li
      a(href='http://vuejs-templates.github.io/webpack/', target='_blank') Docs for This Template
  h2 Ecosystem
  ul
    li
      a(href='http://router.vuejs.org/', target='_blank') vue-router
    li
      a(href='http://vuex.vuejs.org/', target='_blank') vuex
    li
      a(href='http://vue-loader.vuejs.org/', target='_blank') vue-loader
    li
      a(href='https://github.com/vuejs/awesome-vue', target='_blank') awesome-vue
</template>
```

## sass/scss
Similarily, we also use npm to install css preprocessing compiler into our project.

```javascript=
npm install sass-loader node-sass --save-dev
```

Then we can use sass or scss in `App.vue` and `Hello.vue`.

```style=
<style lang="sass">
#app
  font-family: 'Avenir', Helvetica, Arial, sans-serif
  -webkit-font-smoothing: antialiased
  -moz-osx-font-smoothing: grayscale
  text-align: center
  color: #2c3e50
  margin-top: 60px
</style>
```

```style=
<style lang="sass" scoped>
h1, h2
  font-weight: normal

ul
  list-style-type: none
  padding: 0

li
  display: inline-block
  margin: 0 10px

a
  color: #42b983
</style>
```

## Happy coding
Now save the file. If you still have `npm run dev` running, Webpack will reload your changes automatically for you! In the browser `http://localhost:8080/` check out the below view if you will success compile.

![](http://i.imgur.com/ggJ6rRg.png)

## Reference
* [vuejs/vue-loader](https://github.com/vuejs/vue-loader)
* [gitBook vue-cli webpack模板中文文档](https://loulanyijian.github.io/vue-cli-doc-Chinese/pre-processors.html)
* [levibostian/webpack, Tachyons, pug, Vue.js web app.
Raw](https://gist.github.com/levibostian/96cc285d4235d73f09cdc22f2590ccba)
* [Vue.js 2 Quickstart Tutorial 2017](https://medium.com/codingthesmartway-com-blog/vue-js-2-quickstart-tutorial-2017-246195cfbdd2)
