<template>
  <div id="app">
    <navbar></navbar>
    <div>
      <sidebar></sidebar>
      <main-content></main-content>
    </div>
  </div>
</template>

<script>
import { Navbar, Sidebar, MainContent } from '@/layout';

export default {
  components: { Navbar, Sidebar, MainContent },
};
</script>


<style lang="scss">
// Import Bulma's core
@import "~bulma/sass/utilities/_all";

// Set your colors
$primary: #8c67ef;
$primary-invert: findColorInvert($primary);
$twitter: #4099FF;
$twitter-invert: findColorInvert($twitter);

$black: #505050;

// Setup $colors to use as bulma classes (e.g. 'is-twitter')
$colors: (
    "white": ($white, $black),
    "black": ($black, $white),
    "light": ($light, $light-invert),
    "dark": ($dark, $dark-invert),
    "primary": ($primary, $primary-invert),
    "info": ($info, $info-invert),
    "success": ($success, $success-invert),
    "warning": ($warning, $warning-invert),
    "danger": ($danger, $danger-invert),
    "twitter": ($twitter, $twitter-invert)
);

// Links
$link: $primary;
$link-invert: $primary-invert;
$link-focus-border: $primary;

// Import Bulma and Buefy styles
@import "~bulma";
@import "~buefy/src/scss/buefy";

#app {
  height: 100%;
  min-height: 100%;
  //display: flex;
  //flex-direction: column;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  a i.fa,
  button i.fa {
    padding-right:8px;
  }
}

.menu-list a.router-link-exact-active,
.menu-list a.router-link-exact-active:hover {
  color: $primary-invert;
  background-color: #505050;
  border-radius: 0px;
}

.page {
  margin: 20px;
}

body {
  overflow: auto;
}

.bg-primary {
  background-color: rgb(0,159,110);
}
.bg-secondary {
  background-color: $light;
}
</style>
