<template>
  <div id="app">
    <div class="sticky-container">
      <div class="title-bar sticky is-stuck is-at-top">
        <div class="title-bar-left">
          <span>LOGO</span>
          <router-link class="button" to="/">Home</router-link>
          <router-link class="button" to="/about">About</router-link>
        </div>
        <div class="title-bar-right">
          <a href="https://www.facebook.com/kaspar.tilk" class="social-logo social-logo-fb"></a>
          <a href="https://twitter.com/KasparTilk" class="social-logo social-logo-twitter"></a>
          <a href="https://www.linkedin.com/in/kaspartilk" class="social-logo social-logo-linkedin"></a>
        </div>
      </div>
    </div>
    <div class="body-content">
      <router-view/>
    </div>
  </div>
</template>

<style lang="scss">
@import "~foundation-sites/scss/foundation.scss";
@import "_settings.scss";
@include foundation-button;
@include foundation-title-bar;
@include foundation-sticky;

body {
  margin: 0;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.title-bar {
  padding-top: 0.5rem;
  padding-bottom: 0;
  box-shadow: 0 2px 5px 0 rgba(0,0,0,0.16), 0 2px 10px 0 rgba(0,0,0,0.12);

  a {
    text-decoration: none;
    font-weight: bold;
    color: white;
    border-bottom: 2px solid transparent;

    &.router-link-exact-active {
      border-bottom: 2px solid white;
    }
  }

  .button {
    margin: 0;
    background-color: transparent;
  }

  .social-logo {
    height: 24px;
    width: 24px;
    margin-left: 0.5rem;
    padding: 0;
    background-size: cover;
    background-repeat: no-repeat;
    display: inline-block;

    &-fb {
      background-image: url("./assets/flogo-HexRBG-Wht-58.svg");

      &:hover {
        background-image: url("./assets/f-ogo_RGB_HEX-58.svg");
      }
    }

    &-twitter {
      background-image: url("./assets/Twitter_Social_Icon_Rounded_Square_White.svg");

      &:hover {
        background-image: url("./assets/Twitter_Social_Icon_Rounded_Square_Color.svg");
      }
    }

    &-linkedin {
      background-image: url("./assets/In-White-28px-R.png");

      &:hover {
        background-image: url("./assets/In-2CRev-28px-R.png");
      }
    }
  }

  .title-bar-right {
    text-align: center;
  }
}

.body-content {
  padding-top: 50px;
}
</style>
